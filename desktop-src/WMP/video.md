---
title: Vídeo (SDK do Windows Media Player)
description: Vídeo
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Aparências móveis do Windows Media Player, vídeo
- capas, vídeo
- referência para capas, vídeo
- vídeo em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105764505"
---
# <a name="video-windows-media-player-sdk"></a><span data-ttu-id="1f71c-107">Vídeo (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="1f71c-107">Video (Windows Media Player SDK)</span></span>

<span data-ttu-id="1f71c-108">Uma exibição de vídeo permite que o usuário exiba arquivos de vídeo digital.</span><span class="sxs-lookup"><span data-stu-id="1f71c-108">A video display allows the user to view digital video files.</span></span> <span data-ttu-id="1f71c-109">A área de exibição de vídeo só fica visível quando o vídeo é reproduzido ou pausado.</span><span class="sxs-lookup"><span data-stu-id="1f71c-109">The video display area is only visible when video is playing or paused.</span></span> <span data-ttu-id="1f71c-110">Ao projetar sua capa, você desejará reservar espaço na imagem de plano de fundo para conter a exibição do vídeo.</span><span class="sxs-lookup"><span data-stu-id="1f71c-110">When you design your skin, you will want to reserve space in the Background image to contain the video display.</span></span> <span data-ttu-id="1f71c-111">Se você não fizer isso, a exibição de vídeo poderá se sobrepor a qualquer arte visível, como o arquivo de plano de fundo, os botões e o trackbars, que impedirá o usuário de operar os controles em sua capa.</span><span class="sxs-lookup"><span data-stu-id="1f71c-111">If you don't, the video display may superimpose itself over any visible art, such as the Background file, buttons, and trackbars, which will keep the user from operating the controls on your skin.</span></span>

<span data-ttu-id="1f71c-112">A seção de vídeo do arquivo de definição de capa deve começar com esta linha:</span><span class="sxs-lookup"><span data-stu-id="1f71c-112">The Video section of the skin definition file must begin with this line:</span></span>


```C++
[ Video ]

```



<span data-ttu-id="1f71c-113">Em seguida, você deve adicionar uma linha que especifica o local e o tamanho da área de exibição do vídeo em sua capa.</span><span class="sxs-lookup"><span data-stu-id="1f71c-113">You then must add a line that specifies the location and size of the video display area in your skin.</span></span>


```C++
0,38,240,172

```



<span data-ttu-id="1f71c-114">Você pode usar o modelo a seguir para a seção de vídeo de seu arquivo de definição de capa:</span><span class="sxs-lookup"><span data-stu-id="1f71c-114">You can use the following template for the Video section of your skin definition file:</span></span>


```C++
//  <Location>
//  ----------

```



<span data-ttu-id="1f71c-115">As seções a seguir fornecem mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="1f71c-115">The following sections provide further details.</span></span>

-   [<span data-ttu-id="1f71c-116">Local do vídeo</span><span class="sxs-lookup"><span data-stu-id="1f71c-116">Video Location</span></span>](video-location.md)
-   [<span data-ttu-id="1f71c-117">Origem da imagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="1f71c-117">Video Image Source</span></span>](video-image-source.md)
-   [<span data-ttu-id="1f71c-118">Tamanho do vídeo</span><span class="sxs-lookup"><span data-stu-id="1f71c-118">Video Size</span></span>](video-size.md)
-   [<span data-ttu-id="1f71c-119">Exemplo de seção de vídeo</span><span class="sxs-lookup"><span data-stu-id="1f71c-119">Sample Video Section</span></span>](sample-video-section.md)

## <a name="related-topics"></a><span data-ttu-id="1f71c-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f71c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f71c-121">**Referência de capa**</span><span class="sxs-lookup"><span data-stu-id="1f71c-121">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




