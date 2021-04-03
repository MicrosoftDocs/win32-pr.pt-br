---
description: Outros objetos de origem
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Outros objetos de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646037"
---
# <a name="other-source-objects"></a><span data-ttu-id="811cb-103">Outros objetos de origem</span><span class="sxs-lookup"><span data-stu-id="811cb-103">Other Source Objects</span></span>

<span data-ttu-id="811cb-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="811cb-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="811cb-105">Além das fontes de vídeo e áudio, os [serviços de edição do DirectShow](directshow-editing-services.md) (des) oferecem suporte aos seguintes objetos de origem.</span><span class="sxs-lookup"><span data-stu-id="811cb-105">In addition to video and audio sources, [DirectShow Editing Services](directshow-editing-services.md) (DES) supports the following source objects.</span></span>

<span data-ttu-id="811cb-106">**Imagens ainda**</span><span class="sxs-lookup"><span data-stu-id="811cb-106">**Still Images**</span></span>

<span data-ttu-id="811cb-107">O DES dá suporte aos seguintes formatos de arquivo para imagens ainda:</span><span class="sxs-lookup"><span data-stu-id="811cb-107">DES supports the following file formats for still images:</span></span>

-   <span data-ttu-id="811cb-108">Bitmap (.bpm)</span><span class="sxs-lookup"><span data-stu-id="811cb-108">Bitmap (.bmp)</span></span>
-   <span data-ttu-id="811cb-109">GIF (Graphics Interchange Format)</span><span class="sxs-lookup"><span data-stu-id="811cb-109">GIF (Graphics Interchange Format)</span></span>
-   <span data-ttu-id="811cb-110">JPEG (grupo de especialistas do conjunto fotográfico)</span><span class="sxs-lookup"><span data-stu-id="811cb-110">JPEG (Joint Photographic Experts Group)</span></span>
-   <span data-ttu-id="811cb-111">Adaptador gráfico Targa ou Truevision (. tga): modo 2 (RGB não compactado) em formato de 16 bits, 24, bits ou 32 bits.</span><span class="sxs-lookup"><span data-stu-id="811cb-111">Targa or Truevision Graphics Adapter (.tga): Mode 2 (uncompressed RGB) in 16-bit, 24,-bit, or 32-bit format.</span></span>

<span data-ttu-id="811cb-112">Esses arquivos podem ser usados como imagens ainda ou para criar animações.</span><span class="sxs-lookup"><span data-stu-id="811cb-112">These files can be used as still images or to create animations.</span></span> <span data-ttu-id="811cb-113">Para arquivos bitmap, JPEG e Targa, se você estiver usando o arquivo como uma imagem ainda, chame o método [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) para definir a taxa de quadros como zero.</span><span class="sxs-lookup"><span data-stu-id="811cb-113">For bitmap, JPEG, and Targa files, if you are using the file as a still image, call the [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) method to set the frame rate to zero.</span></span>

<span data-ttu-id="811cb-114">**Sequências DIB**</span><span class="sxs-lookup"><span data-stu-id="811cb-114">**DIB Sequences**</span></span>

<span data-ttu-id="811cb-115">Dada uma série de arquivos bitmap, JPEG ou Targa, o mecanismo de renderização pode construir uma sequência DIB.</span><span class="sxs-lookup"><span data-stu-id="811cb-115">Given a series of bitmap, JPEG, or Targa files, the render engine can construct a DIB sequence.</span></span> <span data-ttu-id="811cb-116">Para criar uma sequência DIB, dê aos arquivos nomes sequenciais numéricos, como Image001.bmp, Image002.bmp, Image003.bmp e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="811cb-116">To create a DIB sequence, give the files numerically sequential names, such as Image001.bmp, Image002.bmp, Image003.bmp, and so on.</span></span> <span data-ttu-id="811cb-117">Use o primeiro arquivo na sequência como a origem.</span><span class="sxs-lookup"><span data-stu-id="811cb-117">Use the first file in the sequence as the source.</span></span> <span data-ttu-id="811cb-118">Defina a taxa de quadros para a sequência chamando [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md).</span><span class="sxs-lookup"><span data-stu-id="811cb-118">Set the frame rate for the sequence by calling [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md).</span></span> <span data-ttu-id="811cb-119">O mecanismo de renderização percorre as imagens na sequência na taxa de quadros especificada.</span><span class="sxs-lookup"><span data-stu-id="811cb-119">The render engine cycles through the images in the sequence at the specified frame rate.</span></span>

<span data-ttu-id="811cb-120">Se a sequência for muito curta para preencher a duração, considerando a taxa de quadros, o restante da duração será um preto sólido.</span><span class="sxs-lookup"><span data-stu-id="811cb-120">If the sequence is too short to fill the duration, given the frame rate, the rest of the duration is solid black.</span></span> <span data-ttu-id="811cb-121">Nenhum erro ocorre durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="811cb-121">No error occurs during rendering.</span></span>

<span data-ttu-id="811cb-122">**Fontes GIF**</span><span class="sxs-lookup"><span data-stu-id="811cb-122">**GIF Sources**</span></span>

