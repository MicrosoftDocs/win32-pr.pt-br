---
title: Como processar a notificação DTN_WMKEYDOWN dados
description: Este tópico demonstra como processar uma notificação \_ WMKEYDOWN de DTN. Lidar com esse código de notificação permite que o proprietário do controle forneça respostas específicas a teclas nos campos de retorno de chamada do controle.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbef0804afb388f9cadad60b04bf93ce4730ef255476f0c7f216edfd24846a19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540346"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a>Como processar a notificação wmkeydown de DTN \_

Este tópico demonstra como processar uma notificação [ \_ WMKEYDOWN de DTN.](dtn-wmkeydown.md) Lidar com esse código de notificação permite que o proprietário do controle forneça respostas específicas a teclas nos campos de retorno de chamada do controle.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções


Os controles DTP (selador de data e hora) enviam a mensagem [ \_ WMKEYDOWN do DTN](dtn-wmkeydown.md) para relatar que o usuário digitou a entrada em um campo de retorno de chamada. Se você quiser emular as mesmas respostas de teclado com suporte para campos DTP padrão ou fornecer respostas personalizadas, seu aplicativo deverá incluir código para lidar com essa notificação.

O exemplo de código C++ a seguir é uma função definida pelo aplicativo que processa a notificação [ \_ WMKEYDOWN do DTN.](dtn-wmkeydown.md)

**Aviso de segurança:** Usar **lstrcmp** incorretamente pode comprometer a segurança do seu aplicativo. Por exemplo, antes de chamar **lstrcmp** no exemplo de código a seguir, você deve garantir que as duas cadeias de caracteres sejam terminadas em nulo. Você deve revisar [considerações de segurança: Controles Windows Microsoft antes](sec-comctls.md) de continuar.



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de selador de data e hora](using-date-and-time-picker.md)
</dt> <dt>

[Referência de controle do selador de data e hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selador de data e hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




