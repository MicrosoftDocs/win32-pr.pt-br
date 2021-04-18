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
# <a name="subclassing-and-automatic-message-translation"></a>Subclasse e tradução automática de mensagens

A subclasse é uma técnica que permite que um aplicativo intercepte e processe mensagens enviadas ou postadas em uma janela específica antes que um procedimento de janela tenha a oportunidade de processá-las. O sistema operacional converte automaticamente as mensagens na [página de código do Windows (ANSI)](code-pages.md) ou no formato [Unicode](unicode.md) , dependendo do formulário da função que tem uma subclasse do procedimento de janela.

A seguinte chamada para a função [**SetWindowLongA**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) subclasses o procedimento de janela atual associado à janela identificada pelo parâmetro *HWND* . Como alternativa, um aplicativo pode usar [**SetWindowLongPtrA**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra). O novo procedimento de janela **NewWndProc** receberá mensagens com texto no formato de página de código do Windows.


```C++
OldWndProc = (WNDPROC) SetWindowLongA(hWnd,
             GWL_WNDPROC, (LONG)NewWndProc); 
```



Quando o **NewWndProc** conclui o processamento de uma mensagem, ele usa a função [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) da seguinte maneira para passar a mensagem para **OldWndProc**.


```C++
CallWindowProc(OldWndProc, hWnd, uMessage, wParam, lParam);
```



Se **OldWndProc** tiver sido criado com um estilo de classe de Unicode, as mensagens serão convertidas do formulário de página de código do Windows recebido por **NewWndProc** em Unicode.

Da mesma forma, uma chamada para a função [**SetWindowLongW**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ou [**SetWindowLongPtrW**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) subclasses o procedimento de janela atual com um procedimento de janela que espera mensagens de texto Unicode. A conversão de mensagens, se necessário, é executada durante o processamento da função [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) .

Para obter mais informações sobre subclasses, consulte [procedimentos de janela](../winmsg/window-procedures.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando Unicode e conjuntos de caracteres](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
