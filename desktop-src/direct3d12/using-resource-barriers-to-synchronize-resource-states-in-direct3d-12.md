---
title: Como usar barreiras de recursos para sincronizar estados de recursos no Direct3D 12
description: Para reduzir o uso geral da CPU e habilitar o multi-threading e o pré-processamento do driver, o Direct3D 12 move a responsabilidade do gerenciamento de estado por recurso do driver gráfico para o aplicativo.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df27e7997b4f3f56ae8e87688e5cc136dc7eb87d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343471"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a>Como usar barreiras de recursos para sincronizar estados de recursos no Direct3D 12

Para reduzir o uso geral da CPU e habilitar o multi-threading e o pré-processamento do driver, o Direct3D 12 move a responsabilidade do gerenciamento de estado por recurso do driver gráfico para o aplicativo. Um exemplo de estado por recurso é se um recurso de textura está sendo acessado no momento como por meio de um Modo de Exibição de Recursos sombreador ou como uma Exibição de Destino de Renderização. No Direct3D 11, os drivers eram necessários para acompanhar esse estado em segundo plano. Isso é caro da perspectiva da CPU e complica significativamente qualquer tipo de design multi-threaded. No Microsoft Direct3D 12, a maioria dos estados por recurso é gerenciada pelo aplicativo com uma única API, [**ID3D12GraphicsCommandList::ResourceBa ltd.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

-   [Usando a API ResourceBa fox para gerenciar o estado por recurso](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [Estados de recurso](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [Estados iniciais para recursos](#initial-states-for-resources)
    -   [Restrições de estado de recurso de leitura/gravação](#readwrite-resource-state-restrictions)
    -   [Estados de recurso para apresentar buffers de volta](#resource-states-for-presenting-back-buffers)
    -   [Descartando recursos](#discarding-resources)
-   [Transições de estado implícitas](#implicit-state-transitions)
    -   [Promoção de estado comum](#common-state-promotion)
    -   [Decaimento de estado para comum](#state-decay-to-common)
    -   [Implicações de desempenho](#performance-implications)
-   [Barreiras de divisão](#split-barriers)
-   [Cenário de exemplo de barreira de recursos](#resource-barrier-example-scenario)
-   [Exemplo comum de promoção de estado e decaimento](#common-state-promotion-and-decay-sample)
-   [Exemplo de barreiras de divisão](#example-of-split-barriers)
-   [Tópicos relacionados](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a>Usando a API ResourceBa fox para gerenciar o estado por recurso

O [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifica o driver de gráficos de situações em que o driver pode precisar sincronizar vários acessos à memória na qual um recurso está armazenado. O método é chamado com uma ou mais estruturas de descrição de barreira de recurso que indicam o tipo de barreira de recurso que está sendo declarado.

Há três tipos de barreiras de recursos:

-   **Barreira de transição** – uma barreira de transição indica que um conjunto de subrecursos faz a transição entre diferentes usos. Uma estrutura de [**barreira de \_ transição de recursos \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) é usada para especificar o subrecurso que está em transição, bem como os Estados de *antes* e *depois* do subrecurso.

    O sistema verifica se as transições de subrecurso em uma lista de comandos são consistentes com as transições anteriores na mesma lista de comandos. A camada de depuração rastreia ainda mais o estado do subrecurso para encontrar outros erros, no entanto, essa validação é conservadora e não exaustiva.

    Observe que você pode usar o \_ sinalizador D3D12 \_ de \_ todos os \_ subrecursos de barreira de recursos para especificar que todos os subrecursos em um recurso estão sendo transferidos.

-   **Barreira de alias** – uma barreira de alias indica uma transição entre os usos de dois recursos diferentes que têm mapeamentos sobrepostos no mesmo heap. Isso se aplica a recursos reservados e colocados. Uma estrutura de [**barreira de \_ alias de recursos \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) é usada para especificar o recurso *before* e o *After* .

    Observe que um ou ambos os recursos podem ser nulos, o que indica que qualquer recurso de ladrilho pode causar alias. Para obter mais informações sobre o uso de recursos em ladrilho, consulte recursos de [lado](../direct3d11/tiled-resources.md) e de [volume](volume-tiled-resources.md).

-   **Barreira de modo de exibição de acesso não ordenado (UAV)** -uma barreira UAV indica que todos os acessos de UAV, leitura ou gravação, a um recurso específico devem ser concluídos entre quaisquer acessos UAV futuros, leitura ou gravação. Não é necessário que um aplicativo coloque uma barreira de UAV entre duas chamadas de desenho ou expedição que somente leem de um UAV. Além disso, não é necessário colocar uma barreira de UAV entre duas chamadas de desenho ou expedição que são escritas no mesmo UAV se o aplicativo souber que é seguro executar o acesso UAV em qualquer ordem. Uma [**estrutura D3D12 \_ RESOURCE \_ UAV \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) é usada para especificar o recurso UAV ao qual a barreira se aplica. O aplicativo pode especificar NULL para o UAV da barreira, o que indica que qualquer acesso UAV pode exigir a barreira.

Quando [**ResourceBa array**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) é chamado com uma matriz de descrições de barreira de recursos, a API se comporta como se tivesse sido chamada uma vez para cada elemento, na ordem em que foram fornecidas.

A qualquer momento, uma sub-fonte está exatamente em um estado, determinado pelo conjunto de sinalizadores [**D3D12 \_ RESOURCE \_ STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) fornecidos para [**ResourceBa ltda.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) O aplicativo deve garantir que os *estados antes* e *depois* de chamadas consecutivas para **ResourceBarrier concordem.**

> [!TIP]
>
> Os aplicativos devem fazer várias transições em lote em uma chamada à API sempre que possível.

 

### <a name="resource-states"></a>Estados de recurso

Para ver a lista completa de estados de recurso entre os que um recurso pode fazer a transição, consulte o tópico de referência para a enumeração [**D3D12 \_ RESOURCE \_ STATES.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)

Para dividir as barreiras de recursos, consulte também [**D3D12 \_ RESOURCE \_ BARRIER \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).

### <a name="initial-states-for-resources"></a>Estados iniciais para recursos

Os recursos podem ser criados com qualquer estado inicial especificado pelo usuário (válido para a descrição do recurso), com as seguintes exceções:

-   O carregamento de heaps deve começar no estado D3D12 RESOURCE STATE GENERIC READ, que é uma combinação \_ OR bit a bit \_ \_ \_ de:
    -   VÉRTICE DE ESTADO DO RECURSO D3D12 \_ \_ E BUFFER \_ \_ \_ CONSTANTE \_
    -   D3D12 \_ RESOURCE \_ STATE \_ INDEX \_ BUFFER
    -   D3D12 \_ RESOURCE \_ STATE \_ COPY \_ SOURCE
    -   RECURSO D3D12 \_ RESOURCE STATE NON PIXEL \_ \_ \_ \_ \_ SHADER
    -   \_Recurso D3D12 \_ \_ \_ sombreador de pixel do estado do recurso \_
    -   \_ \_ \_ Argumento indireto de estado do recurso D3D12 \_
-   Os heaps readback devem começar no estado de \_ destino da cópia de estado do recurso D3D12 \_ \_ \_ .
-   Buffers de back de cadeia de permuta iniciam automaticamente \_ no \_ estado comum do estado do recurso D3D12 \_ .

Antes que um heap possa ser o destino de uma operação de cópia de GPU, normalmente o heap deve primeiro ser transferido para o \_ estado de destino da cópia de estado do recurso D3D12 \_ \_ \_ . No entanto, os recursos criados em heaps de carregamento devem começar no e não podem ser alterados a partir do \_ estado de leitura genérico, pois apenas a CPU estará escrevendo. Por outro lado, os recursos confirmados criados em heaps READBACK devem começar no e não podem mudar a partir do estado de destino da cópia \_ .

### <a name="readwrite-resource-state-restrictions"></a>Restrições de estado do recurso de leitura/gravação

Os bits de uso de estado do recurso que são usados para descrever um estado de recurso são divididos em Estados somente leitura e de leitura/gravação. O tópico de referência para [**os \_ \_ Estados de recurso D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indica o nível de acesso de leitura/gravação para cada bit na enumeração.

No máximo, apenas um bit de leitura/gravação pode ser definido para qualquer recurso. Se um bit de gravação for definido, nenhum bit somente leitura poderá ser definido para esse recurso. Se nenhum bit de gravação for definido, qualquer número de bits de leitura poderá ser definido.

### <a name="resource-states-for-presenting-back-buffers"></a>Estados de recursos para apresentar buffers de fundo

Antes de um buffer de fundo ser apresentado, ele deve estar no \_ estado comum do estado do recurso D3D12 \_ \_ . Observe que o estado do recurso D3D12 \_ Resource State \_ \_ presente é um sinônimo para o \_ estado do recurso D3D12 \_ \_ comum, e ambos têm um valor de 0. Se [**IDXGISwapChain::P reenviado**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (ou [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) for chamado em um recurso que não está atualmente nesse estado, um aviso de camada de depuração será emitido.

### <a name="discarding-resources"></a>Descartando recursos

Todas as sub-fontes em um recurso devem estar no estado RENDER TARGET ou no estado DEPTH WRITE para recursos de \_ \_ destino/profundidade/estêncil de renderização, respectivamente, quando [**ID3D12GraphicsCommandList::D iscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) é chamado.

## <a name="implicit-state-transitions"></a>Transições de estado implícitas

Os recursos só podem ser "promovidos" de D3D12 \_ RESOURCE \_ STATE \_ COMMON. Da mesma forma, os recursos só serão "decair" para D3D12 \_ RESOURCE \_ STATE \_ COMMON.

### <a name="common-state-promotion"></a>Promoção de estado comum

Todos os recursos de buffer, bem como texturas com o sinalizador D3D12 RESOURCE FLAG ALLOW SIMULTANEOUS ACCESS definido são promovidos implicitamente de \_ \_ \_ \_ \_ D3D12 RESOURCE STATE \_ COMMON \_ \_ \_ para o estado relevante no primeiro acesso à GPU, incluindo LEITURA GENÉRICA para abranger qualquer cenário de leitura. Qualquer recurso no estado COMMON pode ser acessado como por meio dele estava em um único estado com

<dl> 1 sinalizador WRITE ou  
1 ou mais sinalizadores READ  
</dl>

Os recursos podem ser promovidos do estado COMMON com base na tabela a seguir:



| Sinalizador de estado                    | Buffers e Simultaneous-Access texturas                             | Texturas sem acesso simultâneo                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| VÉRTICE \_ E \_ BUFFER \_ CONSTANTE | Sim                                          | Não                                   |
| BUFFER DE \_ ÍNDICE                 | Sim                                          | Não                                   |
| DESTINO \_ DE RENDERIZAÇÃO                | Sim                                          | Não                                   |
| ACESSO NÃO \_ ORGANIZADO             | Sim                                          | Não                                   |
| GRAVAÇÃO \_ DE PROFUNDIDADE                  | Não<sup>\*</sup>                              | Não                                   |
| LEITURA DE \_ PROFUNDIDADE                   | Não<sup>\*</sup>                              | Não                                   |
| \_recurso de \_ sombreador não pixel \_  | Sim                                          | Sim                                  |
| \_recurso sombreador de pixel \_       | Sim                                          | Sim                                  |
| saída de fluxo \_                   | Sim                                          | Não                                   |
| argumento indireto \_            | Sim                                          | Não                                   |
| COPIAR \_ dest                    | Sim                                          | Sim                                  |
| origem da cópia \_                  | Sim                                          | Sim                                  |
| RESOLVER \_ dest                 | Sim                                          | Não                                   |
| RESOLVER \_ origem               | Sim                                          | Não                                   |
| PREDICAÇÃO                   | Sim                                          | Não                                   |



 

<sup>\*</sup>Os recursos do estêncil de profundidade devem ser texturas de acesso não simultâneas e, portanto, nunca podem ser promovidas implicitamente.

Quando esse acesso ocorre, a promoção age como uma barreira de recursos implícita. Para os acessos subsequentes, as barreiras de recursos serão necessárias para alterar o estado do recurso, se necessário. Observe que a promoção de um estado de leitura promovido em vários Estados de leitura é válida, mas esse não é o caso para os Estados de gravação.  
Por exemplo, se um recurso no estado comum for promovido para recurso de \_ sombreador \_ de pixel em uma chamada de desenho, ele ainda poderá ser promovido para NON_PIXEL \_ recurso de sombreador \_ | \_ \_ Recurso de sombreador de pixel em outra chamada de desenho. No entanto, se ele for usado em uma operação de gravação, como um destino de cópia, uma barreira de transição de estado de recurso dos Estados de leitura promovidos combinados, aqui NON_PIXEL \_ recurso de sombreador \_ | O \_ \_ recurso de sombreador de pixel, para copiar \_ dest é necessário.  
Da mesma forma, se for promovido de COMMON para COPY \_ dest, uma barreira ainda será necessária para fazer a transição do dest de cópia \_ para o destino de renderização \_ .

Observe que a promoção de Estado comum é "gratuita", pois não há necessidade de a GPU executar qualquer espera de sincronização. A promoção representa o fato de que os recursos no estado comum não devem exigir acompanhamento de driver ou trabalho de GPU adicional para dar suporte a determinados acessos.

### <a name="state-decay-to-common"></a>Estado decaimento para comum

O outro lado da promoção de estado comum é decair de volta para D3D12 \_ RESOURCE \_ STATE \_ COMMON. Os recursos que atendem a determinados requisitos são considerados sem estado e retornam efetivamente ao estado comum quando a GPU termina a execução de [**uma operação ExecuteCommandLists.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) O decaimento não ocorre entre listas de comandos executadas juntas na mesma **chamada ExecuteCommandLists.**

Os seguintes recursos serão decair [**quando uma operação ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) for concluída na GPU:

-   Recursos que estão sendo acessados em uma fila de cópia *ou*
-   Recursos de buffer em qualquer tipo de fila *ou*
-   Recursos de textura em qualquer tipo de fila que tenha o sinalizador D3D12 \_ RESOURCE FLAG ALLOW SIMULTANEOUS ACCESS definido \_ \_ \_ \_ *ou*
-   Qualquer recurso promovido implicitamente para um estado somente leitura.

Assim como a promoção de estado comum, o decaimento é gratuito, já que nenhuma sincronização adicional é necessária. Combinar promoção de estado comum e decaimento pode ajudar a eliminar muitas transições [**desnecessárias do ResourceBa ltda.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) Em alguns casos, isso pode fornecer melhorias significativas de desempenho.

Buffers e Simultaneous-Access recursos serão decair para o estado comum, independentemente de eles ter sido explicitamente transições usando barreiras de recursos ou promovidos implicitamente.

### <a name="performance-implications"></a>Implicações de desempenho

Ao registrar transições explícitas de [**ResourceBastate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) em recursos no estado comum, é correto usar D3D12 RESOURCE STATE COMMON ou qualquer estado promovendo como o valor BeforeState na estrutura \_ \_ \_ D3D12 RESOURCE TRANSITION  \_ \_ \_ BARRIER. Isso permite o gerenciamento de estado tradicional que ignora o decaimento automático de buffers e texturas de acesso simultâneo. No entanto, isso pode não ser desejável, pois evitar chamadas de transição **do ResourceBa ltda** com recursos conhecidos por estar no estado comum pode melhorar significativamente o desempenho. As barreiras de recursos podem ser caras. Elas são projetadas para forçar liberações de cache, alterações de layout de memória e outras sincronizações que podem não ser necessárias para os recursos que já estão no estado comum. Uma lista de comandos que usa uma barreira de recurso de um estado não comum para outro Estado não comum em um recurso atualmente no estado comum pode introduzir muita sobrecarga desnecessária.

Além disso, evite transições [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explícitas \_ para \_ o estado do recurso D3D12 \_ comum, a menos que seja absolutamente necessário (por exemplo, o próximo acesso está em uma fila de comando de cópia que exige que os recursos comecem no estado comum). As transições excessivas para o estado comum podem reduzir drasticamente o desempenho da GPU.

Em resumo, tente contar com a promoção de Estado comum e decaimento sempre que sua semântica permitir que você saia sem emitir chamadas [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .

## <a name="split-barriers"></a>Barreiras de divisão

Uma barreira de transição de recurso com o sinalizador de barreira de D3D12 de \_ recursos \_ \_ \_ inicial \_ só começa uma barreira de divisão e a barreira de transição é considerada pendente. Embora a barreira esteja pendente, o recurso (sub) não pode ser lido ou gravado pela GPU. A única barreira de transição legal que pode ser aplicada a um recurso (sub) com uma barreira pendente é uma com o mesmo estado *anterior* e *posterior* e o \_ sinalizador de finalização do sinalizador de barreira de recursos D3D12 \_ \_ \_ \_ , que a barreira conclui a transição pendente.

As barreiras de divisão fornecem dicas para a GPU em que um recurso no estado *a* seguir será usado no estado *B* , em algum momento depois. Isso dá à GPU a opção de otimizar a carga de trabalho de transição, possivelmente reduzindo ou eliminando as vagas de execução. A emissão da barreira somente final garante que todo o trabalho de transição da GPU seja concluído antes de passar para o próximo comando.

O uso de barreiras de divisão pode ajudar a melhorar o desempenho, especialmente em cenários de vários mecanismos ou em que os recursos de leitura/gravação são transferidos de modo disperso em uma ou mais listas de comandos.

## <a name="resource-barrier-example-scenario"></a>Cenário de exemplo de barreira de recurso

Os snippets a seguir mostram o uso do [**método ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) em um exemplo de multi-threading.

Criando a exibição de estêncil de profundidade, fazendo a transição dela para um estado grave.


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



Criando a exibição de buffer de vértice, primeiro alterando-a de um estado comum para um destino e, em seguida, de um destino para um estado acessível genérico.


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



Criando a exibição de buffer de índice, primeiro alterando-a de um estado comum para um destino e, em seguida, de um destino para um estado acessível genérico.


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



Criando texturas e exibições de recursos de sombreador. A textura é alterada de um estado comum para um destino e, em seguida, de um destino para um recurso de sombreador de pixel.


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



Iniciando um quadro; isso não só usa [**ResourceBa widget para**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) indicar que o backbuffer deve ser usado como um destino de renderização, mas também inicializa o recurso de quadro (que chama **ResourceBa widget** no buffer de estêncil de profundidade).


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



Encerrando um quadro, indicando que o buffer de fundo agora é usado para apresentar.


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



Inicializar um recurso de quadro, chamado ao iniciar um quadro, faz a transição do buffer de estêncil de profundidade para write-able.


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



As barreiras são trocadas no meio do quadro, fazendo a transição do mapa de sombra de writeable para leitura.


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



Concluir é chamado quando um quadro é encerrado, fazendo a transição do mapa de sombra para um estado comum.


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a>Exemplo comum de promoção de estado e decaimento

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a>Exemplo de barreiras de divisão

O exemplo a seguir mostra como usar uma barreira de divisão para reduzir as paralisações de pipeline. O código a seguir não usa barreiras de divisão:

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

O código a seguir usa barreiras de divisão:

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a>Tópicos relacionados

[Tutoriais de vídeo de aprendizado avançado do DirectX: Barreiras de recursos e acompanhamento de estado](https://www.youtube.com/watch?v=nmB2XMasz2o)

[Sincronização de vários mecanismos](./user-mode-heap-synchronization.md)

[Envio de trabalho no Direct3D 12](command-queues-and-command-lists.md)

[Uma olhada dentro das barreiras de estado do recurso D3D12](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

