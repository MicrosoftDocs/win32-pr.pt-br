---
description: O sistema manipula cores em bitmaps de forma diferente das cores em canetas, pincéis e texto.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Cor em bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091205"
---
# <a name="color-in-bitmaps"></a><span data-ttu-id="154d4-103">Cor em bitmaps</span><span class="sxs-lookup"><span data-stu-id="154d4-103">Color in Bitmaps</span></span>

<span data-ttu-id="154d4-104">O sistema manipula cores em bitmaps de forma diferente das cores em canetas, pincéis e texto.</span><span class="sxs-lookup"><span data-stu-id="154d4-104">The system handles colors in bitmaps differently than colors in pens, brushes, and text.</span></span> <span data-ttu-id="154d4-105">Os bitmaps compatíveis, criados usando a função [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) ou [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , são específicos do dispositivo e retêm informações de cores em um formato dependente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="154d4-105">Compatible bitmaps, created by using the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, are device specific and retain color information in a device-dependent format.</span></span> <span data-ttu-id="154d4-106">Nenhum valor de cor é usado e as cores não estão sujeitas a aproximações e pontilhamento.</span><span class="sxs-lookup"><span data-stu-id="154d4-106">No color values are used, and the colors are not subject to approximations and dithering.</span></span>

<span data-ttu-id="154d4-107">Os bitmaps independentes de dispositivo (DIBs) retêm informações de cores como valores de cor ou índices de paleta de cores.</span><span class="sxs-lookup"><span data-stu-id="154d4-107">Device-independent bitmaps (DIBs) retain color information either as color values or color palette indexes.</span></span> <span data-ttu-id="154d4-108">Se forem usados valores de cor, as cores estarão sujeitas à aproximação, mas não ao pontilhamento.</span><span class="sxs-lookup"><span data-stu-id="154d4-108">If color values are used, the colors are subject to approximation, but not dithering.</span></span> <span data-ttu-id="154d4-109">Os índices de paleta de cores só podem ser usados com dispositivos que dão suporte a paletas de cores.</span><span class="sxs-lookup"><span data-stu-id="154d4-109">Color palette indexes can only be used with devices that support color palettes.</span></span> <span data-ttu-id="154d4-110">Embora o sistema não tenha cores aproximadas ou pontilhadas identificadas por índices, a cor resultante pode ser diferente daquela desejada, pois os índices geram resultados válidos apenas no contexto da paleta de cores que era atual no momento em que o bitmap foi criado.</span><span class="sxs-lookup"><span data-stu-id="154d4-110">Although the system does not approximate or dither colors identified by indexes, the resulting color may be different than that intended, because the indexes yield valid results only in the context of the color palette that was current at the time the bitmap was created.</span></span> <span data-ttu-id="154d4-111">Se a paleta for alterada, faça as cores no bitmap.</span><span class="sxs-lookup"><span data-stu-id="154d4-111">If the palette changes, so do the colors in the bitmap.</span></span> <span data-ttu-id="154d4-112">Para obter mais informações sobre índices de paleta, consulte [Default Palette](default-palette.md) and [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span><span class="sxs-lookup"><span data-stu-id="154d4-112">For more information on palette indexes, see [Default Palette](default-palette.md) and [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span></span>

<span data-ttu-id="154d4-113">Além de referenciar a paleta lógica, um aplicativo também pode fazer referência a um valor em uma tabela de cores DIB.</span><span class="sxs-lookup"><span data-stu-id="154d4-113">In addition to referencing the logical palette, an application can also reference a value in a DIB color table.</span></span> <span data-ttu-id="154d4-114">Para selecionar uma cor em uma tabela de cores DIB, chame [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span><span class="sxs-lookup"><span data-stu-id="154d4-114">To select a color in a DIB color table, call [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span></span> <span data-ttu-id="154d4-115">Observe que isso só é possível para um contexto de dispositivo que tenha um DIB selecionado para ele.</span><span class="sxs-lookup"><span data-stu-id="154d4-115">Note that this is only possible for a device context that has a DIB selected into it.</span></span>

 

 



