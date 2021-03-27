---
description: O sistema altera o tamanho de uma janela quando o usuário escolhe comandos de menu da janela, como tamanho e maximizar, ou quando o aplicativo chama funções, como a função SetWindowPos.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Janelas redimensionadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f740191f8b85038f17a687ebc547305f882383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827643"
---
# <a name="resized-windows"></a><span data-ttu-id="0bb88-103">Janelas redimensionadas</span><span class="sxs-lookup"><span data-stu-id="0bb88-103">Resized Windows</span></span>

<span data-ttu-id="0bb88-104">O sistema altera o tamanho de uma janela quando o usuário escolhe comandos de menu da janela, como tamanho e maximizar, ou quando o aplicativo chama funções, como a função [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) .</span><span class="sxs-lookup"><span data-stu-id="0bb88-104">The system changes the size of a window when the user chooses window menu commands, such as Size and Maximize, or when the application calls functions, such as the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function.</span></span> <span data-ttu-id="0bb88-105">Quando uma janela muda de tamanho, o sistema assume que o conteúdo da parte exposta anteriormente da janela não é afetado e não precisa ser redesenhado.</span><span class="sxs-lookup"><span data-stu-id="0bb88-105">When a window changes size, the system assumes that the contents of the previously exposed portion of the window are not affected and need not be redrawn.</span></span> <span data-ttu-id="0bb88-106">O sistema invalida apenas a parte recentemente exposta da janela, o que poupa tempo quando a mensagem eventual de [**\_ pintura do WM**](wm-paint.md) é processada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0bb88-106">The system invalidates only the newly exposed portion of the window, which saves time when the eventual [**WM\_PAINT**](wm-paint.md) message is processed by the application.</span></span> <span data-ttu-id="0bb88-107">Nesse caso, o **WM \_ Paint** não é gerado quando o tamanho da janela é reduzido.</span><span class="sxs-lookup"><span data-stu-id="0bb88-107">In this case, **WM\_PAINT** is not generated when the size of the window is reduced.</span></span>

<span data-ttu-id="0bb88-108">Para algumas janelas, qualquer alteração no tamanho da janela invalida o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0bb88-108">For some windows, any change to the size of the window invalidates the contents.</span></span> <span data-ttu-id="0bb88-109">Por exemplo, um aplicativo de relógio que adapte a face do relógio para se ajustar perfeitamente dentro de sua janela deve redesenhar o relógio sempre que a janela mudar de tamanho.</span><span class="sxs-lookup"><span data-stu-id="0bb88-109">For example, a clock application that adapts the face of the clock to fit neatly within its window must redraw the clock whenever the window changes size.</span></span> <span data-ttu-id="0bb88-110">Para forçar o sistema a invalidar toda a área do cliente da janela quando uma alteração vertical, horizontal ou vertical e horizontal for feita, um aplicativo deverá especificar o \_ estilo cs VREDRAW ou cs \_ HREDRAW, ou ambos, ao registrar a classe Window.</span><span class="sxs-lookup"><span data-stu-id="0bb88-110">To force the system to invalidate the entire client area of the window when a vertical, horizontal, or both vertical and horizontal change is made, an application must specify the CS\_VREDRAW or CS\_HREDRAW style, or both, when registering the window class.</span></span> <span data-ttu-id="0bb88-111">Qualquer janela pertencente a uma classe de janela que tenha esses estilos é invalidada sempre que o usuário ou o aplicativo altera o tamanho da janela.</span><span class="sxs-lookup"><span data-stu-id="0bb88-111">Any window belonging to a window class having these styles is invalidated each time the user or the application changes the size of the window.</span></span>

 

 
