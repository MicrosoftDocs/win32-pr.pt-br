---
title: Como usar recursos dinâmicos
description: Você cria e usa recursos dinâmicos quando seu aplicativo precisa alterar dados nesses recursos. Você pode criar texturas e buffers para uso dinâmico.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d85933490d1e3bbbd09cc83720651c4fd634012f8e5aa70562396e87c096ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633096"
---
# <a name="how-to-use-dynamic-resources"></a>Como usar recursos dinâmicos

**APIs importantes**

-   [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [**USO DE D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

Você cria e usa recursos dinâmicos quando seu aplicativo precisa alterar dados nesses recursos. Você pode criar texturas e buffers para uso dinâmico.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Como criar uma textura](overviews-direct3d-11-resources-textures-create.md)
-   [Como inicializar uma textura programaticamente](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [Como criar um buffer constante](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a>Pré-requisitos

Partimos do princípio de que você conhece C++. Você também precisa ter experiência básica com conceitos de programação de elementos gráficos.

## <a name="instructions"></a>Instruções

### <a name="step-1-specify-dynamic-usage"></a>Etapa 1: Especificar o uso dinâmico

Se você quiser que seu aplicativo seja capaz de fazer alterações nos recursos, especifique esses recursos como dinâmicos e que podem ser escritos quando os criar.

**Para especificar o uso dinâmico**

1.  Especifique o uso do recurso como dinâmico. Por exemplo, especifique o valor DINÂMICO  de [**USO D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) no membro Uso de [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para  um vértice ou buffer constante e especifique o valor DINÂMICO de USO **D3D11 \_ \_** no membro Uso de [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) para uma textura 2D.
2.  Especifique o recurso como que pode ser escrito. Por exemplo, especifique o [**valor D3D11 \_ CPU ACCESS \_ \_ WRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) no membro **CPUAccessFlags** de [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) ou [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).
3.  Passe a descrição do recurso para a função de criação. Por exemplo, passe o endereço de [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) e passe o endereço [**de D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) para [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).

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



### <a name="step-2-change-a-dynamic-resource"></a>Etapa 2: Alterar um recurso dinâmico

Se você especificou um recurso como dinâmico e que pode ser escrito quando o criou, poderá fazer alterações posteriormente nesse recurso.

**Para alterar dados em um recurso dinâmico**

1.  Configurar os novos dados para o recurso. Declare uma [**variável de tipo D3D11 \_ \_ MAPPED SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) e inicialize-a como zero. Você usará essa variável para alterar o recurso.
2.  Desabilite o acesso à GPU (unidade de processamento de gráficos) aos dados que você deseja alterar e obter um ponteiro para a memória que contém os dados. Para obter esse ponteiro, passe [**D3D11 \_ MAP WRITE DISCARD \_ \_ para**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) o parâmetro *MapType* ao chamar [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map). De definir esse ponteiro para o endereço da [**variável D3D11 \_ \_ MAPPED SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) da etapa anterior.
3.  Escreva os novos dados na memória.
4.  Chame [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) para reaquecer o acesso à GPU aos dados quando terminar de escrever os novos dados.

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

Recomendamos que você crie apenas uma textura dinâmica por formato e, possivelmente, por tamanho. Não recomendamos criar mipmaps dinâmicos, cubos e volumes devido à sobrecarga adicional no mapeamento de todos os níveis. Para mipmaps, você pode especificar [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) somente no nível superior. Todos os níveis são descartados mapeando apenas o nível superior. Esse comportamento é o mesmo para volumes e cubos. Para cubos, os níveis superior e face 0 são mapeados.

### <a name="using-dynamic-buffers"></a>Usando buffers dinâmicos

Quando você chama [**Map em**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) um buffer de vértice estático enquanto a GPU está usando o buffer, você tem uma penalidade de desempenho significativa. Nessa situação, o **Mapa** deve aguardar até que a GPU termine de ler os dados de vértice ou índice do buffer antes que o **Mapa** possa retornar ao aplicativo de chamada, o que causa um atraso significativo. Chamar **Mapa** e, em seguida, renderizar de um buffer estático várias vezes por quadro também impede que a GPU em buffer de comandos de renderização porque ele deve concluir comandos antes de retornar o ponteiro do mapa. Sem comandos em buffer, a GPU permanece ociosa até que o aplicativo termine de preencher o buffer de vértice ou buffer de índice e emite um comando de renderização.

O ideal é que os dados de vértice ou índice nunca mudem, mas isso nem sempre é possível. Há muitas situações em que o aplicativo precisa alterar dados de vértice ou índice a cada quadro, talvez até várias vezes por quadro. Para essas situações, recomendamos que você crie o vértice ou buffer de índice com [**D3D11 \_ USAGE \_ DYNAMIC.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) Esse sinalizador de uso faz com que o runtime otimize para operações de mapa frequentes. **D3D11 \_ USAGE \_ DYNAMIC** só é útil quando o buffer é mapeado com frequência; Se os dados permanecerem constantes, coloque esses dados em um vértice estático ou buffer de índice.

Para receber uma melhoria de desempenho ao usar buffers de vértice dinâmicos, seu aplicativo deve chamar [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) com os valores apropriados [**de \_ MAP D3D11.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica que o aplicativo não precisa manter os dados antigos de vértice ou índice no buffer. Se a GPU ainda estiver usando o buffer quando você chamar **Map** com **D3D11 \_ MAP WRITE \_ \_ DISCARD**, o runtime retornará um ponteiro para uma nova região de memória em vez dos dados de buffer antigos. Isso permite que a GPU continue usando os dados antigos enquanto o aplicativo coloca os dados no novo buffer. Nenhum gerenciamento de memória adicional é necessário no aplicativo; o buffer antigo é reutilizado ou destruído automaticamente quando a GPU é concluída com ele.

> [!Note]  
> Quando você mapeia um buffer [**com D3D11 \_ MAP WRITE \_ \_ DISCARD,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)o runtime sempre descarta todo o buffer. Não é possível preservar informações em áreas não mapeadas do buffer especificando um campo de deslocamento não zero ou tamanho limitado.

 

Há casos em que a quantidade de dados que o aplicativo precisa armazenar por mapa é pequena, como adicionar quatro vértices para renderizar um sprite. [**D3D11 \_ MAP \_ WRITE \_ NO \_ OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica que o aplicativo não substituirá os dados já em uso no buffer dinâmico. A [**chamada**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) Mapa retornará um ponteiro para os dados antigos, o que permitirá que o aplicativo adicione novos dados em regiões nãoutiladas do vértice ou buffer de índice. O aplicativo não deve modificar vértices ou índices usados em uma operação de desenho, pois eles ainda podem estar em uso pela GPU. Recomendamos que o aplicativo use [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) depois que o buffer dinâmico ficar cheio para receber uma nova região de memória, o que descarta os dados antigos de vértice ou índice após a gpu ser concluída.

O mecanismo de consulta assíncrona é útil para determinar se os vértices ainda estão em uso pela GPU. Emita uma consulta do tipo [**D3D11 \_ QUERY \_ EVENT após**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) a última chamada de desenho que usa os vértices. Os vértices não estão mais em uso [**quando ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) retorna S \_ OK. Ao mapear um buffer com [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) ou sem valores de mapa, você sempre tem a garantia de que os vértices estão sincronizados corretamente com a GPU. Mas, quando você mapear sem valores de mapa, incorrerá na penalidade de desempenho descrita anteriormente.

> [!Note]  
> O runtime do Direct3D 11.1, que está disponível a partir do Windows 8, permite mapear buffers constantes dinâmicos e SRVs (exibições de recursos de sombreador) de buffers dinâmicos com [**D3D11 \_ MAP WRITE NO \_ \_ \_ OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). O Direct3D 11 e runtimes anteriores limitaram o mapeamento de atualização parcial sem sobrescrever para buffers de vértice ou índice. Para determinar se um dispositivo Direct3D dá suporte a esses recursos, chame [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) com [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature). **CheckFeatureSupport** preenche os membros de uma estrutura [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) com os recursos do dispositivo. Os membros relevantes aqui **são MapNoOverwriteOnDynamicConstantBuffer** e **MapNoOverwriteOnDynamicBufferSRV.**

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




