---
description: Mesclagem alfa
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: Mesclagem alfa (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4293448849926cfc6723495619137262e004636e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087835"
---
# <a name="alpha-blending-directshow"></a><span data-ttu-id="db3e5-103">Mesclagem alfa (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="db3e5-103">Alpha Blending (DirectShow)</span></span>

<span data-ttu-id="db3e5-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="db3e5-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="db3e5-105">Este artigo descreve a mistura alfa nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="db3e5-105">This article describes alpha blending in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="db3e5-106">Alfa mede a transparência de um pixel ou imagem.</span><span class="sxs-lookup"><span data-stu-id="db3e5-106">Alpha measures the transparency of a pixel or image.</span></span> <span data-ttu-id="db3e5-107">No vídeo RGB não compactado de 32 bits, quatro componentes definem cada pixel: um canal alfa (A) e três componentes de cor (RGB).</span><span class="sxs-lookup"><span data-stu-id="db3e5-107">In 32-bit uncompressed RGB video, four components define each pixel: an alpha channel (A) and three color components (RGB).</span></span> <span data-ttu-id="db3e5-108">Um pixel com um valor alfa igual a zero é completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="db3e5-108">A pixel with an alpha value of zero is completely transparent.</span></span> <span data-ttu-id="db3e5-109">Um pixel com um valor alfa de 255 é opaco.</span><span class="sxs-lookup"><span data-stu-id="db3e5-109">A pixel with an alpha value of 255 is opaque.</span></span> <span data-ttu-id="db3e5-110">Entre esses valores, o pixel tem vários graus de transparência.</span><span class="sxs-lookup"><span data-stu-id="db3e5-110">Between these values, the pixel has various degrees of transparency.</span></span>

<span data-ttu-id="db3e5-111">O DirectShow define dois tipos de mídia para vídeo RGB de 32 bits:</span><span class="sxs-lookup"><span data-stu-id="db3e5-111">DirectShow defines two media types for 32-bit RGB video:</span></span>

-   <span data-ttu-id="db3e5-112">**MEDIASUBTYPE \_ ARGB32**: o vídeo é RGB de 32 bits com um canal alfa válido.</span><span class="sxs-lookup"><span data-stu-id="db3e5-112">**MEDIASUBTYPE\_ARGB32**: The video is 32-bit RGB with a valid alpha channel.</span></span>
-   <span data-ttu-id="db3e5-113">**MEDIASUBTYPE \_ RGB32**: os pixels são 32 bits, mas o canal alfa não é necessariamente válido.</span><span class="sxs-lookup"><span data-stu-id="db3e5-113">**MEDIASUBTYPE\_RGB32**: Pixels are 32 bits, but the alpha channel is not necessarily valid.</span></span>

<span data-ttu-id="db3e5-114">Para executar a mesclagem alfa no DES, defina o tipo de mídia descompactado do grupo de vídeos como MEDIASUBTYPE \_ ARGB32.</span><span class="sxs-lookup"><span data-stu-id="db3e5-114">To perform alpha blending in DES, set the video group's uncompressed media type to MEDIASUBTYPE\_ARGB32.</span></span> <span data-ttu-id="db3e5-115">Em C++, chame o método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="db3e5-115">In C++, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span> <span data-ttu-id="db3e5-116">No formato XTL, definir o atributo [**bitdepth**](bitdepth-attribute.md) do elemento [**Group**](group-element.md) como 32 também realiza isso.</span><span class="sxs-lookup"><span data-stu-id="db3e5-116">In the XTL format, setting the [**bitdepth**](bitdepth-attribute.md) attribute of the [**group**](group-element.md) element to 32 accomplishes this as well.</span></span>

<span data-ttu-id="db3e5-117">Em seguida, você precisa de dados de vídeo que contenham um canal alfa.</span><span class="sxs-lookup"><span data-stu-id="db3e5-117">Next, you need video data that contains an alpha channel.</span></span> <span data-ttu-id="db3e5-118">Há várias opções:</span><span class="sxs-lookup"><span data-stu-id="db3e5-118">There are several options:</span></span>

-   <span data-ttu-id="db3e5-119">Você pode usar um arquivo AVI que já tem vídeo RGB de 32 bits com dados alfa.</span><span class="sxs-lookup"><span data-stu-id="db3e5-119">You can use an AVI file that already has 32-bit RGB video with alpha data.</span></span> <span data-ttu-id="db3e5-120">Atualmente, o Alpha não tem suporte para arquivos de origem MPEG ou Microsoft Windows Media Format (WMF).</span><span class="sxs-lookup"><span data-stu-id="db3e5-120">Currently, alpha is not supported for MPEG or Microsoft Windows Media Format (WMF) source files.</span></span>
-   <span data-ttu-id="db3e5-121">O DES dá suporte a arquivos de bitmap de 32 bits (. bmp) e de Targa (. tga) com dados alfa.</span><span class="sxs-lookup"><span data-stu-id="db3e5-121">DES supports 32-bit bitmap (.bmp) and Targa (.tga) files with alpha data.</span></span>
-   <span data-ttu-id="db3e5-122">Você pode escrever um filtro de origem personalizado que cria dados RGB de 32 bits com Alfa.</span><span class="sxs-lookup"><span data-stu-id="db3e5-122">You can write a custom source filter that creates 32-bit RGB data with alpha.</span></span> <span data-ttu-id="db3e5-123">O tipo de mídia de saída deve ser **MEDIASUBTYPE \_ ARGB32**.</span><span class="sxs-lookup"><span data-stu-id="db3e5-123">The output media type must be **MEDIASUBTYPE\_ARGB32**.</span></span> <span data-ttu-id="db3e5-124">Use o filtro como o subobjeto em um objeto de origem da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="db3e5-124">Use the filter as the subobject in a timeline source object.</span></span>

<span data-ttu-id="db3e5-125">Se a fonte de vídeo não tiver alfa, você poderá usar um efeito que cria dados alfa.</span><span class="sxs-lookup"><span data-stu-id="db3e5-125">If your video source does not have alpha, you can use an effect that creates alpha data.</span></span> <span data-ttu-id="db3e5-126">O [efeito de setter alfa](alpha-setter-effect.md) define o canal alfa para a imagem inteira como um valor constante.</span><span class="sxs-lookup"><span data-stu-id="db3e5-126">The [Alpha Setter Effect](alpha-setter-effect.md) sets the alpha channel for the entire image to a constant value.</span></span> <span data-ttu-id="db3e5-127">Para variar o alfa ao longo do tempo, use a interface [**IPropertySetter**](ipropertysetter.md) com o efeito de setter alfa.</span><span class="sxs-lookup"><span data-stu-id="db3e5-127">To vary the alpha over time, use the [**IPropertySetter**](ipropertysetter.md) interface with the Alpha Setter Effect.</span></span> <span data-ttu-id="db3e5-128">A fonte original não precisa ser de 32 bits, desde que o tipo de mídia descompactado do grupo seja **MEDIASUBTYPE \_ ARGB32**.</span><span class="sxs-lookup"><span data-stu-id="db3e5-128">The original source does not have to be 32 bits, as long as the group's uncompressed media type is **MEDIASUBTYPE\_ARGB32**.</span></span>

<span data-ttu-id="db3e5-129">Por fim, passe o vídeo para um efeito ou transição que executa a mistura alfa.</span><span class="sxs-lookup"><span data-stu-id="db3e5-129">Finally, pass the video to an effect or transition that performs alpha blending.</span></span> <span data-ttu-id="db3e5-130">A [transição do compositor](compositor-transition.md) executa a mesclagem alfa e a [transição de chave](key-transition.md) pode ser a chave por valor alfa.</span><span class="sxs-lookup"><span data-stu-id="db3e5-130">The [Compositor Transition](compositor-transition.md) performs alpha blending, and the [Key Transition](key-transition.md) can key by alpha value.</span></span>

<span data-ttu-id="db3e5-131">O projeto de exemplo XTL a seguir executa a mesclagem alfa:</span><span class="sxs-lookup"><span data-stu-id="db3e5-131">The following sample XTL project performs alpha blending:</span></span>


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a><span data-ttu-id="db3e5-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db3e5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db3e5-133">Usando os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="db3e5-133">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



