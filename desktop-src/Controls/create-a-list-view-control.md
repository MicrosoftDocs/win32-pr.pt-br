---
title: Como criar um controle List-View dados
description: Este tópico demonstra como criar um controle de exibição de lista. Para criar um controle de exibição de lista, use a função CreateWindow ou CreateWindowEx e especifique a classe de janela \_ LISTVIEW do WC.
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71eddfb60a2ea035a5afe62423289da40a47b61841d3ba58c4cafa2824a65b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826606"
---
# <a name="how-to-create-a-list-view-control"></a>Como criar um controle List-View dados

Este tópico demonstra como criar um controle de exibição de lista. Para criar um controle de exibição de lista, use a [**função CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especifique a classe de janela [**\_ LISTVIEW do WC.**](common-control-window-classes.md)

Um controle de exibição de lista também pode ser criado como parte de um modelo de caixa de diálogo. Você deve especificar [**WC \_ LISTVIEW**](common-control-window-classes.md) como o nome da classe. Para usar um controle de exibição de lista como parte de um modelo de caixa de diálogo, você deve chamar [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) ou [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) antes de criar uma instância da caixa de diálogo.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções


Primeiro, registre a classe de janela chamando a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e especificando o bit [**ICC \_ LISTVIEW \_ CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) na estrutura **INITCOMMONCONTROLSEX** que o acompanha. Isso garante que a DLL de controles comuns seja carregada. Em seguida, use [**a função CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especifique a classe de janela [**\_ LISTVIEW do WC.**](common-control-window-classes.md)

> [!Note]  
> Por padrão, um controle de exibição de lista usa a fonte de título do ícone. No entanto, você pode usar [**uma mensagem WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) para especificar a fonte a ser usada para o texto. Você deve enviar essa mensagem antes de inserir qualquer item. O controle usa as dimensões da fonte especificada pela mensagem **WM \_ SETFONT** para determinar o espaçamento e o layout. Você também pode personalizar a fonte para cada item. Para obter mais informações, consulte [Desenho personalizado.](custom-draw.md)

 

O exemplo de código C++ a seguir cria um controle de exibição de lista na exibição de relatório.


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




Normalmente, os aplicativos de exibição de lista permitem que o usuário altere de uma exibição para outra.

O exemplo de código C++ a seguir altera o estilo da janela da exibição de lista, que, por sua vez, altera a exibição.


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de exibição de lista](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Sobre List-View controles](list-view-controls-overview.md)
</dt> <dt>

[Usando List-View controles](using-list-view-controls.md)
</dt> </dl>

 

 