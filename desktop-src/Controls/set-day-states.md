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
# <a name="how-to-set-day-states"></a><span data-ttu-id="89825-104">Como definir Estados de dia</span><span class="sxs-lookup"><span data-stu-id="89825-104">How to Set Day States</span></span>

<span data-ttu-id="89825-105">Este tópico demonstra como definir informações de estado de dia.</span><span class="sxs-lookup"><span data-stu-id="89825-105">This topic demonstrates how to set day state information.</span></span> <span data-ttu-id="89825-106">O controle de calendário mensal usa informações de estado de dia para determinar como ele desenha dias específicos dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="89825-106">The month calendar control uses day state information to determine how it draws specific days within the control.</span></span>

<span data-ttu-id="89825-107">Os controles de calendário de mês que usam os Estados de dia de suporte do estilo [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="89825-107">Month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style support day states.</span></span> <span data-ttu-id="89825-108">As informações de estado do dia são expressas como um tipo de dados de 32 bits, [**MONTHDAYSTATE**](monthdaystate.md).</span><span class="sxs-lookup"><span data-stu-id="89825-108">Day state information is expressed as a 32-bit data type, [**MONTHDAYSTATE**](monthdaystate.md).</span></span> <span data-ttu-id="89825-109">Cada bit em um **MONTHDAYSTATE** de bits (0 a 30) especifica o estado de um dia em um mês.</span><span class="sxs-lookup"><span data-stu-id="89825-109">Each bit in a **MONTHDAYSTATE** bitfield (0 through 30) specifies the state of a day in a month.</span></span> <span data-ttu-id="89825-110">Se um bit for on, o dia correspondente será exibido em negrito.</span><span class="sxs-lookup"><span data-stu-id="89825-110">If a bit is on, the corresponding day is displayed in bold.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="89825-111">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="89825-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="89825-112">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="89825-112">Technologies</span></span>

-   [<span data-ttu-id="89825-113">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="89825-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="89825-114">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="89825-114">Prerequisites</span></span>

-   <span data-ttu-id="89825-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="89825-115">C/C++</span></span>
-   <span data-ttu-id="89825-116">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="89825-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="89825-117">Instruções</span><span class="sxs-lookup"><span data-stu-id="89825-117">Instructions</span></span>


<span data-ttu-id="89825-118">Um aplicativo pode definir explicitamente as informações de estado do dia enviando a mensagem [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) ou usando a macro correspondente, [**calendário mensal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span><span class="sxs-lookup"><span data-stu-id="89825-118">An application can explicitly set day state information by sending the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message or by using the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="89825-119">No entanto, as informações de estado de dia geralmente são definidas em resposta ao código de notificação [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , que é enviado sempre que o controle precisa ser atualizado porque, por exemplo, um mês diferente foi rolado para a exibição.</span><span class="sxs-lookup"><span data-stu-id="89825-119">However, day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed because, for example, a different month has scrolled into view.</span></span>

<span data-ttu-id="89825-120">O código de exemplo a seguir mostra como processar o código de notificação [MCN \_ GETDAYSTATE](mcn-getdaystate.md) em um manipulador de mensagens de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="89825-120">The following example code shows how to process the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code in a [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="89825-121">Ele processa MCN \_ GETDAYSTATE especificando que o primeiro e o décimo-quinto dia de cada mês visível devem ser realçados.</span><span class="sxs-lookup"><span data-stu-id="89825-121">It processes MCN\_GETDAYSTATE by specifying that the first and fifteenth day of each visible month should be highlighted.</span></span> <span data-ttu-id="89825-122">O membro **cDayState** da estrutura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) especifica o número de valores [**MONTHDAYSTATE**](monthdaystate.md) que são necessários na matriz, que recebe um tamanho máximo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="89825-122">The **cDayState** member of the [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure specifies the number of [**MONTHDAYSTATE**](monthdaystate.md) values that are needed in the array, which is given an arbitrary maximum size.</span></span> <span data-ttu-id="89825-123">Em seguida, o código executa um loop para definir os bits apropriados em cada elemento válido da matriz, usando a macro **BOLDDAY** definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="89825-123">The code then loops to set the appropriate bits in each valid element of the array, using the application-defined **BOLDDAY** macro.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="89825-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89825-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89825-125">Referência de controle de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="89825-125">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="89825-126">Sobre os controles de calendário mensal</span><span class="sxs-lookup"><span data-stu-id="89825-126">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="89825-127">Usando controles de calendário de mês</span><span class="sxs-lookup"><span data-stu-id="89825-127">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 




