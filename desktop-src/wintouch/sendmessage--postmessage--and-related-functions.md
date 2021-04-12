---
title: SendMessage, mensagem de mensagens e funções relacionadas
description: Esta seção descreve as considerações sobre o encaminhamento de mensagens usando SendMessage, CreateMessage e funções relacionadas com mensagens de toque.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fc42e31f3c971c704d18f04a961fb6bd40eb91d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366335"
---
# <a name="sendmessage-postmessage-and-related-functions"></a>SendMessage, mensagem de mensagens e funções relacionadas

Esta seção descreve as considerações sobre o encaminhamento de mensagens usando [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [CreateMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)e funções relacionadas com mensagens de toque.

Se uma mensagem de toque for encaminhada usando [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [CreateMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)ou alguma outra função relacionada, o identificador de entrada por toque será fechado. Se você tiver recuperado as informações contidas referenciadas por um identificador de entrada por toque por meio de uma chamada para [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), esses dados permanecerão válidos até que você libere a memória.

Um aplicativo que recebe mensagens de toque encaminhadas por meio de um desses mecanismos possui o identificador de entrada por toque que recebe na mensagem *lParam* e é responsável por fechá-la. Se você não fechar o identificador com uma chamada para [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), passar a mensagem para [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)ou encaminhar a mensagem usando [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [mensagem](/windows/win32/api/winuser/nf-winuser-postmessagea)posterior ou alguma função relacionada, você terá um vazamento de memória.

> [!Note]  
> As mensagens de toque estão sujeitas às regras normais de UIPI (isolamento de privilégio de interface do usuário) quando elas são encaminhadas.

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a>Funções relacionadas a SendMessage e a mensagem

As funções a seguir podem afetar o estado do identificador de entrada por toque.

-   [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   SendNotifyMessage
-   SendMessageCallback
-   SendMessageTimeout
-   PostThreadMessage

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções](mtfunctions.md)
</dt> <dt>

[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 