---
description: Correção de taxa de proporção
ms.assetid: 0ed6010b-9168-44b1-be49-0c9d5d77ce3f
title: Correção de taxa de proporção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2460f7ecce1513394d941eafe8bdf8a7a80e9727
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105771676"
---
# <a name="aspect-ratio-correction"></a><span data-ttu-id="b52e3-103">Correção de taxa de proporção</span><span class="sxs-lookup"><span data-stu-id="b52e3-103">Aspect Ratio Correction</span></span>

<span data-ttu-id="b52e3-104">Este tópico aplica-se ao Windows XP Service Pack 2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b52e3-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="b52e3-105">No modo de combinação, o VMR dimensiona o vídeo para a taxa de proporção correta.</span><span class="sxs-lookup"><span data-stu-id="b52e3-105">In mixing mode, the VMR sizes the video to the correct aspect ratio.</span></span> <span data-ttu-id="b52e3-106">(Exceção: consulte [mixagem sem quadrados](non-square-mixing.md).) Isso pode exigir o alongamento do vídeo se a taxa de proporção preferida não for igual à taxa de proporção física da imagem.</span><span class="sxs-lookup"><span data-stu-id="b52e3-106">(Exception: See [Non-Square Mixing](non-square-mixing.md).) This may require stretching the video if the preferred aspect ratio is not the same as the image's physical aspect ratio.</span></span> <span data-ttu-id="b52e3-107">Por exemplo, o formato DV (Digital Video) é 720 x 480 pixels (3:2), mas deve ser exibido a uma taxa de proporção de 4:3.</span><span class="sxs-lookup"><span data-stu-id="b52e3-107">For example, digital video (DV) format is 720 x 480 pixels (3:2) but should be displayed at a 4:3 aspect ratio.</span></span>

<span data-ttu-id="b52e3-108">O VMR dá suporte a dois comportamentos diferentes para correção de taxa de proporção:</span><span class="sxs-lookup"><span data-stu-id="b52e3-108">The VMR supports two different behaviors for aspect ratio correction:</span></span>

-   <span data-ttu-id="b52e3-109">Ajuste o tamanho horizontal ou vertical, para que a imagem sempre seja ampliada, nunca reduzida.</span><span class="sxs-lookup"><span data-stu-id="b52e3-109">Adjust either the horizontal or vertical size, so that the image is always stretched, never shrunk.</span></span> <span data-ttu-id="b52e3-110">Esse agora é o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="b52e3-110">This is now the default behavior.</span></span>
-   <span data-ttu-id="b52e3-111">Ajuste o tamanho horizontal, alongando ou reduzindo o vídeo.</span><span class="sxs-lookup"><span data-stu-id="b52e3-111">Adjust the horizontal size, either stretching or shrinking the video.</span></span>

<span data-ttu-id="b52e3-112">Como o segundo comportamento (somente ajuste horizontal) pode envolver a redução do vídeo, a imagem de saída pode ter menos resolução.</span><span class="sxs-lookup"><span data-stu-id="b52e3-112">Because the second behavior (horizontal adjustment only) may entail shrinking the video, the output image may have less resolution.</span></span> <span data-ttu-id="b52e3-113">Por esse motivo, o primeiro comportamento é preferencial.</span><span class="sxs-lookup"><span data-stu-id="b52e3-113">For this reason, the first behavior is preferred.</span></span> <span data-ttu-id="b52e3-114">Por exemplo, no caso do vídeo 720 x 480 na taxa de proporção 4:3, o comportamento padrão produz uma imagem 720 x 550, enquanto o ajuste horizontal produz uma imagem menor de 640 x 480.</span><span class="sxs-lookup"><span data-stu-id="b52e3-114">For example, in the case of 720 x 480 video at 4:3 aspect ratio, the default behavior produces a 720 x 550 image, while horizontal adjustment produces a smaller 640 x 480 image.</span></span>

<span data-ttu-id="b52e3-115">**VMR-7**: para definir a preferência de correção de taxa de proporção, chame [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span><span class="sxs-lookup"><span data-stu-id="b52e3-115">**VMR-7**: To set the aspect ratio correction preference, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span></span> <span data-ttu-id="b52e3-116">Defina o \_ sinalizador MixerPref ARAdjustXorY para o comportamento padrão ou desmarque este sinalizador apenas para ajuste horizontal.</span><span class="sxs-lookup"><span data-stu-id="b52e3-116">Set the MixerPref\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

<span data-ttu-id="b52e3-117">**VMR-9**: para definir a preferência de correção de taxa de proporção, chame [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span><span class="sxs-lookup"><span data-stu-id="b52e3-117">**VMR-9**: To set the aspect ratio correction preference, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span></span> <span data-ttu-id="b52e3-118">Defina o \_ sinalizador MixerPref9 ARAdjustXorY para o comportamento padrão ou desmarque este sinalizador apenas para ajuste horizontal.</span><span class="sxs-lookup"><span data-stu-id="b52e3-118">Set the MixerPref9\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b52e3-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b52e3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b52e3-120">Usando o modo de mixagem do VMR</span><span class="sxs-lookup"><span data-stu-id="b52e3-120">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



