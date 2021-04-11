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
# <a name="how-to-create-a-date-and-time-picker-control"></a>Como criar um controle de seletor de data e hora

Este tópico demonstra como criar dinamicamente um controle DTP (data and time Picker). O exemplo de código C++ que o acompanha cria um controle DTP em uma caixa de diálogo sem janela restrita. Ele usa o estilo DTS não- [**\_ None**](date-and-time-picker-control-styles.md) para permitir que o usuário simule a desativação da data dentro do controle.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Registre a classe Window chamando a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e especificando o \_ bit classes de data de ICC \_ na estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que acompanha.


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a>Etapa 2:

Para criar o controle DTP, use a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . Especifique [**a \_ classe DATETIMEPICK**](common-control-window-classes.md) como a classe Window e passe o identificador para a caixa de diálogo pai.

O exemplo de código C++ a seguir usa a função [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) para criar uma caixa de diálogo sem janela restrita. Em seguida, ele chama **CreateWindowEx** para criar o controle DTP.


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



## <a name="complete-example"></a>Exemplo completo


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de seletor de data e hora](using-date-and-time-picker.md)
</dt> <dt>

[Referência de controle do seletor de data e hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Seletor de data e hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 