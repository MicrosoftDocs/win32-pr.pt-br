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
# <a name="converting-data-for-the-color-space"></a><span data-ttu-id="b6872-103">Convertendo dados para o espaço de cores</span><span class="sxs-lookup"><span data-stu-id="b6872-103">Converting data for the color space</span></span>

<span data-ttu-id="b6872-104">Para compor a tela ou executar operações de ponto flutuante, você precisa trabalhar no espaço de cores correto.</span><span class="sxs-lookup"><span data-stu-id="b6872-104">To compose to the screen or perform floating-point operations, you need to work in the correct color space.</span></span> <span data-ttu-id="b6872-105">Recomendamos que você execute operações de ponto flutuante em um espaço de cores linear.</span><span class="sxs-lookup"><span data-stu-id="b6872-105">We recommend that you perform floating point operations in a linear color space.</span></span> <span data-ttu-id="b6872-106">Em seguida, para apresentar suas imagens à tela, converta os dados em dados padrão RGB (sRGB, gama 2,2-corrigido) espaço de cores.</span><span class="sxs-lookup"><span data-stu-id="b6872-106">Then, to present your images to the screen, convert the data to standard RGB data (sRGB, gamma 2.2-corrected) color space.</span></span> <span data-ttu-id="b6872-107">A apresentação para a tela no espaço de cores sRGB é importante para precisão de cores.</span><span class="sxs-lookup"><span data-stu-id="b6872-107">Presenting to the screen in sRGB color space is important for color accuracy.</span></span> <span data-ttu-id="b6872-108">Se as imagens não forem corrigidas em gama 2,2, elas alocarão muitos bits ou muita largura de banda para destacar que as pessoas não podem diferenciar, e muito poucos, bits ou largura de banda para valores de sombra aos quais as pessoas são sensíveis e, portanto, exigiria mais bits ou largura de banda para manter a mesma qualidade visual.</span><span class="sxs-lookup"><span data-stu-id="b6872-108">If images are not gamma 2.2-corrected, they allocate too many bits or too much bandwidth to highlights that people can't differentiate, and too few bits or bandwidth to shadow values that people are sensitive to, and so would require more bits or bandwidth to maintain the same visual quality.</span></span> <span data-ttu-id="b6872-109">Portanto, para garantir a melhor precisão de cor, apresente as imagens na tela que são corrigidas em gama 2,2.</span><span class="sxs-lookup"><span data-stu-id="b6872-109">Therefore, to ensure the best color accuracy, present images to the screen that are gamma 2.2-corrected.</span></span>

