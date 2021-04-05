---
description: Para compor a tela ou executar operações de ponto flutuante, você precisa trabalhar no espaço de cores correto.
ms.assetid: 1DD8E2D3-430F-4EE4-9C41-78736C904920
title: Convertendo dados para o espaço de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b5dbec2f826c40d5274cbddb3b54d1cdd9f695
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645758"
---
# <a name="converting-data-for-the-color-space"></a>Convertendo dados para o espaço de cores

Para compor a tela ou executar operações de ponto flutuante, você precisa trabalhar no espaço de cores correto. Recomendamos que você execute operações de ponto flutuante em um espaço de cores linear. Em seguida, para apresentar suas imagens à tela, converta os dados em dados padrão RGB (sRGB, gama 2,2-corrigido) espaço de cores. A apresentação para a tela no espaço de cores sRGB é importante para precisão de cores. Se as imagens não forem corrigidas em gama 2,2, elas alocarão muitos bits ou muita largura de banda para destacar que as pessoas não podem diferenciar, e muito poucos, bits ou largura de banda para valores de sombra aos quais as pessoas são sensíveis e, portanto, exigiria mais bits ou largura de banda para manter a mesma qualidade visual. Portanto, para garantir a melhor precisão de cor, apresente as imagens na tela que são corrigidas em gama 2,2.

-   [Precisão da cor](#color-accuracy)
-   [Tópicos relacionados](#related-topics)

## <a name="color-accuracy"></a>Precisão da cor

Para apresentação, os formatos de exibição com valor inteiro (como o [**\_ formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**\_ formato dxgi \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)e assim por diante) sempre contêm dados corrigidos por gama de sRGB. Formatos de exibição com valor flutuante (atualmente, somente o [**\_ formato dxgi \_ R16G16B16A16 \_ float**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) contêm dados com valor linear.

O \_ [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB indica ao sistema operacional para ajudar o aplicativo a inserir dados sRGB na tela. O aplicativo sempre deve posicionar dados sRGB em buffers de fundo com formatos com valor inteiro para apresentar os dados sRGB à tela, mesmo que os dados não tenham esse modificador de formato em seu nome de formato. Para obter uma lista completa dos formatos de verificação de exibição:

-   [Suporte ao formato DXGI para hardware 12,1 de nível de recurso Direct3D](hardware-support-for-direct3d-12-1-formats.md)
-   [Suporte ao formato DXGI para hardware 12,0 de nível de recurso Direct3D](hardware-support-for-direct3d-12-0-formats.md)
-   [Suporte ao formato DXGI para hardware 11,1 de nível de recurso Direct3D](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Suporte ao formato DXGI para hardware 11,0 de nível de recurso Direct3D](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Suporte de hardware para formatos Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Suporte de hardware para formatos Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
-   [Suporte de hardware para formatos Direct3D 10](/previous-versions//cc627090(v=vs.85))

Quando você grava valores de saída de ponto flutuante do sombreador de pixel em exibições de destino de renderização (**RenderTargetView** s) com o \_ [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB que estão associados ao [pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline), você os converte para o espaço de cores de gama 2,2 corrigido. Da mesma forma, quando os modos de exibição de recurso de sombreador (**ShaderResourceView** s) com o \_ modificador de formato sRGB estiverem associados ao pipeline, você converterá os valores de espaço de cor de gama 2,2 para o espaço de cores linear ao lê-los de **ShaderResourceView** s. O sombreador pode, então, executar operações neles.

Por exemplo, use um código semelhante a este para gravar valores de saída de ponto flutuante de um sombreador em um formato **RenderTargetView** :


```
struct PSOut
{
    float4 color : SV_Target;
};

PSOut S( PSIn input )
{
    PSOut output;
    output.color = float4( 1.0, 0.0, 0.0, 1.0 );
    return output;
}
```



Quando a rotina ' s retorna, os valores de ponto flutuante (1, 0, 0, 1) são convertidos no formato **RenderTargetView** . Em seguida, se você atribuir \_ o [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB ao **RenderTargetView**, a conversão gama ocorrerá.

Estas são as etapas a serem seguidas para garantir que o conteúdo exibido na tela tenha a melhor precisão de cor.

**Para garantir a precisão da cor no pipeline**

1.  Se uma textura tiver conteúdo sRGB, verifique se o **ShaderResourceView** tem \_ o [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB para que, ao ler o **ShaderResourceView** no sombreador, você converta o conteúdo da textura do espaço de cores do gama 2,2 para o espaço de cores linear.
2.  Verifique se o **RenderTargetView** também tem \_ o [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB para que os valores de saída do sombreador sejam convertidos em gama.

Se você seguir as etapas anteriores, ao chamar o método [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) , o conteúdo exibido na tela terá a melhor precisão de cor.

Você pode usar o método [**ID3D11Device:: CreateRenderTargetView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) para criar exibições **\_ \_ \* \_ sRGB do formato dxgi** em buffers de fundo de uma cadeia de permuta que você cria somente com um formato **\_ \_ \* \_ UNORM de formato dxgi** . Essa é uma exceção especial para a regra para criar exibições de destino de renderização, que declara que você pode usar um formato diferente com **ID3D11Device:: CreateRenderTargetView** somente se você criou o recurso que deseja exibir com **o \_ formato dxgi sem \_ \* \_ tipo**.

Para obter mais informações sobre regras para converter dados, consulte [regras de conversão de dados](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion).

Para obter informações sobre como ler e gravar em uma textura simultaneamente, consulte [desempacotando e empacotando o \_ formato dxgi para a edição de imagem In-Place](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprimorando a apresentação com o modelo de flip, retângulos sujos e áreas roladas](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
