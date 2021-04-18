---
description: A subclasse é uma técnica que permite que um aplicativo intercepte e processe mensagens enviadas ou postadas em uma janela específica antes que um procedimento de janela tenha a oportunidade de processá-las.
ms.assetid: 6f7ee9ff-479d-4cb0-8de1-1c3b671551f9
title: Subclasse e tradução automática de mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7f0aebabe4bde259a982152327ce61a14de915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758136"
---
# <a name="subclassing-and-automatic-message-translation"></a><span data-ttu-id="02af0-103">Subclasse e tradução automática de mensagens</span><span class="sxs-lookup"><span data-stu-id="02af0-103">Subclassing and Automatic Message Translation</span></span>

<span data-ttu-id="02af0-104">A subclasse é uma técnica que permite que um aplicativo intercepte e processe mensagens enviadas ou postadas em uma janela específica antes que um procedimento de janela tenha a oportunidade de processá-las.</span><span class="sxs-lookup"><span data-stu-id="02af0-104">Subclassing is a technique that allows an application to intercept and process messages sent or posted to a particular window before a window procedure has a chance to process them.</span></span> <span data-ttu-id="02af0-105">O sistema operacional converte automaticamente as mensagens na [página de código do Windows (ANSI)](code-pages.md) ou no formato [Unicode](unicode.md) , dependendo do formulário da função que tem uma subclasse do procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="02af0-105">The operating system automatically translates messages into [Windows (ANSI) code page](code-pages.md) or [Unicode](unicode.md) form, depending on the form of the function that has subclassed the window procedure.</span></span>

<span data-ttu-id="02af0-106">A seguinte chamada para a função [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) subclasses o procedimento de janela atual associado à janela identificada pelo parâmetro *HWND* .</span><span class="sxs-lookup"><span data-stu-id="02af0-106">The following call to the [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function subclasses the current window procedure associated with the window identified by the *hWnd* parameter.</span></span> <span data-ttu-id="02af0-107">Como alternativa, um aplicativo pode usar [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span><span class="sxs-lookup"><span data-stu-id="02af0-107">Alternatively, an application can use [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra).</span></span> <span data-ttu-id="02af0-108">O novo procedimento de janela **NewWndProc** receberá mensagens com texto no formato de página de código do Windows.</span><span class="sxs-lookup"><span data-stu-id="02af0-108">The new window procedure **NewWndProc**, will receive messages with text in Windows code page format.</span></span>


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



<span data-ttu-id="02af0-109">Quando o **NewWndProc** conclui o processamento de uma mensagem, ele usa a função [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) da seguinte maneira para passar a mensagem para **OldWndProc**.</span><span class="sxs-lookup"><span data-stu-id="02af0-109">When **NewWndProc** has finished processing a message, it uses the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function as follows to pass the message to **OldWndProc**.</span></span>


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



<span data-ttu-id="02af0-110">Se **OldWndProc** tiver sido criado com um estilo de classe de Unicode, as mensagens serão convertidas do formulário de página de código do Windows recebido por **NewWndProc** em Unicode.</span><span class="sxs-lookup"><span data-stu-id="02af0-110">If **OldWndProc** was created with a class style of UNICODE, messages are translated from the Windows code page form received by **NewWndProc** into Unicode.</span></span>

<span data-ttu-id="02af0-111">Da mesma forma, uma chamada para a função [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ou [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) subclasses o procedimento de janela atual com um procedimento de janela que espera mensagens de texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="02af0-111">Similarly, a call to the [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function subclasses the current window procedure with a window procedure that expects Unicode text messages.</span></span> <span data-ttu-id="02af0-112">A conversão de mensagens, se necessário, é executada durante o processamento da função [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="02af0-112">Message translation, if necessary, is performed during the processing of the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function.</span></span>

<span data-ttu-id="02af0-113">Para obter mais informações sobre subclasses, consulte [procedimentos de janela](../winmsg/window-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="02af0-113">For more information about subclassing, see [Window Procedures](../winmsg/window-procedures.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02af0-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02af0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02af0-115">Usando Unicode e conjuntos de caracteres</span><span class="sxs-lookup"><span data-stu-id="02af0-115">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
