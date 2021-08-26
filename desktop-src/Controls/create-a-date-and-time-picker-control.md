---
title: Como criar um controle de selador de data e hora
description: Este tópico demonstra como criar dinamicamente um controle DTP (selador de data e hora).
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa3f18e6033d3764e385280da383d74c351201694969266dcc383654a4372ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920886"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a>Como criar um controle de selador de data e hora

Este tópico demonstra como criar dinamicamente um controle DTP (selador de data e hora). O exemplo de código C++ que acompanha cria um controle DTP em uma caixa de diálogo sem modo. Ele usa o [**estilo DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) para permitir que o usuário simule a desativação da data dentro do controle .

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Registre a classe de janela chamando a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e especificando o bit ICC DATE CLASSES na estrutura \_ \_ [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que acompanha.


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a>Etapa 2:

Para criar o controle DTP, use a [**função CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) [**Especifique DATETIMEPICK \_ CLASS**](common-control-window-classes.md) como a classe de janela e passe o handle para a caixa de diálogo pai.

O exemplo de código C++ a seguir usa a [**função CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) para criar uma caixa de diálogo sem modo. Em seguida, ele **chama CreateWindowEx** para criar o controle DTP.


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

[Usando controles de selador de data e hora](using-date-and-time-picker.md)
</dt> <dt>

[Referência de controle do selador de data e hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selador de data e hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 