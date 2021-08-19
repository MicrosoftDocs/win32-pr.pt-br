---
title: Como definir estados de dia
description: Este tópico demonstra como definir informações de estado de dia. O controle de calendário do mês usa informações de estado de dia para determinar como ele desenha dias específicos dentro do controle .
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3ed2c99e6faf18f0e1d06ec06eaaf9a0d573faebe6f3697e43562603447571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078470"
---
# <a name="how-to-set-day-states"></a>Como definir estados de dia

Este tópico demonstra como definir informações de estado de dia. O controle de calendário do mês usa informações de estado de dia para determinar como ele desenha dias específicos dentro do controle .

Controles de calendário de mês que usam os estados de dia de suporte no estilo [**\_ DAYSTATE do MCS.**](month-calendar-control-styles.md) As informações de estado de dia são expressas como um tipo de dados de 32 bits, [**MONTHDAYSTATE.**](monthdaystate.md) Cada bit em um campo de bits **MONTHDAYSTATE** (0 a 30) especifica o estado de um dia em um mês. Se um bit estiver on, o dia correspondente será exibido em negrito.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções


Um aplicativo pode definir explicitamente informações de estado de dia enviando a mensagem [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) ou usando a macro correspondente, [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). No entanto, as informações de estado de dia geralmente são definidas em resposta ao código de notificação [ \_ MCN GETDAYSTATE,](mcn-getdaystate.md) que é enviado sempre que o controle precisa ser atualizado porque, por exemplo, um mês diferente foi rolado para a exibição.

O código de exemplo a seguir mostra como processar o código de notificação [ \_ MCN GETDAYSTATE](mcn-getdaystate.md) em um manipulador [**de mensagens WM \_ NOTIFY.**](wm-notify.md) Ele processa MCN GETDAYSTATE especificando que o primeiro e o décimo \_ quinto dia de cada mês visível devem ser realçadas. O **membro cDayState** da estrutura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) especifica o número de valores [**MONTHDAYSTATE**](monthdaystate.md) necessários na matriz, que recebe um tamanho máximo arbitrário. Em seguida, o código é loop para definir os bits apropriados em cada elemento válido da matriz, usando a macro **BOLDDAY** definida pelo aplicativo.



```C++
    #define BOLDDAY(ds, iDay)  \
        if (iDay > 0 && iDay < 32)(ds) |= (0x00000001 << (iDay - 1))

    case WM_NOTIFY:
            if (((LPNMHDR)lParam)->code == MCN_GETDAYSTATE)
            {
                MONTHDAYSTATE rgMonths[12] = { 0 };
                int cMonths = ((NMDAYSTATE*)lParam)->cDayState;
                for (int i = 0; i < cMonths; i++)
                {
                    BOLDDAY(rgMonths[i], 1);
                    BOLDDAY(rgMonths[i], 15);
                }
                ((NMDAYSTATE*)lParam)->prgDayState = rgMonths;
                return TRUE;
            }
            break;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de calendário mensal](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Sobre controles de calendário de mês](month-calendar-controls.md)
</dt> <dt>

[Usando controles de calendário de mês](using-month-calendar-controls.md)
</dt> </dl>

 

 




