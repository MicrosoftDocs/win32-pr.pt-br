---
description: Além da região de atualização, cada janela tem uma região visível que define a parte da janela visível para o usuário.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Regiões da janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02555339412c604f79f69294febbab524fc92a70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011410"
---
# <a name="window-regions"></a><span data-ttu-id="1843b-103">Regiões da janela</span><span class="sxs-lookup"><span data-stu-id="1843b-103">Window Regions</span></span>

<span data-ttu-id="1843b-104">Além da região de atualização, cada janela tem uma *região visível* que define a parte da janela visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="1843b-104">In addition to the update region, every window has a *visible region* that defines the window portion visible to the user.</span></span> <span data-ttu-id="1843b-105">O sistema altera a região visível para a janela sempre que a janela muda de tamanho ou sempre que outra janela é movida, de modo que ela obscurece ou expõe uma parte da janela.</span><span class="sxs-lookup"><span data-stu-id="1843b-105">The system changes the visible region for the window whenever the window changes size or whenever another window is moved such that it obscures or exposes a portion of the window.</span></span> <span data-ttu-id="1843b-106">Os aplicativos não podem alterar a região visível diretamente, mas o sistema usa automaticamente a região visível para criar a região de recorte para qualquer contexto de dispositivo de exibição recuperado para a janela.</span><span class="sxs-lookup"><span data-stu-id="1843b-106">Applications cannot change the visible region directly, but the system automatically uses the visible region to create the clipping region for any display device context retrieved for the window.</span></span>

<span data-ttu-id="1843b-107">A *região de recorte* determina onde o sistema permite desenhar.</span><span class="sxs-lookup"><span data-stu-id="1843b-107">The *clipping region* determines where the system permits drawing.</span></span> <span data-ttu-id="1843b-108">Quando o aplicativo recupera um contexto de dispositivo de exibição usando a função [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , o sistema define a região de recorte para o contexto do dispositivo para a interseção da região visível e a região de atualização.</span><span class="sxs-lookup"><span data-stu-id="1843b-108">When the application retrieves a display device context using the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function, the system sets the clipping region for the device context to the intersection of the visible region and the update region.</span></span> <span data-ttu-id="1843b-109">Os aplicativos podem alterar a região de recorte usando funções como [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) e [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), para limitar ainda mais o desenho a uma parte específica da área de atualização.</span><span class="sxs-lookup"><span data-stu-id="1843b-109">Applications can change the clipping region by using functions such as [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) and [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), to further limit drawing to a particular portion of the update area.</span></span>

<span data-ttu-id="1843b-110">Os \_ estilos WS CLIPCHILDREN e WS \_ CLIPSIBLINGS especificam ainda mais como o sistema calcula a região visível para uma janela.</span><span class="sxs-lookup"><span data-stu-id="1843b-110">The WS\_CLIPCHILDREN and WS\_CLIPSIBLINGS styles further specify how the system calculates the visible region for a window.</span></span> <span data-ttu-id="1843b-111">Se uma janela tiver um ou ambos os estilos, a região visível excluirá todas as janelas filhas ou irmãos (Windows com a mesma janela pai).</span><span class="sxs-lookup"><span data-stu-id="1843b-111">If a window has one or both of these styles, the visible region excludes any child window or sibling windows (windows having the same parent window).</span></span> <span data-ttu-id="1843b-112">Portanto, o desenho que, de outra forma, invasoria nessas janelas sempre será recortado.</span><span class="sxs-lookup"><span data-stu-id="1843b-112">Therefore, drawing that would otherwise intrude in these windows will always be clipped.</span></span>

 

 



