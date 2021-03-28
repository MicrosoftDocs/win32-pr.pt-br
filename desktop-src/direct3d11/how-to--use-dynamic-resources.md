---
title: Como usar recursos dinâmicos
description: Você cria e usa recursos dinâmicos quando seu aplicativo precisa alterar os dados nesses recursos. Você pode criar texturas e buffers para uso dinâmico.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41e00cda7236040679c7863454e4cc18d81106b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159421"
---
# <a name="how-to-use-dynamic-resources"></a>Como: usar recursos dinâmicos

**APIs importantes**

-   [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [**ID3D11DeviceContext:: mapeamento**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [**Uso de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

Você cria e usa recursos dinâmicos quando seu aplicativo precisa alterar os dados nesses recursos. Você pode criar texturas e buffers para uso dinâmico.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Como: criar uma textura](overviews-direct3d-11-resources-textures-create.md)
-   [Como: inicializar uma textura programaticamente](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [Como: criar um buffer de constantes](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a>Pré-requisitos

Partimos do princípio de que você conhece C++. Você também precisa ter experiência básica com conceitos de programação de elementos gráficos.

## <a name="instructions"></a>Instruções

### <a name="step-1-specify-dynamic-usage"></a>Etapa 1: especificar o uso dinâmico

Se você quiser que seu aplicativo seja capaz de fazer alterações nos recursos, deverá especificar esses recursos como dinâmicos e graváveis ao criá-los.

**Para especificar o uso dinâmico**

1.  Especifique o uso do recurso como dinâmico. Por exemplo, especifique o [**valor \_ \_ dinâmico de uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) no membro de **uso** do [**buffer de D3D11 \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para um vértice ou um buffer de constante e especifique o valor **dinâmico de \_ uso \_ de D3D11** no membro de **uso** de [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) para uma textura 2D.
2.  Especifique o recurso como gravável. Por exemplo, especifique o valor de [**gravação de \_ acesso de CPU \_ \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) no membro **CPUAccessFlags** de [**D3D11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) ou [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).
3.  Passe a descrição do recurso para a função de criação. Por exemplo, passe o endereço do [**\_ buffer D3D11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) e passe o endereço de [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) para [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).

Aqui está um exemplo de criação de um buffer de vértice dinâmico:


```C++
    // Create a vertex buffer for a triangle.

    float2 triangleVertices[] =
    {
        float2(-0.5f, -0.5f),
        float2(0.0f, 0.5f),
        float2(0.5f, -0.5f),
    };

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(float2)* ARRAYSIZE(triangleVertices);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;
    vertexBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
    vertexBufferDesc.MiscFlags = 0;
    vertexBufferDesc.StructureByteStride = 0;

    D3D11_SUBRESOURCE_DATA vertexBufferData;
    vertexBufferData.pSysMem = triangleVertices;
    vertexBufferData.SysMemPitch = 0;
    vertexBufferData.SysMemSlicePitch = 0;

    DX::ThrowIfFailed(
        m_d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        &vertexBufferData,
        &vertexBuffer2
        )
        );

```



### <a name="step-2-change-a-dynamic-resource"></a>Etapa 2: alterar um recurso dinâmico

Se você especificou um recurso como dinâmico e gravável quando o criou, poderá fazer alterações posteriormente nesse recurso.

**Para alterar dados em um recurso dinâmico**

1.  Configure os novos dados para o recurso. Declare uma variável de tipo de [**\_ \_ subrecurso mapeado D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) e inicialize-a como zero. Você usará essa variável para alterar o recurso.
2.  Desabilite o acesso à GPU (unidade de processamento gráfico) aos dados que você deseja alterar e obtenha um ponteiro para a memória que contém os dados. Para obter esse ponteiro, passe [**D3D11 \_ map \_ Write \_ Discard**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) para o parâmetro *MapType* ao chamar [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map). Defina esse ponteiro para o endereço da variável [**de \_ \_ subrecurso mapeado D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) da etapa anterior.
3.  Grave os novos dados na memória.
4.  Chame [**ID3D11DeviceContext:: inmapeamento**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) para reabilitar o acesso de GPU aos dados quando terminar de gravar os novos dados.

Aqui está um exemplo de alteração de um buffer de vértice dinâmico:


```C++
// This might get called as the result of a click event to double the size of the triangle.
void TriangleRenderer::MapDoubleVertices()
{
    D3D11_MAPPED_SUBRESOURCE mappedResource;
    ZeroMemory(&mappedResource, sizeof(D3D11_MAPPED_SUBRESOURCE));
    float2 vertices[] =
    {
        float2(-1.0f, -1.0f),
        float2(0.0f, 1.0f),
        float2(1.0f, -1.0f),
    };
    //  Disable GPU access to the vertex buffer data.
    auto m_d3dContext = m_deviceResources->GetD3DDeviceContext();
    m_d3dContext->Map(vertexBuffer2.Get(), 0, D3D11_MAP_WRITE_DISCARD, 0, &mappedResource);
    //  Update the vertex buffer here.
    memcpy(mappedResource.pData, vertices, sizeof(vertices));
    //  Reenable GPU access to the vertex buffer data.
    m_d3dContext->Unmap(vertexBuffer2.Get(), 0);
}
```



## <a name="remarks"></a>Comentários

### <a name="using-dynamic-textures"></a>Usando texturas dinâmicas

É recomendável que você crie apenas uma textura dinâmica por formato e, possivelmente por tamanho. Não recomendamos a criação de mipmaps, cubos e volumes dinâmicos devido à sobrecarga adicional no mapeamento de cada nível. Para mipmaps, você pode especificar [**o \_ \_ \_ descarte de gravação do mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) somente no nível superior. Todos os níveis são descartados Mapeando apenas o nível superior. Esse comportamento é o mesmo para volumes e cubos. Para cubos, o nível superior e a face 0 são mapeados.

### <a name="using-dynamic-buffers"></a>Usando buffers dinâmicos

Quando você chama [**MAP**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) em um buffer de vértice estático enquanto a GPU está usando o buffer, você obtém uma penalidade de desempenho significativa. Nessa situação, o **mapa** deve aguardar até que a GPU termine de ler os dados de vértice ou de índice do buffer antes que o **mapa** possa retornar ao aplicativo de chamada, o que causa um atraso significativo. Chamar **MAP** e, em seguida, renderizar de um buffer estático várias vezes por quadro também impede a GPU de armazenar em buffer comandos de renderização porque ele deve concluir os comandos antes de retornar o ponteiro de mapa. Sem comandos armazenados em buffer, a GPU permanece ociosa até que o aplicativo termine de preencher o buffer de vértice ou o buffer de índice e emita um comando de renderização.

Idealmente, os dados de vértice ou de índice nunca seriam alterados, mas isso nem sempre é possível. Há muitas situações em que o aplicativo precisa alterar os dados do vértice ou do índice a cada quadro, talvez até várias vezes por quadro. Para essas situações, recomendamos que você crie o vértice ou o buffer de índice com o [**uso de D3D11 \_ \_ dinâmico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). Esse sinalizador de uso faz com que o tempo de execução Otimize para operações de mapeamento frequentes. **D3D11 \_ O uso \_ dinâmico** só é útil quando o buffer é mapeado com frequência; Se os dados permanecerem constantes, coloque-os em um buffer estático de um vértice ou de índice.

Para receber uma melhoria de desempenho quando você usa buffers de vértice dinâmicos, seu aplicativo deve chamar [**MAP**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) com os valores de [**\_ mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) apropriados. [**D3D11 \_ O \_ \_ descarte de gravação de mapa**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica que o aplicativo não precisa manter o vértice antigo ou os dados de índice no buffer. Se a GPU ainda estiver usando o buffer quando você chamar **MAP** com **\_ descarte de \_ gravação \_ de mapa D3D11**, o tempo de execução retornará um ponteiro para uma nova região de memória em vez dos dados de buffer antigos. Isso permite que a GPU continue usando os dados antigos enquanto o aplicativo coloca os dados no novo buffer. Nenhum gerenciamento de memória adicional é necessário no aplicativo; o buffer antigo é reutilizado ou destruído automaticamente quando a GPU é concluída com ele.

> [!Note]  
> Quando você mapeia um buffer com [**\_ descarte de \_ gravação \_ de mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), o tempo de execução sempre descarta todo o buffer. Não é possível preservar as informações em áreas não mapeadas do buffer especificando um campo de tamanho limitado ou um deslocamento diferente de zero.

 

Há casos em que a quantidade de dados que o aplicativo precisa armazenar por mapa é pequena, como adicionar quatro vértices para renderizar um Sprite. [**D3D11 \_ Gravação de mapeamento \_ \_ sem \_ substituição**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica que o aplicativo não substituirá os dados que já estão em uso no buffer dinâmico. A chamada de [**mapa**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) retornará um ponteiro para os dados antigos, o que permitirá que o aplicativo Adicione novos dados em regiões não utilizadas do vértice ou buffer de índice. O aplicativo não deve modificar vértices ou índices que são usados em uma operação de desenho, pois eles ainda podem estar em uso pela GPU. Recomendamos que o aplicativo use o [**\_ descarte de \_ gravação \_ do mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) depois que o buffer dinâmico estiver cheio para receber uma nova região de memória, o que descartará os dados antigos do vértice ou do índice depois que a GPU for concluída.

O mecanismo de consulta assíncrona é útil para determinar se os vértices ainda estão em uso pela GPU. Emita uma consulta do tipo [**\_ \_ evento de consulta D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) após a última chamada de desenho que usa os vértices. Os vértices não estão mais em uso quando [**ID3D11DeviceContext:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) retorna S \_ OK. Ao mapear um buffer com o [**D3D11 \_ map \_ Write \_ Discard**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) ou nenhum valor de mapa, você sempre garante que os vértices sejam sincronizados corretamente com a GPU. Mas, ao mapear sem valores de mapa, você incorrerá na penalidade de desempenho descrita anteriormente.

> [!Note]  
> O tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8, permite o mapeamento de buffers de constantes dinâmicas e SRVs (exibições de recursos do sombreador) de buffers dinâmicos com o [**mapa de D3D11 \_ \_ gravação \_ sem \_ substituição**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). Os tempos de execução do Direct3D 11 e anteriores não limitavam o mapeamento parcial da atualização para os buffers de vértice ou de índice. Para determinar se um dispositivo Direct3D dá suporte a esses recursos, chame [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) com [**Opções do D3D11 \_ Feature \_ D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature). **CheckFeatureSupport** preenche os membros de uma estrutura de [**Opções de D3D11 de \_ dados de recurso \_ \_ \_ D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) com os recursos do dispositivo. Os membros relevantes aqui são **MapNoOverwriteOnDynamicConstantBuffer** e **MapNoOverwriteOnDynamicBufferSRV**.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




