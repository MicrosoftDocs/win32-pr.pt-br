---
title: Trackbars
description: Trackbars
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Capas móveis do Windows Media Player, trackbars
- capas, trackbars
- referência para capas, trackbars
- trackbars em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105807872"
---
# <a name="trackbars"></a><span data-ttu-id="a70c9-107">Trackbars</span><span class="sxs-lookup"><span data-stu-id="a70c9-107">Trackbars</span></span>

<span data-ttu-id="a70c9-108">Um TrackBar exibe uma imagem que muda em pequenos incrementos.</span><span class="sxs-lookup"><span data-stu-id="a70c9-108">A trackbar displays an image that changes in small increments.</span></span> <span data-ttu-id="a70c9-109">Trackbars são usados para controles de volume e controles de posição de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a70c9-109">Trackbars are used for volume controls and playback position controls.</span></span> <span data-ttu-id="a70c9-110">Você pode usar trackbars para exibir informações sobre o item de mídia atual ou para permitir que o usuário altere as configurações ou a posição de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a70c9-110">You can use trackbars to display information about the current media item or to allow the user to change settings or playback position.</span></span> <span data-ttu-id="a70c9-111">Por exemplo, você pode usar um TrackBar para permitir que o usuário ajuste o volume e outro TrackBar que possa mostrar o usuário a posição de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="a70c9-111">For example, you can use a trackbar to enable the user to adjust the volume, and another trackbar that can show the user the current playback position.</span></span> <span data-ttu-id="a70c9-112">Trackbars têm uma imagem em miniatura que define a configuração atual do valor de TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a70c9-112">Trackbars have a thumb image that defines the current setting of the trackbar value.</span></span>

<span data-ttu-id="a70c9-113">A seção trackbars do arquivo de definição de capa deve começar com esta linha:</span><span class="sxs-lookup"><span data-stu-id="a70c9-113">The Trackbars section of the skin definition file must begin with this line:</span></span>


```C++
[ Trackbars ]

```



<span data-ttu-id="a70c9-114">Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre cada uma das trackbars em sua capa.</span><span class="sxs-lookup"><span data-stu-id="a70c9-114">You then must add one or more lines that contain information about each of the trackbars in your skin.</span></span>


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



<span data-ttu-id="a70c9-115">Você pode usar o modelo a seguir para a seção trackbars do seu arquivo de definição de capa:</span><span class="sxs-lookup"><span data-stu-id="a70c9-115">You can use the following template for the Trackbars section of your skin definition file:</span></span>


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



<span data-ttu-id="a70c9-116">Você deve usar a seguinte ordem para informações de TrackBar para cada linha na seção trackbars (cada parte da linha é necessária):</span><span class="sxs-lookup"><span data-stu-id="a70c9-116">You must use the following order for trackbar information for each line in the Trackbars section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="a70c9-117">Tipo de TrackBar</span><span class="sxs-lookup"><span data-stu-id="a70c9-117">Trackbar Type</span></span>](trackbar-type.md)
2.  [<span data-ttu-id="a70c9-118">Local TrackBar</span><span class="sxs-lookup"><span data-stu-id="a70c9-118">Trackbar Location</span></span>](trackbar-location.md)
3.  [<span data-ttu-id="a70c9-119">Origem da imagem para TrackBar desabilitada</span><span class="sxs-lookup"><span data-stu-id="a70c9-119">Image Source for Disabled Trackbar</span></span>](image-source-for-disabled-trackbar.md)
4.  [<span data-ttu-id="a70c9-120">Origem da imagem em miniatura</span><span class="sxs-lookup"><span data-stu-id="a70c9-120">Thumb Image Source</span></span>](thumb-image-source.md)
5.  [<span data-ttu-id="a70c9-121">Tamanho da miniatura</span><span class="sxs-lookup"><span data-stu-id="a70c9-121">Thumb Size</span></span>](thumb-size.md)

<span data-ttu-id="a70c9-122">Para obter um exemplo de código trackbars, consulte a [seção trackbars de exemplo](sample-trackbars-section.md).</span><span class="sxs-lookup"><span data-stu-id="a70c9-122">For an example of Trackbars code, see [Sample Trackbars Section](sample-trackbars-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a70c9-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a70c9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a70c9-124">**Referência de capa**</span><span class="sxs-lookup"><span data-stu-id="a70c9-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




