---
title: Usando paletas do MCIWnd
description: Usando paletas do MCIWnd
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- Macro MCIWndGetPalette
- Macro MCIWndSetPalette
- Macro MCIWndRealize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917272"
---
# <a name="using-mciwnd-palettes"></a><span data-ttu-id="c906d-106">Usando paletas do MCIWnd</span><span class="sxs-lookup"><span data-stu-id="c906d-106">Using MCIWnd Palettes</span></span>

<span data-ttu-id="c906d-107">A reprodução de clipes de vídeo com intensidade de cor de 8 bits (256-capacidade de cor) requer uma paleta para definir as cores que estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="c906d-107">Playing video clips with 8-bit color depth (256-color capacity) requires a palette to define the colors being used.</span></span> <span data-ttu-id="c906d-108">Às vezes, a paleta incluída com um videoclipe não é a paleta mais apropriada a ser usada durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="c906d-108">Sometimes, the palette included with a video clip is not the most appropriate palette to use during playback.</span></span> <span data-ttu-id="c906d-109">Nesse caso, o MCIWnd fornece três maneiras de gerenciar paletas para reprodução:</span><span class="sxs-lookup"><span data-stu-id="c906d-109">In this case, MCIWnd provides three ways to manage palettes for playback:</span></span>

-   <span data-ttu-id="c906d-110">Recupere um identificador para a paleta associada a uma janela MCIWnd usando a macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="c906d-110">Retrieve a handle to the palette associated with an MCIWnd window by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span> <span data-ttu-id="c906d-111">A paleta não está necessariamente associada exclusivamente à janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="c906d-111">The palette is not necessarily associated exclusively with the MCIWnd window.</span></span> <span data-ttu-id="c906d-112">Outros aplicativos podem acessar, e até mesmo invalidar, o identificador da paleta.</span><span class="sxs-lookup"><span data-stu-id="c906d-112">Other applications can access, and even invalidate, the palette handle.</span></span> <span data-ttu-id="c906d-113">Consequentemente, seu aplicativo deve antecipar o uso global da paleta e, quando terminar com a paleta, não deve liberá-la.</span><span class="sxs-lookup"><span data-stu-id="c906d-113">Consequently, your application should anticipate the global use of the palette and, when finished with the palette, should not free it.</span></span>
-   <span data-ttu-id="c906d-114">Especifique uma nova paleta a ser usada com o clipe de vídeo associado a uma janela MCIWnd usando a macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .</span><span class="sxs-lookup"><span data-stu-id="c906d-114">Specify a new palette to use with the video clip associated with an MCIWnd window by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>
-   <span data-ttu-id="c906d-115">Perceba a paleta associada a uma janela do MCIWnd para a paleta do sistema usando a macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .</span><span class="sxs-lookup"><span data-stu-id="c906d-115">Realize the palette associated with an MCIWnd window to the system palette by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span> <span data-ttu-id="c906d-116">Essa macro chama a função [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) com a paleta associada à janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="c906d-116">This macro calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function with the palette associated with the MCIWnd window.</span></span> <span data-ttu-id="c906d-117">Se os manipuladores de mensagens do aplicativo para o [**WM \_ PaletteChanged**](/windows/desktop/gdi/wm-palettechanged) e o [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) chamarem somente **RealizePalette** ou **MCIWndRealize**, você deverá encaminhar essas mensagens para MCIWnd se não as tratar.</span><span class="sxs-lookup"><span data-stu-id="c906d-117">If your application message handlers for [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) call only **RealizePalette** or **MCIWndRealize**, you must forward these messages to MCIWnd if you do not handle them yourself.</span></span>

> [!Note]  
> <span data-ttu-id="c906d-118">Quando um clipe de vídeo com profundidade de cor de 8 bits é carregado na janela MCIWnd, a paleta incluída nesse clipe substitui a paleta associada à janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="c906d-118">When a video clip with 8-bit color depth is loaded into the MCIWnd window, the palette included with that clip replaces the palette associated with the MCIWnd window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c906d-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c906d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c906d-120">Aprimoramentos de reprodução</span><span class="sxs-lookup"><span data-stu-id="c906d-120">Playback Enhancements</span></span>](playback-enhancements.md)
</dt> </dl>

 

 