---
title: Como criar um controle de seletor de data e hora
description: Este tópico demonstra como criar dinamicamente um controle DTP (data and time Picker).
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1253a2972b8d858a7440b3e472d5b3aa347b8175
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104162411"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a><span data-ttu-id="b08ae-103">Como criar um controle de seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="b08ae-103">How to Create a Date and Time Picker Control</span></span>

<span data-ttu-id="b08ae-104">Este tópico demonstra como criar dinamicamente um controle DTP (data and time Picker).</span><span class="sxs-lookup"><span data-stu-id="b08ae-104">This topic demonstrates how to dynamically create a date and time picker (DTP) control.</span></span> <span data-ttu-id="b08ae-105">O exemplo de código C++ que o acompanha cria um controle DTP em uma caixa de diálogo sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="b08ae-105">The accompanying C++ code example creates a DTP control in a modeless dialog box.</span></span> <span data-ttu-id="b08ae-106">Ele usa o estilo DTS não- [**\_ None**](date-and-time-picker-control-styles.md) para permitir que o usuário simule a desativação da data dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="b08ae-106">It uses the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style to enable the user to simulate deactivation of the date within the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b08ae-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="b08ae-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b08ae-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="b08ae-108">Technologies</span></span>

-   [<span data-ttu-id="b08ae-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="b08ae-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b08ae-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="b08ae-110">Prerequisites</span></span>

-   <span data-ttu-id="b08ae-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="b08ae-111">C/C++</span></span>
-   <span data-ttu-id="b08ae-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="b08ae-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b08ae-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="b08ae-113">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="b08ae-114">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="b08ae-114">Step 1:</span></span>

<span data-ttu-id="b08ae-115">Registre a classe Window chamando a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e especificando o \_ bit classes de data de ICC \_ na estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que acompanha.</span><span class="sxs-lookup"><span data-stu-id="b08ae-115">Register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the ICC\_DATE\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a><span data-ttu-id="b08ae-116">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="b08ae-116">Step 2:</span></span>

<span data-ttu-id="b08ae-117">Para criar o controle DTP, use a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="b08ae-117">To create the DTP control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="b08ae-118">Especifique [**a \_ classe DATETIMEPICK**](common-control-window-classes.md) como a classe Window e passe o identificador para a caixa de diálogo pai.</span><span class="sxs-lookup"><span data-stu-id="b08ae-118">Specify [**DATETIMEPICK\_CLASS**](common-control-window-classes.md) as the window class, and pass the handle to the parent dialog box.</span></span>

<span data-ttu-id="b08ae-119">O exemplo de código C++ a seguir usa a função [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) para criar uma caixa de diálogo sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="b08ae-119">The following C++ code example uses the [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) function to create a modeless dialog box.</span></span> <span data-ttu-id="b08ae-120">Em seguida, ele chama **CreateWindowEx** para criar o controle DTP.</span><span class="sxs-lookup"><span data-stu-id="b08ae-120">It then calls **CreateWindowEx** to create the DTP control.</span></span>


```C++
  hwndDlg = CreateDialog  (g_hinst,
                           MAKEINTRESOURCE(IDD_DIALOG1),
                           hwndMain,
                           DlgProc);

  if(hwndDlg)
      hwndDP = CreateWindowEx(0,
                           DATETIMEPICK_CLASS,
                           TEXT("DateTime"),
                           WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                           20,50,220,20,
                           hwndDlg,
                           NULL,
                           g_hinst,
                           NULL);
```



## <a name="complete-example"></a><span data-ttu-id="b08ae-121">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="b08ae-121">Complete example</span></span>


```C++
//  CreateDatePick creates a DTP control within a dialog box.
//  Returns the handle to the new DTP control if successful, or NULL 
//  otherwise.
// 
//    hwndMain - The handle to the main window.
//    g_hinst  - global handle to the program instance.

HWND WINAPI CreateDatePick(HWND hwndMain)
{
    HWND hwndDP = NULL;
    HWND hwndDlg = NULL;

    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(icex);
    icex.dwICC = ICC_DATE_CLASSES;

    InitCommonControlsEx(&icex);

    hwndDlg = CreateDialog  (g_hinst,
                             MAKEINTRESOURCE(IDD_DIALOG1),
                             hwndMain,
                             DlgProc);

    if(hwndDlg)
        hwndDP = CreateWindowEx(0,
                             DATETIMEPICK_CLASS,
                             TEXT("DateTime"),
                             WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                             20,50,220,20,
                             hwndDlg,
                             NULL,
                             g_hinst,
                             NULL);

    return (hwndDP);
}

```



## <a name="related-topics"></a><span data-ttu-id="b08ae-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b08ae-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b08ae-123">Usando controles de seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="b08ae-123">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="b08ae-124">Referência de controle do seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="b08ae-124">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b08ae-125">Seletor de data e hora</span><span class="sxs-lookup"><span data-stu-id="b08ae-125">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 