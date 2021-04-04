---
title: Usando estilos visuais com controles personalizados e Owner-Drawn
description: Este tópico descreve como usar a API de estilos visuais para aplicar estilos visuais a controles personalizados ou controles desenhados pelo proprietário.
ms.assetid: 8b06f9ce-702c-48f8-8cf3-2718a09b8d77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7025bdf7c589649ac62bed7a4ea4f55c418940
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084941"
---
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a>Usando estilos visuais com controles personalizados e Owner-Drawn

Este tópico descreve como usar a API de estilos visuais para aplicar estilos visuais a controles personalizados ou controles desenhados pelo proprietário.

-   [Controles de desenho com estilos visuais](#drawing-controls-with-visual-styles)
-   [Respondendo a alterações de tema](#responding-to-theme-changes)
-   [Tópicos relacionados](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a>Controles de desenho com estilos visuais

Os estilos visuais têm suporte no ComCtrl32.dll versão 6 e versões posteriores. Se seu aplicativo estiver configurado para usar ComCtrl32.dll versão 6 e posterior, e se essa versão estiver disponível no sistema, os estilos visuais atuais serão aplicados automaticamente a todos os controles comuns em seu aplicativo. No entanto, os estilos visuais atuais não são aplicados automaticamente a controles personalizados ou a controles desenhados pelo proprietário. Seu aplicativo deve incluir o código que verifica se os estilos visuais estão disponíveis e, nesse caso, usa a API de estilos visuais para aplicar os estilos visuais selecionados no momento aos controles personalizados e desenhados pelo proprietário.

Para verificar se os estilos visuais estão disponíveis, chame a função [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) . Se os estilos visuais não estiverem disponíveis, use o código de fallback para desenhar o controle.

Se os estilos visuais estiverem disponíveis, você poderá usar funções de estilos visuais, como [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) , para renderizar seu controle. Observe que o [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) permite que você personalize a aparência do texto, retendo algumas propriedades da fonte do tema ao modificar outras.

**Para desenhar um controle no estilo visual atual**

1.  Chame [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), passando o *HWND* do controle ao qual você deseja aplicar estilos visuais e uma lista de classes que descreve o tipo do controle. As classes são definidas em Vssym32. h. **OpenThemeData** retorna um identificador hTheme, mas se o Gerenciador de estilos visual estiver desabilitado ou o estilo visual atual não fornecer informações específicas para um determinado controle, a função retornará **NULL**. Se o valor de retorno for **nulo**, use funções de desenho de estilos não visuais.
2.  Para desenhar o plano de fundo do controle, chame [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) ou [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).
3.  Para determinar o local do retângulo de conteúdo, chame [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).
4.  Para renderizar o texto, use [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) ou [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), baseando as coordenadas no retângulo retornado por [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect). Essas funções podem renderizar texto na fonte do tema para uma parte de controle especificada e um estado, ou na fonte selecionada no momento no contexto do dispositivo (DC).
5.  Quando o controle receber uma mensagem do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , chame [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) para liberar o identificador de tema que foi retornado quando você chamou [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).

O código de exemplo a seguir demonstra uma maneira de desenhar um controle de botão no estilo visual atual.


```C++
HTHEME hTheme = NULL;

hTheme = OpenThemeData(hwndButton, L"Button");
// ...
DrawMyControl(hDC, hwndButton, hTheme, iState);
// ...
if (hTheme)
{
    CloseThemeData(hTheme);
}


void DrawMyControl(HDC hDC, HWND hwndButton, HTHEME hTheme, int iState)
{
    RECT rc, rcContent;
    TCHAR szButtonText[255];
    HRESULT hr;
    size_t cch;

    GetWindowRect(hwndButton, &rc);
    GetWindowText(hwndButton, szButtonText,
                  (sizeof(szButtonText) / sizeof(szButtonText[0])+1));
    hr = StringCchLength(szButtonText,
         (sizeof(szButtonText) / sizeof(szButtonText[0])), &cch);
    if (hTheme)
    {
        hr = DrawThemeBackground(hTheme, hDC, BP_PUSHBUTTON, iState, &rc, 0);
        if (SUCCEEDED(hr))
        {
            hr = GetThemeBackgroundContentRect(hTheme, hDC, BP_PUSHBUTTON, 
                    iState, &rc, &rcContent);
        }

        if (SUCCEEDED(hr))
        {
            hr = DrawThemeText(hTheme, hDC, BP_PUSHBUTTON, iState, 
                    szButtonText, cch,
                    DT_CENTER | DT_VCENTER | DT_SINGLELINE,
                    0, &rcContent);
        }

    }
    else
    {
        // Draw the control without using visual styles.
    }
}
```





O código de exemplo a seguir está no manipulador de mensagens de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) para um controle de botão de subclasse. O texto do controle é desenhado na fonte de estilos visuais, mas a cor é definida pelo aplicativo dependendo do estado do controle.


```C++
// textColor is a COLORREF whose value has been set according to whether the button is "hot".
// paint is the PAINTSTRUCT whose members are filled in by BeginPaint.
HTHEME theme = OpenThemeData(hWnd, L"button");
if (theme)
{
    DTTOPTS opts = { 0 };
    opts.dwSize = sizeof(opts);
    opts.crText = textColor;
    opts.dwFlags |= DTT_TEXTCOLOR;
    WCHAR caption[255];
    size_t cch;
    GetWindowText(hWnd, caption, 255);
    StringCchLength(caption, 255, &cch);
    DrawThemeTextEx(theme, paint.hdc, BP_PUSHBUTTON, CBS_UNCHECKEDNORMAL, 
        caption, cch, DT_CENTER | DT_VCENTER | DT_SINGLELINE, 
        &paint.rcPaint, &opts);
    CloseThemeData(theme);
}
else
{
    // Draw the control without using visual styles.
}
```



Você pode usar partes de outros controles e renderizar cada parte separadamente. Por exemplo, para um controle de calendário que consiste em uma grade, você pode tratar cada quadrado formado pela grade como um botão da barra de ferramentas, obtendo o identificador de tema da seguinte maneira:


```C++
OpenThemeData(hwnd, L"Toolbar");
```



Você pode misturar e combinar partes de controle chamando [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) várias vezes para um determinado controle e usando o identificador de tema apropriado para desenhar partes diferentes. Em alguns estilos visuais, no entanto, determinadas partes podem não ser compatíveis com outras partes.

Outra abordagem para renderizar controles no estilo visual ativo é usar as cores do sistema. Por exemplo, você pode usar cores do sistema para definir a cor do texto ao chamar a função [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) . A maioria das cores do sistema é definida quando um arquivo de estilo visual é aplicado.

## <a name="responding-to-theme-changes"></a>Respondendo a alterações de tema

Quando o controle recebe uma [**mensagem \_ themechanged do WM**](/windows/desktop/winmsg/wm-themechanged) e está mantendo um identificador global para o tema, ele deve fazer o seguinte:

-   Chame [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) para fechar o identificador de tema existente.
-   Chame [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) para obter o identificador de tema para o estilo visual carregado recentemente.

O exemplo a seguir ilustra as duas chamadas.


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitar estilos visuais](cookbook-overview.md)
</dt> <dt>

[Estilos visuais](themes-overview.md)
</dt> </dl>

 

 