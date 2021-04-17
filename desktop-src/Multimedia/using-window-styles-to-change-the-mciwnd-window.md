---
title: Usando estilos de janela para alterar a janela MCIWnd
description: Usando estilos de janela para alterar a janela MCIWnd
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- Função MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758948"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a><span data-ttu-id="66aff-104">Usando estilos de janela para alterar a janela MCIWnd</span><span class="sxs-lookup"><span data-stu-id="66aff-104">Using Window Styles to Change the MCIWnd Window</span></span>

<span data-ttu-id="66aff-105">Assim como em qualquer janela, você pode alterar a aparência e o comportamento de uma janela MCIWnd escolhendo os estilos de janela padrão especificados com a função [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="66aff-105">As with any window, you can change the appearance and behavior of an MCIWnd window by choosing from the standard window styles specified with the [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="66aff-106">Além disso, você pode escolher entre vários outros estilos de janela que são específicos para o Windows MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="66aff-106">In addition, you can choose from several other window styles that are specific to MCIWnd windows.</span></span> <span data-ttu-id="66aff-107">Com esses estilos, seu aplicativo pode alterar essas janelas MCIWnd das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="66aff-107">With these styles, your application can change these MCIWnd windows in the following ways:</span></span>

-   <span data-ttu-id="66aff-108">Alterar o tamanho da janela.</span><span class="sxs-lookup"><span data-stu-id="66aff-108">Change window size.</span></span>
-   <span data-ttu-id="66aff-109">Ocultar ou exibir controles.</span><span class="sxs-lookup"><span data-stu-id="66aff-109">Hide or display controls.</span></span>
-   <span data-ttu-id="66aff-110">Emitir mensagens de notificação.</span><span class="sxs-lookup"><span data-stu-id="66aff-110">Issue notification messages.</span></span>
-   <span data-ttu-id="66aff-111">Exibir informações na barra de título.</span><span class="sxs-lookup"><span data-stu-id="66aff-111">Display information in the title bar.</span></span>

<span data-ttu-id="66aff-112">Você pode definir estilos de janela especificando-os na função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) ou pode usar a macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) para alterar o estilo de uma janela existente do MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="66aff-112">You can set window styles by specifying them in the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function, or you can use the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro to change the style of an existing MCIWnd window.</span></span> <span data-ttu-id="66aff-113">Você também pode consultar uma janela MCIWnd para seus estilos atuais usando a macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .</span><span class="sxs-lookup"><span data-stu-id="66aff-113">You can also query an MCIWnd window for its current styles by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>

<span data-ttu-id="66aff-114">Para obter uma lista dos estilos de janela específicos do MCIWnd, consulte [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span><span class="sxs-lookup"><span data-stu-id="66aff-114">For a list of the MCIWnd-specific window styles, see [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span>

 

 