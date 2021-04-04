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
# <a name="using-visual-styles-with-custom-and-owner-drawn-controls"></a><span data-ttu-id="6a090-103">Usando estilos visuais com controles personalizados e Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="6a090-103">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>

<span data-ttu-id="6a090-104">Este tópico descreve como usar a API de estilos visuais para aplicar estilos visuais a controles personalizados ou controles desenhados pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="6a090-104">This topic describes how to use the visual styles API to apply visual styles to custom controls or owner-drawn controls.</span></span>

-   [<span data-ttu-id="6a090-105">Controles de desenho com estilos visuais</span><span class="sxs-lookup"><span data-stu-id="6a090-105">Drawing Controls with Visual Styles</span></span>](#drawing-controls-with-visual-styles)
-   [<span data-ttu-id="6a090-106">Respondendo a alterações de tema</span><span class="sxs-lookup"><span data-stu-id="6a090-106">Responding to Theme Changes</span></span>](#responding-to-theme-changes)
-   [<span data-ttu-id="6a090-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a090-107">Related topics</span></span>](#related-topics)

## <a name="drawing-controls-with-visual-styles"></a><span data-ttu-id="6a090-108">Controles de desenho com estilos visuais</span><span class="sxs-lookup"><span data-stu-id="6a090-108">Drawing Controls with Visual Styles</span></span>

<span data-ttu-id="6a090-109">Os estilos visuais têm suporte no ComCtrl32.dll versão 6 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="6a090-109">Visual styles are supported by ComCtrl32.dll version 6 and later.</span></span> <span data-ttu-id="6a090-110">Se seu aplicativo estiver configurado para usar ComCtrl32.dll versão 6 e posterior, e se essa versão estiver disponível no sistema, os estilos visuais atuais serão aplicados automaticamente a todos os controles comuns em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a090-110">If your application is configured to use ComCtrl32.dll version 6 and later, and if that version is available on the system, the current visual styles are automatically applied to all common controls in your application.</span></span> <span data-ttu-id="6a090-111">No entanto, os estilos visuais atuais não são aplicados automaticamente a controles personalizados ou a controles desenhados pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="6a090-111">However, the current visual styles are not automatically applied to custom controls or owner-drawn controls.</span></span> <span data-ttu-id="6a090-112">Seu aplicativo deve incluir o código que verifica se os estilos visuais estão disponíveis e, nesse caso, usa a API de estilos visuais para aplicar os estilos visuais selecionados no momento aos controles personalizados e desenhados pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="6a090-112">Your application must include code that checks whether visual styles are available and, if so, uses the visual styles API to apply the currently selected visual styles to your custom and owner-drawn controls.</span></span>

<span data-ttu-id="6a090-113">Para verificar se os estilos visuais estão disponíveis, chame a função [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) .</span><span class="sxs-lookup"><span data-stu-id="6a090-113">To check whether visual styles are available, call the [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) function.</span></span> <span data-ttu-id="6a090-114">Se os estilos visuais não estiverem disponíveis, use o código de fallback para desenhar o controle.</span><span class="sxs-lookup"><span data-stu-id="6a090-114">If visual styles are not available, use fallback code to draw the control.</span></span>

<span data-ttu-id="6a090-115">Se os estilos visuais estiverem disponíveis, você poderá usar funções de estilos visuais, como [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) , para renderizar seu controle.</span><span class="sxs-lookup"><span data-stu-id="6a090-115">If visual styles are available, you can use visual-styles functions such as [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) to render your control.</span></span> <span data-ttu-id="6a090-116">Observe que o [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) permite que você personalize a aparência do texto, retendo algumas propriedades da fonte do tema ao modificar outras.</span><span class="sxs-lookup"><span data-stu-id="6a090-116">Note that [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) enables you to customize the appearance of text, retaining some properties of the theme font while modifying others.</span></span>

<span data-ttu-id="6a090-117">**Para desenhar um controle no estilo visual atual**</span><span class="sxs-lookup"><span data-stu-id="6a090-117">**To draw a control in the current visual style**</span></span>

1.  <span data-ttu-id="6a090-118">Chame [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), passando o *HWND* do controle ao qual você deseja aplicar estilos visuais e uma lista de classes que descreve o tipo do controle.</span><span class="sxs-lookup"><span data-stu-id="6a090-118">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata), passing the *hwnd* of the control you want to apply visual styles to and a class list that describes the control's type.</span></span> <span data-ttu-id="6a090-119">As classes são definidas em Vssym32. h.</span><span class="sxs-lookup"><span data-stu-id="6a090-119">The classes are defined in Vssym32.h.</span></span> <span data-ttu-id="6a090-120">**OpenThemeData** retorna um identificador hTheme, mas se o Gerenciador de estilos visual estiver desabilitado ou o estilo visual atual não fornecer informações específicas para um determinado controle, a função retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6a090-120">**OpenThemeData** returns an HTHEME handle, but if the visual styles manager is disabled or the current visual style does not supply specific information for a given control, the function returns **NULL**.</span></span> <span data-ttu-id="6a090-121">Se o valor de retorno for **nulo**, use funções de desenho de estilos não visuais.</span><span class="sxs-lookup"><span data-stu-id="6a090-121">If the return value is **NULL**, use non-visual-styles drawing functions.</span></span>
2.  <span data-ttu-id="6a090-122">Para desenhar o plano de fundo do controle, chame [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) ou [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span><span class="sxs-lookup"><span data-stu-id="6a090-122">To draw the control background, call [**DrawThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackground) or [**DrawThemeBackgroundEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemebackgroundex).</span></span>
3.  <span data-ttu-id="6a090-123">Para determinar o local do retângulo de conteúdo, chame [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span><span class="sxs-lookup"><span data-stu-id="6a090-123">To determine the location of the content rectangle, call [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span>
4.  <span data-ttu-id="6a090-124">Para renderizar o texto, use [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) ou [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), baseando as coordenadas no retângulo retornado por [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span><span class="sxs-lookup"><span data-stu-id="6a090-124">To render text, use either [**DrawThemeText**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetext) or [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex), basing the coordinates on the rectangle returned by [**GetThemeBackgroundContentRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebackgroundcontentrect).</span></span> <span data-ttu-id="6a090-125">Essas funções podem renderizar texto na fonte do tema para uma parte de controle especificada e um estado, ou na fonte selecionada no momento no contexto do dispositivo (DC).</span><span class="sxs-lookup"><span data-stu-id="6a090-125">These functions can render text either in the theme's font for a specified control part and state, or in the font currently selected into the device context (DC).</span></span>
5.  <span data-ttu-id="6a090-126">Quando o controle receber uma mensagem do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) , chame [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) para liberar o identificador de tema que foi retornado quando você chamou [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span><span class="sxs-lookup"><span data-stu-id="6a090-126">When your control receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to release the theme handle that was returned when you called [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="6a090-127">O código de exemplo a seguir demonstra uma maneira de desenhar um controle de botão no estilo visual atual.</span><span class="sxs-lookup"><span data-stu-id="6a090-127">The following example code demonstrates one way to draw a button control in the current visual style.</span></span>


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





<span data-ttu-id="6a090-128">O código de exemplo a seguir está no manipulador de mensagens de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) para um controle de botão de subclasse.</span><span class="sxs-lookup"><span data-stu-id="6a090-128">The following example code is in the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message handler for a subclassed button control.</span></span> <span data-ttu-id="6a090-129">O texto do controle é desenhado na fonte de estilos visuais, mas a cor é definida pelo aplicativo dependendo do estado do controle.</span><span class="sxs-lookup"><span data-stu-id="6a090-129">The text for the control is drawn in the visual styles font, but the color is application-defined depending on the state of the control.</span></span>


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



<span data-ttu-id="6a090-130">Você pode usar partes de outros controles e renderizar cada parte separadamente.</span><span class="sxs-lookup"><span data-stu-id="6a090-130">You can use parts from other controls and render each part separately.</span></span> <span data-ttu-id="6a090-131">Por exemplo, para um controle de calendário que consiste em uma grade, você pode tratar cada quadrado formado pela grade como um botão da barra de ferramentas, obtendo o identificador de tema da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6a090-131">For example, for a calendar control that consists of a grid, you can treat each square formed by the grid as a toolbar button, by obtaining the theme handle as follows:</span></span>


```C++
OpenThemeData(hwnd, L"Toolbar");
```



<span data-ttu-id="6a090-132">Você pode misturar e combinar partes de controle chamando [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) várias vezes para um determinado controle e usando o identificador de tema apropriado para desenhar partes diferentes.</span><span class="sxs-lookup"><span data-stu-id="6a090-132">You can mix and match control parts by calling [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) multiple times for a given control and using the appropriate theme handle to draw different parts.</span></span> <span data-ttu-id="6a090-133">Em alguns estilos visuais, no entanto, determinadas partes podem não ser compatíveis com outras partes.</span><span class="sxs-lookup"><span data-stu-id="6a090-133">In some visual styles, however, certain parts might not be compatible with other parts.</span></span>

<span data-ttu-id="6a090-134">Outra abordagem para renderizar controles no estilo visual ativo é usar as cores do sistema.</span><span class="sxs-lookup"><span data-stu-id="6a090-134">Another approach to rendering controls in the active visual style is to use the system colors.</span></span> <span data-ttu-id="6a090-135">Por exemplo, você pode usar cores do sistema para definir a cor do texto ao chamar a função [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) .</span><span class="sxs-lookup"><span data-stu-id="6a090-135">For example, you can use system colors to set the text color when calling the [**DrawThemeTextEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemetextex) function.</span></span> <span data-ttu-id="6a090-136">A maioria das cores do sistema é definida quando um arquivo de estilo visual é aplicado.</span><span class="sxs-lookup"><span data-stu-id="6a090-136">Most system colors are set when a visual style file is applied.</span></span>

## <a name="responding-to-theme-changes"></a><span data-ttu-id="6a090-137">Respondendo a alterações de tema</span><span class="sxs-lookup"><span data-stu-id="6a090-137">Responding to Theme Changes</span></span>

<span data-ttu-id="6a090-138">Quando o controle recebe uma [**mensagem \_ themechanged do WM**](/windows/desktop/winmsg/wm-themechanged) e está mantendo um identificador global para o tema, ele deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6a090-138">When your control receives a [**WM\_THEMECHANGED**](/windows/desktop/winmsg/wm-themechanged) message and is holding a global handle to the theme, it should do the following:</span></span>

-   <span data-ttu-id="6a090-139">Chame [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) para fechar o identificador de tema existente.</span><span class="sxs-lookup"><span data-stu-id="6a090-139">Call [**CloseThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-closethemedata) to close the existing theme handle.</span></span>
-   <span data-ttu-id="6a090-140">Chame [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) para obter o identificador de tema para o estilo visual carregado recentemente.</span><span class="sxs-lookup"><span data-stu-id="6a090-140">Call [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) to get the theme handle to the newly loaded visual style.</span></span>

<span data-ttu-id="6a090-141">O exemplo a seguir ilustra as duas chamadas.</span><span class="sxs-lookup"><span data-stu-id="6a090-141">The following example illustrates the two calls.</span></span>


```C++
case WM_THEMECHANGED:
     CloseThemeData (g_hTheme);
     g_hTheme = OpenThemeData (hwnd, L"MyClassName");
```



## <a name="related-topics"></a><span data-ttu-id="6a090-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a090-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a090-143">Habilitar estilos visuais</span><span class="sxs-lookup"><span data-stu-id="6a090-143">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="6a090-144">Estilos visuais</span><span class="sxs-lookup"><span data-stu-id="6a090-144">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 