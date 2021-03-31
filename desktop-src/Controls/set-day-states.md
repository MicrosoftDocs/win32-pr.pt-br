---
title: Como definir Estados de dia
description: Este tópico demonstra como definir informações de estado de dia. O controle de calendário mensal usa informações de estado de dia para determinar como ele desenha dias específicos dentro do controle.
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa1fc105c94a15e1a658218013dca00129c883c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917820"
---
# <a name="how-to-set-day-states"></a>Como definir Estados de dia

Este tópico demonstra como definir informações de estado de dia. O controle de calendário mensal usa informações de estado de dia para determinar como ele desenha dias específicos dentro do controle.

Os controles de calendário de mês que usam os Estados de dia de suporte do estilo [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) . As informações de estado do dia são expressas como um tipo de dados de 32 bits, [**MONTHDAYSTATE**](monthdaystate.md). Cada bit em um **MONTHDAYSTATE** de bits (0 a 30) especifica o estado de um dia em um mês. Se um bit for on, o dia correspondente será exibido em negrito.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Um aplicativo pode definir explicitamente as informações de estado do dia enviando a mensagem [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) ou usando a macro correspondente, [**calendário mensal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). No entanto, as informações de estado de dia geralmente são definidas em resposta ao código de notificação [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , que é enviado sempre que o controle precisa ser atualizado porque, por exemplo, um mês diferente foi rolado para a exibição.

O código de exemplo a seguir mostra como processar o código de notificação [MCN \_ GETDAYSTATE](mcn-getdaystate.md) em um manipulador de mensagens de [**\_ notificação do WM**](wm-notify.md) . Ele processa MCN \_ GETDAYSTATE especificando que o primeiro e o décimo-quinto dia de cada mês visível devem ser realçados. O membro **cDayState** da estrutura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) especifica o número de valores [**MONTHDAYSTATE**](monthdaystate.md) que são necessários na matriz, que recebe um tamanho máximo arbitrário. Em seguida, o código executa um loop para definir os bits apropriados em cada elemento válido da matriz, usando a macro **BOLDDAY** definida pelo aplicativo.



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

[Sobre os controles de calendário mensal](month-calendar-controls.md)
</dt> <dt>

[Usando controles de calendário de mês](using-month-calendar-controls.md)
</dt> </dl>

 

 