<span data-ttu-id="811cb-123">O DES dá suporte a fontes GIF, incluindo GIFs animadas e transparentes, usando a especificação GIF89a.</span><span class="sxs-lookup"><span data-stu-id="811cb-123">DES supports GIF sources, including animated and transparent GIFs, using the GIF89a specification.</span></span> <span data-ttu-id="811cb-124">Com um GIF animado, ao contrário dos outros tipos de arquivo, você não precisa definir a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="811cb-124">With an animated GIF, unlike the other file types, you do not need to set the frame rate.</span></span> <span data-ttu-id="811cb-125">O arquivo GIF especifica o atraso entre cada imagem na animação.</span><span class="sxs-lookup"><span data-stu-id="811cb-125">The GIF file specifies the delay between each image in the animation.</span></span>

<span data-ttu-id="811cb-126">Para dar suporte a GIFs transparentes, o DES converte regiões transparentes na imagem para o RGB terceto RGB (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="811cb-126">To support transparent GIFs, DES converts transparent regions in the image to the RGB triplet RGB(0,0,0).</span></span> <span data-ttu-id="811cb-127">Em seguida, você pode usar a [transição de chave](key-transition.md) para a chave em RGB (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="811cb-127">You can then use the [Key Transition](key-transition.md) to key on RGB(0,0,0).</span></span>

<span data-ttu-id="811cb-128">O DES também converte todas as regiões pretas que estão dentro do intervalo RGB (0 – 7, 0 – 7, 0 – 7) para o valor RGB (8, 8, 8) — exceto para o índice de transparência, se ele cair nesse intervalo.</span><span class="sxs-lookup"><span data-stu-id="811cb-128">DES also converts any black regions that fall within the range RGB(0–7,0–7,0–7) to the value RGB(8,8,8)—except for the transparency index, if it falls in that range.</span></span> <span data-ttu-id="811cb-129">Essa conversão não é detectável para os olhos.</span><span class="sxs-lookup"><span data-stu-id="811cb-129">This conversion is not detectable to the eye.</span></span>

<span data-ttu-id="811cb-130">**Fonte de cores do vídeo**</span><span class="sxs-lookup"><span data-stu-id="811cb-130">**Video Color Source**</span></span>

<span data-ttu-id="811cb-131">O objeto de [fonte de cor do vídeo](video-color-source.md) cria uma imagem de vídeo contínua de uma cor sólida.</span><span class="sxs-lookup"><span data-stu-id="811cb-131">The [Video Color Source](video-color-source.md) object creates a continuous video image of a solid color.</span></span> <span data-ttu-id="811cb-132">Um uso para esse objeto é torná-lo uma camada em uma transição.</span><span class="sxs-lookup"><span data-stu-id="811cb-132">One use for this object is to make it a layer in a transition.</span></span> <span data-ttu-id="811cb-133">Por exemplo, use-o em um vídeo fade-in ou esmaecimento.</span><span class="sxs-lookup"><span data-stu-id="811cb-133">For example, use it in a video fade-in or fade-out.</span></span>

<span data-ttu-id="811cb-134">**Filtros de origem personalizados**</span><span class="sxs-lookup"><span data-stu-id="811cb-134">**Custom Source Filters**</span></span>

<span data-ttu-id="811cb-135">O DES pode usar um filtro de origem do DirectShow como uma origem da linha do tempo, se o filtro atender às seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="811cb-135">DES can use a DirectShow source filter as a timeline source, if the filter meets the following conditions:</span></span>

-   <span data-ttu-id="811cb-136">Ele dá suporte à busca</span><span class="sxs-lookup"><span data-stu-id="811cb-136">It supports seeking</span></span>
-   <span data-ttu-id="811cb-137">Ele produz um formato compatível com o DES.</span><span class="sxs-lookup"><span data-stu-id="811cb-137">It produces a format that DES supports.</span></span> <span data-ttu-id="811cb-138">O formato pode ser compactado, desde que o sistema do usuário tenha um filtro do DirectShow capaz de decodificá-lo.</span><span class="sxs-lookup"><span data-stu-id="811cb-138">The format can be compressed as long as the user's system has a DirectShow filter capable of decoding it.</span></span>

<span data-ttu-id="811cb-139">Para usar uma fonte personalizada, especifique o CLSID do filtro como o GUID do subobjeto do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="811cb-139">To use a custom source, specify the CLSID of the filter as the subobject GUID of the source object.</span></span> <span data-ttu-id="811cb-140">Para obter mais informações, consulte [subobjetos](subobjects.md).</span><span class="sxs-lookup"><span data-stu-id="811cb-140">For more information, see [Subobjects](subobjects.md).</span></span> <span data-ttu-id="811cb-141">Para dar suporte a propriedades personalizadas, implemente-as como propriedades de **IDispatch** "Put".</span><span class="sxs-lookup"><span data-stu-id="811cb-141">To support custom properties, implement them as **IDispatch** "put" properties.</span></span> <span data-ttu-id="811cb-142">Somente propriedades estáticas têm suporte em objetos de origem; Não há suporte para propriedades dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="811cb-142">Only static properties are supported on source objects; dynamic properties are not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="811cb-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="811cb-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="811cb-144">Trabalhando com fontes</span><span class="sxs-lookup"><span data-stu-id="811cb-144">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



