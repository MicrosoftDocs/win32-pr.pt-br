---
description: Um recurso de textura é uma coleção estruturada de dados.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Criando recursos de textura (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920399"
---
# <a name="creating-texture-resources-direct3d-10"></a>Criando recursos de textura (Direct3D 10)

Um recurso de [textura](d3d10-graphics-programming-guide-resources-types.md) é uma coleção estruturada de dados. Normalmente, os valores de cor são armazenados em texturas e acessados durante a renderização pelo [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) em vários estágios para entrada e saída. Criar texturas e definir como elas serão usadas é uma parte importante da renderização de cenas de aparência interessante no Direct3D 10.

Embora as texturas normalmente contenham informações de cor, a criação de texturas usando o [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) diferente permite que eles armazenem diferentes tipos de dados. Esses dados podem então ser aproveitados pelo pipeline do Direct3D 10 de maneiras não tradicionais.

Todas as texturas têm limites quanto à quantidade de memória consumida e quantas texels elas contêm. Esses limites são especificados pelas [constantes de recurso](d3d10-graphics-reference-resource-constants.md).

-   [Criar uma textura de um arquivo](#create-a-texture-from-a-file)
    -   [Criar textura e exibir separadamente](#create-texture-and-view-separately)
    -   [Criar textura e exibição simultaneamente](#create-texture-and-view-simultaneously)
-   [Criando texturas vazias](#creating-empty-textures)
    -   [Renderizando para uma textura](#rendering-to-a-texture)
    -   [Preenchendo texturas manualmente](#filling-textures-manually)
-   [Vários Rendertargets](#multiple-rendertargets)
-   [Tópicos relacionados](#related-topics)

## <a name="create-a-texture-from-a-file"></a>Criar uma textura de um arquivo

> [!Note]  
> A [biblioteca do utilitário D3DX](d3d10-graphics-reference-d3dx10.md) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Quando você cria uma textura no Direct3D 10, também precisa criar uma [exibição](d3d10-graphics-programming-guide-resources-access-views.md). Uma exibição é um objeto que informa ao dispositivo como uma textura deve ser acessada durante a renderização. A maneira mais comum de acessar uma textura é ler usando um [sombreador](../direct3dhlsl/dx-graphics-hlsl.md). Uma exibição de recurso de sombreador informará um sombreador como ler de uma textura durante a renderização. O tipo de exibição que uma textura usará deve ser especificado quando você criá-la.

Criar uma textura e carregar seus dados iniciais pode ser feito de duas maneiras diferentes: criar uma textura e uma exibição separadamente ou criar a textura e a exibição ao mesmo tempo. A API fornece as duas técnicas para que você possa escolher quais são as mais adequados às suas necessidades.

### <a name="create-texture-and-view-separately"></a>Criar textura e exibir separadamente

A maneira mais fácil de criar uma textura é carregá-la de um arquivo de imagem. Para criar a textura, basta preencher uma estrutura e fornecer o nome da textura para [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



A função D3DX [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) faz três coisas: primeiro, ela cria um objeto de textura Direct3D 10; em segundo lugar, ele lê o arquivo de imagem de entrada; em terceiro lugar, ele armazena os dados da imagem no objeto de textura. No exemplo acima, um arquivo BMP é carregado, mas a função pode carregar uma variedade de tipos de arquivo.

O sinalizador BIND indica que a textura será criada como um recurso de sombreador que permite que um estágio de sombreador Leia a partir da textura durante a renderização.

O exemplo acima não especifica todos os parâmetros de carregamento. Na verdade, geralmente é benéfico simplesmente zerar os parâmetros de carregamento, pois isso permite que o D3DX escolha os valores apropriados com base na imagem de entrada. Se você quiser que a imagem de entrada determine todos os parâmetros com os quais a textura é criada, basta especificar **NULL** para o parâmetro **loadinfo** da seguinte maneira:


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



A especificação de **NULL** para as informações de carregamento é um atalho simples, mas poderoso.

Agora que uma textura foi criada, você precisa criar uma exibição de recurso de sombreador para que a textura possa ser associada como uma entrada a um sombreador. Como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) retorna um ponteiro para um recurso e não um ponteiro para uma textura, você precisa determinar o tipo exato de recurso que foi carregado e, em seguida, pode criar uma exibição de recurso de sombreador usando [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



Embora o exemplo acima crie uma exibição de recurso de sombreador 2D, o código para criar outros tipos de modo de exibição de recurso de sombreador é muito semelhante. Qualquer estágio do sombreador agora pode usar essa textura como uma entrada.

Usar [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) para criar uma textura e sua exibição associada é uma maneira de preparar uma textura para ser associada a um estágio do sombreador. Outra maneira de fazer isso é criar a textura e sua exibição ao mesmo tempo, que é abordado na próxima seção.

### <a name="create-texture-and-view-simultaneously"></a>Criar textura e exibição simultaneamente

O Direct3D 10 exige uma textura e uma exibição de recurso de sombreador para ler de uma textura durante o tempo de execução. Como a criação de uma textura e uma exibição de recurso de sombreador é uma tarefa comum, o D3DX fornece o [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) para fazer isso por você.


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



Com uma única chamada D3DX, o modo de exibição de recurso textura e sombreador são criados. A funcionalidade do parâmetro **loadinfo** é inalterada; Você pode usá-lo para personalizar como a textura é criada ou derivar os parâmetros necessários do arquivo de entrada, especificando **NULL** para o parâmetro **loadinfo** .

O objeto [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) retornado pela função [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) pode ser usado posteriormente para recuperar a interface [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) original, se necessário. Isso pode ser feito chamando o método [**getResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) .

O D3DX fornece uma única função para criar uma textura e uma exibição de recurso de sombreador como um convienience; cabe a você decidir qual método de criação de uma textura e exibição é mais adequado às necessidades do seu aplicativo.

Agora que você sabe como criar uma textura e sua exibição de recurso de sombreador, a próxima seção mostrará como você pode fazer amostragem (leitura) dessa textura usando um sombreador.

## <a name="creating-empty-textures"></a>Criando texturas vazias

Às vezes, os aplicativos desejarão criar uma textura e computar os dados a serem armazenados na textura ou usar o [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) de gráficos para renderizar para essa textura e, posteriormente, usar os resultados em outro processamento. Essas texturas podem ser atualizadas pelo pipeline de gráficos ou pelo próprio aplicativo, dependendo do tipo de [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) especificado para a textura quando ela foi criada.

### <a name="rendering-to-a-texture"></a>Renderizando para uma textura

O caso mais comum de criar uma textura vazia para ser preenchida com dados durante o tempo de execução é o caso em que um aplicativo deseja renderizar para uma textura e, em seguida, usar os resultados da operação de renderização em uma passagem subsequente. As texturas criadas com essa finalidade devem especificar o [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)padrão.

O exemplo de código a seguir cria uma textura vazia que o pipeline pode processar e, subsequentemente, usar como uma entrada para um [sombreador](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



A criação da textura exige que o aplicativo especifique algumas informações sobre as propriedades que a textura terá. A largura e a altura da textura em texels são definidas como 256. Para esse destino de renderização, um único nível de mipmap é tudo o que precisamos. Somente um destino de renderização é necessário para que o tamanho da matriz seja definido como 1. Cada Texel contém valores de ponto flutuante de 4 32 bits, que podem ser usados para armazenar informações muito precisas (consulte o [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). Um exemplo por pixel é tudo o que será necessário. O uso é definido como padrão, pois isso permite o posicionamento mais eficiente do destino de renderização na memória. Por fim, o fato de que a textura será associada como um destino de renderização e um recurso de sombreador em diferentes pontos no tempo é especificado.

As texturas não podem ser associadas diretamente para renderização no pipeline; Use uma exibição de destino de renderização, conforme mostrado no exemplo de código a seguir.


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



O formato da exibição de destino de renderização é simplesmente definido como o formato da textura original. As informações no recurso devem ser interpretadas como uma textura 2D e só queremos usar o primeiro nível de mipmap do destino de renderização.

Da mesma forma como uma exibição de destino de renderização deve ser criada para que o destino de renderização possa ser associado à saída para o pipeline, um modo de exibição de recurso de sombreador deve ser criado para que o destino de renderização possa ser associado ao pipeline como uma entrada. O exemplo de código a seguir demonstra isso.


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



Os parâmetros de sombreador – descrições de modo de exibição de recursos são muito semelhantes aos das descrições de exibição de destino de renderização e foram escolhidos pelos mesmos motivos.

### <a name="filling-textures-manually"></a>Preenchendo texturas manualmente

Às vezes, os aplicativos gostariam de calcular valores em tempo de execução, colocá-los em uma textura manualmente e, em seguida, fazer com que o [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) de gráficos Use essa textura em operações de renderização posteriores. Para fazer isso, o aplicativo deve criar uma textura vazia de forma a permitir que a CPU acesse a memória subjacente. Isso é feito criando uma textura dinâmica e obtendo acesso à memória subjacente chamando um método específico. O exemplo de código a seguir demonstra como fazer isso.


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



Observe que o formato é definido como um 32 bits por pixel, em que cada componente é definido por 8 bits. O parâmetro Usage é definido como dinâmico, enquanto os sinalizadores de associação são definidos para especificar que a textura será acessada por um sombreador. O restante da descrição da textura é semelhante à criação de um destino de renderização.

O [**mapa**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) de chamada permite que o aplicativo acesse a memória subjacente da textura. O ponteiro recuperado é usado para preencher a textura com dados. Isso pode ser visto no exemplo de código a seguir.


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a>Vários Rendertargets

Até oito exibições de destino de renderização podem ser associadas ao pipeline de cada vez (com [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)). Para cada pixel (ou cada amostra se a multiamostragem estiver habilitada), a mesclagem é feita de forma independente para cada exibição de destino de renderização. Duas das variáveis de estado de mistura-BlendEnable e RenderTargetWriteMask-são matrizes de oito, cada membro de matriz corresponde a uma exibição de destino de renderização. Ao usar vários destinos de renderização, cada destino de renderização deve ser o mesmo [tipo de recurso](d3d10-graphics-programming-guide-resources-types.md) (buffer, textura 1D, matriz de textura 2D etc.) e deve ter a mesma dimensão (largura, altura, profundidade para texturas 3D e tamanho da matriz para matrizes de textura). Se os destinos de renderização forem de várias amostras, eles deverão ter o mesmo número de amostras por pixel.

Pode haver apenas um buffer de estêncil de profundidade ativo, independentemente de quantos destinos de renderização estão ativos. Ao usar matrizes de textura como destinos de renderização, todas as dimensões de exibição devem corresponder. Os destinos de renderização não precisam ter o mesmo formato de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
