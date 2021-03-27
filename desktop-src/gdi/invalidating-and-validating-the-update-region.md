---
description: Um aplicativo invalida uma parte de uma janela e define a região de atualização usando a função InvalidateRect ou InvalidateRgn.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Invalidando e validando a região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba895875f9ec1350b6eb28ccb8f1721df6999ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967657"
---
# <a name="invalidating-and-validating-the-update-region"></a><span data-ttu-id="12889-103">Invalidando e validando a região de atualização</span><span class="sxs-lookup"><span data-stu-id="12889-103">Invalidating and Validating the Update Region</span></span>

<span data-ttu-id="12889-104">Um aplicativo invalida uma parte de uma janela e define a região de atualização usando a função [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) ou [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) .</span><span class="sxs-lookup"><span data-stu-id="12889-104">An application invalidates a portion of a window and sets the update region by using the [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function.</span></span> <span data-ttu-id="12889-105">Essas funções adicionam o retângulo ou a região especificada (em coordenadas do cliente) à região de atualização, combinando o retângulo ou a região com qualquer coisa que o sistema ou o aplicativo possa ter adicionado anteriormente à região de atualização.</span><span class="sxs-lookup"><span data-stu-id="12889-105">These functions add the specified rectangle or region (in client coordinates) to the update region, combining the rectangle or region with anything the system or the application may have previously added to the update region.</span></span>

<span data-ttu-id="12889-106">As funções [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) e [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) não geram mensagens do [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="12889-106">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) and [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) functions do not generate [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="12889-107">Em vez disso, o sistema acumula as alterações feitas por essas funções e suas próprias alterações enquanto uma janela processa outras mensagens em sua fila de mensagens.</span><span class="sxs-lookup"><span data-stu-id="12889-107">Instead, the system accumulates the changes made by these functions and its own changes while a window processes other messages in its message queue.</span></span> <span data-ttu-id="12889-108">Ao acumular alterações, uma janela processa todas as alterações de uma vez em vez de atualizar bits e partes uma etapa por vez.</span><span class="sxs-lookup"><span data-stu-id="12889-108">By accumulating changes, a window processes all changes at once instead of updating bits and pieces one step at a time.</span></span>

<span data-ttu-id="12889-109">As funções [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) e [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) validam uma parte da janela removendo um retângulo ou uma região especificada da região de atualização.</span><span class="sxs-lookup"><span data-stu-id="12889-109">The [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) and [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) functions validate a portion of the window by removing a specified rectangle or region from the update region.</span></span> <span data-ttu-id="12889-110">Essas funções normalmente são usadas quando a janela atualizou uma parte específica da tela na região de atualização antes de receber a mensagem de [**\_ pintura do WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="12889-110">These functions are typically used when the window has updated a specific part of the screen in the update region before receiving the [**WM\_PAINT**](wm-paint.md) message.</span></span>

 

 



