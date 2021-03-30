---
title: Como criar um controle de calendário mensal
description: Este tópico demonstra como criar dinamicamente um controle de calendário mensal usando a função CreateWindowEx.
ms.assetid: 35ADDA85-5D7D-46F4-A637-99FEE4592B3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f3824618e9801b68eb67b13c64c638a5057481
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103643003"
---
# <a name="how-to-create-a-month-calendar-control"></a>Como criar um controle de calendário mensal

Este tópico demonstra como criar dinamicamente um controle de calendário mensal usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Para criar um controle de calendário mensal, use a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a [**\_ classe calendário mensal**](common-control-window-classes.md) como a classe de janela. Você deve primeiro registrar a classe de janela chamando a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , especificando o bit das **\_ \_ classes de data ICC** na estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que acompanha.

O exemplo a seguir demonstra como criar um controle de calendário de mês em uma caixa de diálogo sem janela restrita existente. Observe que os valores de tamanho passados para [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) são todos zeros. Como o tamanho mínimo necessário depende da fonte usada pelo controle, o exemplo usa a macro [**calendário mensal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) para solicitar informações de tamanho e, em seguida, redimensiona o controle chamando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Se você alterar posteriormente a fonte com o [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont), as dimensões do controle não serão alteradas. Você deve chamar **calendário mensal \_ GetMinReqRect** novamente e redimensionar o controle para se ajustar à nova fonte.



```C++
// Child window identifier of the month calendar.
#define IDC_MONTHCAL 101

// Symbols used by SetWindowPos function (arbitrary values).
#define LEFT 35
#define TOP  40

// Description:
//   Creates a month calendar control in a dialog box.  
// Parameters:
//   hwndOwner - handle of the owner window.
// Nonlocal variables:
//   MonthCalDlgProc - window procedure of the dialog box that 
//     contains the month calendar.
//   g_hInst - global instance handle.
//
HRESULT CreateMonthCalDialog(HWND hwndOwner)
{
    RECT rc;
    INITCOMMONCONTROLSEX icex;
    HWND hwndDlg = NULL;
    HWND hwndMonthCal = NULL;

    // Return an error code if the owner handle is invalid.
    if (hwndOwner == NULL)
        return E_INVALIDARG;

    // Load the window class.
    icex.dwSize = sizeof(icex);
    icex.dwICC  = ICC_DATE_CLASSES;
    InitCommonControlsEx(&icex);

    // Create a modeless dialog box to hold the control.
    hwndDlg = CreateDialog(g_hInst,
                    MAKEINTRESOURCE(IDD_DATE_PICKER),
                    hwndOwner,
                    MonthCalDlgProc);
   
    // Return if creating the dialog box failed. 
    if (hwndDlg == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                        
    // Create the month calendar.
    hwndMonthCal  = CreateWindowEx(0,
                    MONTHCAL_CLASS,
                    L"",
                    WS_BORDER | WS_CHILD | WS_VISIBLE | MCS_DAYSTATE,
                    0,0,0,0, // resize it later
                    hwndDlg,
                    (HMENU) IDC_MONTHCAL,
                    g_hInst,
                    NULL);

    // Return if creating the month calendar failed. 
    if (hwndMonthCal == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                     
    // Get the size required to show an entire month.
    MonthCal_GetMinReqRect(hwndMonthCal, &rc);

    // Resize the control now that the size values have been obtained.
    SetWindowPos(hwndMonthCal, NULL, LEFT, TOP, 
        rc.right, rc.bottom, SWP_NOZORDER);

    // Set the calendar to the annual view.
    MonthCal_SetCurrentView(hwndMonthCal, MCMV_YEAR);

    // Make the window visible.
    ShowWindow(hwndDlg, SW_SHOW);

    return S_OK;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de calendário mensal](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Sobre os controles de calendário mensal](month-calendar-controls.md)
</dt> <dt>

[Usando controles de calendário de mês](using-month-calendar-controls.md)
</dt> </dl>

 

 