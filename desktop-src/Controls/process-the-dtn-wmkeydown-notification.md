---
title: Como processar a notificação de DTN_WMKEYDOWN
description: Este tópico demonstra como processar uma notificação DTN \_ WMKEYDOWN. Manipular esse código de notificação permite que o proprietário do controle forneça respostas específicas para pressionamentos de teclas dentro dos campos de retorno de chamada do controle.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103824075"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a>Como processar a notificação DTN \_ WMKEYDOWN

Este tópico demonstra como processar uma notificação [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) . Manipular esse código de notificação permite que o proprietário do controle forneça respostas específicas para pressionamentos de teclas dentro dos campos de retorno de chamada do controle.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Os controles do seletor de data e hora (DTP) enviam a mensagem [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) para relatar que o usuário digitou entrada em um campo de retorno de chamada. Se você quiser emular as mesmas respostas de teclado com suporte para campos DTP padrão ou fornecer respostas personalizadas, seu aplicativo deverá incluir o código para lidar com essa notificação.

O exemplo de código C++ a seguir é uma função definida pelo aplicativo que processa a notificação [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) .

**Aviso de segurança:** O uso incorreto do **lstrcmp** pode comprometer a segurança do seu aplicativo. Por exemplo, antes de chamar **lstrcmp** no exemplo de código a seguir, você deve verificar se as duas cadeias de caracteres são terminadas em nulo. Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.



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

[Usando controles de seletor de data e hora](using-date-and-time-picker.md)
</dt> <dt>

[Referência de controle do seletor de data e hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Seletor de data e hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




