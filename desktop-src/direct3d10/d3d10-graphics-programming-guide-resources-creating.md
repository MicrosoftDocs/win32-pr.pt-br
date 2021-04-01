---
description: A criação de buffers requer a definição dos dados que o buffer armazenará, fornecendo dados de inicialização e configurando sinalizadores de uso e de associação apropriados. Para criar texturas, consulte criando recursos de textura (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Criando recursos de buffer (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646403"
---
# <a name="creating-buffer-resources-direct3d-10"></a>Criando recursos de buffer (Direct3D 10)

A criação de buffers requer a definição dos dados que o buffer armazenará, fornecendo dados de inicialização e configurando sinalizadores de uso e de associação apropriados. Para criar texturas, consulte [criando recursos de textura (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).

-   [Criar um buffer de vértice](#create-a-vertex-buffer)
    -   [Criar uma descrição do buffer](#create-a-buffer-description)
    -   [Criar os dados de inicialização para o buffer](#create-the-initialization-data-for-the-buffer)
    -   [Criar o buffer](#create-the-buffer)
-   [Criar um buffer de índice](#create-an-index-buffer)
-   [Criar um buffer de constantes](#create-a-constant-buffer)
-   [Tópicos relacionados](#related-topics)

## <a name="create-a-vertex-buffer"></a>Criar um buffer de vértice

As etapas para criar um [buffer de vértice](d3d10-graphics-programming-guide-resources-types.md) são as seguintes.

-   [Criar uma descrição do buffer](#create-a-buffer-description)
-   [Criar os dados de inicialização para o buffer](#create-the-initialization-data-for-the-buffer)
-   [Criar o buffer](#create-the-buffer)

### <a name="create-a-buffer-description"></a>Criar uma descrição do buffer

Ao criar um buffer de vértice, uma descrição de buffer (consulte [**\_ \_ desc buffer d3d10**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) é usada para definir como os dados são organizados dentro do buffer, como o pipeline pode acessar o buffer e como o buffer será usado.

O exemplo a seguir demonstra como criar uma descrição de buffer para um único triângulo com vértices que contêm valores de posição e cor.


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



Neste exemplo, a descrição do buffer é inicializada com quase todas as configurações padrão para [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**acesso à CPU**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) e [**sinalizadores diversos**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag). As outras configurações são para o [**sinalizador BIND**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) que identifica o recurso como um buffer de vértice apenas e o tamanho do buffer.

Os sinalizadores de acesso de uso e CPU são importantes para o desempenho. Juntos, esses dois sinalizadores determinam a frequência com que um recurso é acessado, em que tipo de memória o recurso pode ser carregado e qual processador precisa acessar o recurso. Uso padrão esse recurso não será atualizado com muita frequência. Definir o acesso à CPU como 0 significa que a CPU não precisará ler ou gravar o recurso. Em combinação, isso significa que o tempo de execução pode carregar o recurso na memória de desempenho mais alta para a GPU, já que o recurso não requer acesso à CPU.

Como esperado, há uma compensação entre o melhor desempenho e a acessibilidade de qualquer momento por um dos processadores. Por exemplo, o uso padrão sem acesso à CPU significa que o recurso pode ser disponibilizado para a GPU exclusivamente. Isso pode incluir o carregamento do recurso na memória não acessível diretamente pela CPU. O recurso só pode ser modificado com [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).

### <a name="create-the-initialization-data-for-the-buffer"></a>Criar os dados de inicialização para o buffer

Um buffer é apenas uma coleção de elementos e é apresentado como uma matriz 1D. Como resultado, a densidade de memória do sistema e a densidade da fatia da memória do sistema são as mesmas; o tamanho da declaração de dados de vértice. Um aplicativo pode fornecer dados de inicialização quando um buffer é criado usando uma [**Descrição de subrecurso**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), que contém um ponteiro para os dados do recurso real e contém informações sobre o tamanho e o layout desses dados.

Qualquer buffer criado com uso imutável (consulte [**d3d10 \_ Usage \_ imutável**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) deve ser inicializado no momento da criação. Os buffers que usam qualquer um dos outros sinalizadores de uso podem ser atualizados após a inicialização usando [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)e [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), ou acessando sua memória subjacente usando o método [**MAP**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) .

### <a name="create-the-buffer"></a>Criar o buffer

Usar a descrição do buffer e os dados de inicialização (que é opcional) chamar [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) para criar um buffer de vértice. O trecho de código a seguir demonstra como criar um buffer de vértice de uma matriz de dados de vértice declarada pelo aplicativo.


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a>Criar um buffer de índice

A criação de um buffer de índice é muito semelhante à criação de um buffer de vértice; com duas diferenças. Um buffer de índice contém apenas dados de 16 bits ou 32 bits (em vez da ampla gama de formatos disponíveis para um buffer de vértice. Um buffer de índice também requer um sinalizador de ligação de buffer de índice.

O exemplo a seguir demonstra como criar um buffer de índice de uma matriz de dados de índice.


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a>Criar um buffer de constantes

O Direct3D 10 introduz um buffer constante. Um buffer de constante, ou buffer de constante de sombreador, é um buffer que contém constantes de sombreador. Aqui está um exemplo de criação de um buffer constante, extraído do [exemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



Observe que, ao usar a interface de [**interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) , o processo de criação, associação e confirmação de um buffer constante é manipulado pela instância da **interface ID3D10Effect** . Nesse caso, só nescesary obter a variável do efeito com um dos métodos getvariance, como [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) , e atualizar a variável com um dos métodos SetVariable, como [**setmatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix). Para obter um exemplo de como usar a **interface ID3D10Effect** para gerenciar um buffer de constantes [, consulte Tutorial 7: mapeamento de textura e buffers de constantes](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