-   [<span data-ttu-id="b6872-110">Precisão da cor</span><span class="sxs-lookup"><span data-stu-id="b6872-110">Color accuracy</span></span>](#color-accuracy)
-   [<span data-ttu-id="b6872-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6872-111">Related topics</span></span>](#related-topics)

## <a name="color-accuracy"></a><span data-ttu-id="b6872-112">Precisão da cor</span><span class="sxs-lookup"><span data-stu-id="b6872-112">Color accuracy</span></span>

<span data-ttu-id="b6872-113">Para apresentação, os formatos de exibição com valor inteiro (como o [**\_ formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**\_ formato dxgi \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)e assim por diante) sempre contêm dados corrigidos por gama de sRGB.</span><span class="sxs-lookup"><span data-stu-id="b6872-113">For presentation, integer-valued display formats (such as [**DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI\_FORMAT\_R10G10B10\_XR\_BIAS\_A2\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), and so on) always contain sRGB gamma-corrected data.</span></span> <span data-ttu-id="b6872-114">Formatos de exibição com valor flutuante (atualmente, somente o [**\_ formato dxgi \_ R16G16B16A16 \_ float**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) contêm dados com valor linear.</span><span class="sxs-lookup"><span data-stu-id="b6872-114">Float-valued display formats (currently only [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) contain linear-valued data.</span></span>

<span data-ttu-id="b6872-115">O \_ [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB indica ao sistema operacional para ajudar o aplicativo a inserir dados sRGB na tela.</span><span class="sxs-lookup"><span data-stu-id="b6872-115">The \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) indicates to the operating system to help the app place sRGB data on the screen.</span></span> <span data-ttu-id="b6872-116">O aplicativo sempre deve posicionar dados sRGB em buffers de fundo com formatos com valor inteiro para apresentar os dados sRGB à tela, mesmo que os dados não tenham esse modificador de formato em seu nome de formato.</span><span class="sxs-lookup"><span data-stu-id="b6872-116">The app must always place sRGB data into back buffers with integer-valued formats to present the sRGB data to the screen, even if the data doesn't have this format modifier in its format name.</span></span> <span data-ttu-id="b6872-117">Para obter uma lista completa dos formatos de verificação de exibição:</span><span class="sxs-lookup"><span data-stu-id="b6872-117">For a complete list of display scan-out formats:</span></span>

-   [<span data-ttu-id="b6872-118">Suporte ao formato DXGI para hardware 12,1 de nível de recurso Direct3D</span><span class="sxs-lookup"><span data-stu-id="b6872-118">DXGI Format Support for Direct3D Feature Level 12.1 Hardware</span></span>](hardware-support-for-direct3d-12-1-formats.md)
-   [<span data-ttu-id="b6872-119">Suporte ao formato DXGI para hardware 12,0 de nível de recurso Direct3D</span><span class="sxs-lookup"><span data-stu-id="b6872-119">DXGI Format Support for Direct3D Feature Level 12.0 Hardware</span></span>](hardware-support-for-direct3d-12-0-formats.md)
-   [<span data-ttu-id="b6872-120">Suporte ao formato DXGI para hardware 11,1 de nível de recurso Direct3D</span><span class="sxs-lookup"><span data-stu-id="b6872-120">DXGI Format Support for Direct3D Feature Level 11.1 Hardware</span></span>](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [<span data-ttu-id="b6872-121">Suporte ao formato DXGI para hardware 11,0 de nível de recurso Direct3D</span><span class="sxs-lookup"><span data-stu-id="b6872-121">DXGI Format Support for Direct3D Feature Level 11.0 Hardware</span></span>](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   <span data-ttu-id="b6872-122">[Suporte de hardware para formatos Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6872-122">[Hardware Support for Direct3D 10Level9 Formats](/previous-versions//ff471324(v=vs.85))</span></span>
-   <span data-ttu-id="b6872-123">[Suporte de hardware para formatos Direct3D 10,1](/previous-versions//cc627091(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6872-123">[Hardware Support for Direct3D 10.1 Formats](/previous-versions//cc627091(v=vs.85))</span></span>
-   <span data-ttu-id="b6872-124">[Suporte de hardware para formatos Direct3D 10](/previous-versions//cc627090(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6872-124">[Hardware Support for Direct3D 10 Formats](/previous-versions//cc627090(v=vs.85))</span></span>

<span data-ttu-id="b6872-125">Quando você grava valores de saída de ponto flutuante do sombreador de pixel em exibições de destino de renderização (**RenderTargetView** s) com o \_ [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB que estão associados ao [pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline), você os converte para o espaço de cores de gama 2,2 corrigido.</span><span class="sxs-lookup"><span data-stu-id="b6872-125">When you write floating-point output values from the pixel shader into render-target views (**RenderTargetView** s) with the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) that are bound to the [pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline), you convert them to gamma 2.2-corrected color space.</span></span> <span data-ttu-id="b6872-126">Da mesma forma, quando os modos de exibição de recurso de sombreador (**ShaderResourceView** s) com o \_ modificador de formato sRGB estiverem associados ao pipeline, você converterá os valores de espaço de cor de gama 2,2 para o espaço de cores linear ao lê-los de **ShaderResourceView** s.</span><span class="sxs-lookup"><span data-stu-id="b6872-126">Similarly, when shader-resource views (**ShaderResourceView** s) with the \_SRGB format modifier are bound to the pipeline, you convert the values from gamma 2.2-corrected color space to linear color space when you read them from the **ShaderResourceView** s.</span></span> <span data-ttu-id="b6872-127">O sombreador pode, então, executar operações neles.</span><span class="sxs-lookup"><span data-stu-id="b6872-127">The shader can then perform operations on them.</span></span>

<span data-ttu-id="b6872-128">Por exemplo, use um código semelhante a este para gravar valores de saída de ponto flutuante de um sombreador em um formato **RenderTargetView** :</span><span class="sxs-lookup"><span data-stu-id="b6872-128">For example, use code similar to this to write floating-point output values from a shader into a **RenderTargetView** format:</span></span>


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



<span data-ttu-id="b6872-129">Quando a rotina ' s retorna, os valores de ponto flutuante (1, 0, 0, 1) são convertidos no formato **RenderTargetView** .</span><span class="sxs-lookup"><span data-stu-id="b6872-129">When the 'S' routine returns, the floating point (1, 0, 0, 1) values are converted to the **RenderTargetView** format.</span></span> <span data-ttu-id="b6872-130">Em seguida, se você atribuir \_ o [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB ao **RenderTargetView**, a conversão gama ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="b6872-130">Then, if you assign the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) to the **RenderTargetView**, the gamma conversion occurs.</span></span>

<span data-ttu-id="b6872-131">Estas são as etapas a serem seguidas para garantir que o conteúdo exibido na tela tenha a melhor precisão de cor.</span><span class="sxs-lookup"><span data-stu-id="b6872-131">These are steps to follow to ensure that the content that is displayed on the screen has the best color accuracy.</span></span>

<span data-ttu-id="b6872-132">**Para garantir a precisão da cor no pipeline**</span><span class="sxs-lookup"><span data-stu-id="b6872-132">**To ensure color accuracy in the pipeline**</span></span>

1.  <span data-ttu-id="b6872-133">Se uma textura tiver conteúdo sRGB, verifique se o **ShaderResourceView** tem \_ o [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB para que, ao ler o **ShaderResourceView** no sombreador, você converta o conteúdo da textura do espaço de cores do gama 2,2 para o espaço de cores linear.</span><span class="sxs-lookup"><span data-stu-id="b6872-133">If a texture has sRGB content, ensure the **ShaderResourceView** has the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) so when you read from the **ShaderResourceView** into the shader, you convert the texture content from gamma 2.2-corrected color space to linear color space.</span></span>
2.  <span data-ttu-id="b6872-134">Verifique se o **RenderTargetView** também tem \_ o [modificador de formato](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sRGB para que os valores de saída do sombreador sejam convertidos em gama.</span><span class="sxs-lookup"><span data-stu-id="b6872-134">Ensure the **RenderTargetView** also has the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) so the shader output values are gamma converted.</span></span>

<span data-ttu-id="b6872-135">Se você seguir as etapas anteriores, ao chamar o método [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) , o conteúdo exibido na tela terá a melhor precisão de cor.</span><span class="sxs-lookup"><span data-stu-id="b6872-135">If you follow the preceding steps, when you call the [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) method, the content that is displayed on the screen has the best color accuracy.</span></span>

<span data-ttu-id="b6872-136">Você pode usar o método [**ID3D11Device:: CreateRenderTargetView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) para criar exibições **\_ \_ \* \_ sRGB do formato dxgi** em buffers de fundo de uma cadeia de permuta que você cria somente com um formato **\_ \_ \* \_ UNORM de formato dxgi** .</span><span class="sxs-lookup"><span data-stu-id="b6872-136">You can use the [**ID3D11Device::CreateRenderTargetView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) method to create **DXGI\_FORMAT\_\*\_SRGB** views on back buffers from a swap chain that you create only with a **DXGI\_FORMAT\_\*\_UNORM** format.</span></span> <span data-ttu-id="b6872-137">Essa é uma exceção especial para a regra para criar exibições de destino de renderização, que declara que você pode usar um formato diferente com **ID3D11Device:: CreateRenderTargetView** somente se você criou o recurso que deseja exibir com **o \_ formato dxgi sem \_ \* \_ tipo**.</span><span class="sxs-lookup"><span data-stu-id="b6872-137">This is a special exception to the rule for creating render-target views, which states that you can use a different format with **ID3D11Device::CreateRenderTargetView** only if you created the resource that you want to view with **DXGI\_FORMAT\_\*\_TYPELESS**.</span></span>

<span data-ttu-id="b6872-138">Para obter mais informações sobre regras para converter dados, consulte [regras de conversão de dados](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion).</span><span class="sxs-lookup"><span data-stu-id="b6872-138">For more info about rules for converting data, see [Data Conversion Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion).</span></span>

<span data-ttu-id="b6872-139">Para obter informações sobre como ler e gravar em uma textura simultaneamente, consulte [desempacotando e empacotando o \_ formato dxgi para a edição de imagem In-Place](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format).</span><span class="sxs-lookup"><span data-stu-id="b6872-139">For info about how to simultaneously both read from and write to a texture, see [Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6872-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6872-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6872-141">Aprimorando a apresentação com o modelo de flip, retângulos sujos e áreas roladas</span><span class="sxs-lookup"><span data-stu-id="b6872-141">Enhancing presentation with the flip model, dirty rectangles, and scrolled areas</span></span>](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
