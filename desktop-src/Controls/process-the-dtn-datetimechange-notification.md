---
title: Como processar a notificação de DTN_DATETIMECHANGE
description: Este tópico demonstra como processar a notificação de alterações, feitas pelo usuário, para o controle do seletor de data e hora (DTP).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434c7ebbda673f76a757375e9a3d23504483d42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917824"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a><span data-ttu-id="ccc54-103">Como processar a notificação DTN \_ DATETIMECHANGE</span><span class="sxs-lookup"><span data-stu-id="ccc54-103">How to Process the DTN\_DATETIMECHANGE Notification</span></span>

<span data-ttu-id="ccc54-104">Este tópico demonstra como processar a notificação de alterações, feitas pelo usuário, para o controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="ccc54-104">This topic demonstrates how to process notification of changes, made by the user, to the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ccc54-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="ccc54-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ccc54-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="ccc54-106">Technologies</span></span>

-   [<span data-ttu-id="ccc54-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="ccc54-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ccc54-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ccc54-108">Prerequisites</span></span>

-   <span data-ttu-id="ccc54-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="ccc54-109">C/C++</span></span>
-   <span data-ttu-id="ccc54-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="ccc54-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ccc54-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="ccc54-111">Instructions</span></span>


<span data-ttu-id="ccc54-112">Um controle DTP envia o código de notificação [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) sempre que ocorre uma alteração.</span><span class="sxs-lookup"><span data-stu-id="ccc54-112">A DTP control sends the [DTN\_DATETIMECHANGE](dtn-datetimechange.md) notification code whenever a change occurs.</span></span> <span data-ttu-id="ccc54-113">Por exemplo, essa notificação será gerada quando o usuário alterar um dos campos no controle ou, no caso em que o controle está definido como o estilo [**DTS \_ mynone**](date-and-time-picker-control-styles.md) , quando o usuário altera o estado da caixa de seleção do controle.</span><span class="sxs-lookup"><span data-stu-id="ccc54-113">For example, this notification will be generated when the user changes one of the fields in the control or, in the case where the control is set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style, when the user changes the state of the control's check box.</span></span>

<span data-ttu-id="ccc54-114">Seu aplicativo deve incluir código para processar \_ mensagens DTN DATETIMECHANGE enviadas pelo controle DTP.</span><span class="sxs-lookup"><span data-stu-id="ccc54-114">Your application must include code to process DTN\_DATETIMECHANGE messages that are sent by the DTP control.</span></span>

<span data-ttu-id="ccc54-115">O exemplo de código C++ a seguir é uma função definida pelo aplicativo projetada para indicar o estado de um controle DTP que é definido para o estilo **DTS \_ All None** .</span><span class="sxs-lookup"><span data-stu-id="ccc54-115">The following C++ code example is an application-defined function designed to indicate the state of a DTP control that is set to the **DTS\_SHOWNONE** style.</span></span>



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
}
```



## <a name="related-topics"></a><span data-ttu-id="ccc54-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ccc54-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccc54-117">Usando controles de seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="ccc54-117">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="ccc54-118">Referência de controle do seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="ccc54-118">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ccc54-119">Seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="ccc54-119">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




