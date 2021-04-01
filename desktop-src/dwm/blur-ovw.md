---
title: Desfoque do DWM por trás da visão geral
description: Um dos efeitos de Gerenciador de Janelas da Área de Trabalho de assinatura (DWM) é uma área de não-cliente translúcida e borrada. As APIs do DWM permitem que os aplicativos apliquem esses efeitos à área do cliente de suas janelas de nível superior.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), efeito desfoque-atrás
- DWM (Gerenciador de Janelas da Área de Trabalho), efeito desfoque-atrás
- efeito borrar-atrás
- efeito translúcida
- efeito de vidro transparente
- Gerenciador de Janelas da Área de Trabalho (DWM), efeito translúcida
- DWM (Gerenciador de Janelas da Área de Trabalho), efeito translúcida
- Gerenciador de Janelas da Área de Trabalho (DWM), efeito de vidro transparente
- DWM (Gerenciador de Janelas da Área de Trabalho), efeito de vidro transparente
- Gerenciador de Janelas da Área de Trabalho (DWM), estendendo o quadro da janela na área do cliente
- DWM (Gerenciador de Janelas da Área de Trabalho), estendendo o quadro de janela na área do cliente
- estendendo o quadro da janela na área do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf7378cfcaff93aa9a54ce399890ec1bfd8cc1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008063"
---
# <a name="dwm-blur-behind-overview"></a><span data-ttu-id="9a9cc-116">Desfoque do DWM por trás da visão geral</span><span class="sxs-lookup"><span data-stu-id="9a9cc-116">DWM Blur Behind Overview</span></span>

<span data-ttu-id="9a9cc-117">Um dos efeitos de Gerenciador de Janelas da Área de Trabalho de assinatura (DWM) é uma área de não-cliente translúcida e borrada.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-117">One of the signature Desktop Window Manager (DWM) effects is a translucent and blurred non-client area.</span></span> <span data-ttu-id="9a9cc-118">As APIs do DWM permitem que os aplicativos apliquem esses efeitos à área do cliente de suas janelas de nível superior.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-118">The DWM APIs enable applications to apply these effects to the client area of their top-level windows.</span></span>

> [!Note]  
> <span data-ttu-id="9a9cc-119">O Windows Vista Home Basic Edition não dá suporte ao efeito de vidro transparente.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-119">Windows Vista Home Basic edition does not support the transparent glass effect.</span></span> <span data-ttu-id="9a9cc-120">As áreas que normalmente renderizariam com o efeito de vidro transparente em outras edições do Windows são renderizadas como opacas.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-120">Areas that would typically render with the transparent glass effect on other Windows editions are rendered as opaque.</span></span>
> <span data-ttu-id="9a9cc-121">A partir do Windows 8, chamar essa função não resulta no efeito de desfoque, devido a uma alteração de estilo na maneira como as janelas são renderizadas.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-121">Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>


 

<span data-ttu-id="9a9cc-122">Este tópico discute os seguintes cenários de desfoque do cliente que o DWM habilita.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-122">This topic discusses the following client blur-behind scenarios that the DWM enables.</span></span>

-   [<span data-ttu-id="9a9cc-123">Adicionando desfoque a uma região específica da área do cliente</span><span class="sxs-lookup"><span data-stu-id="9a9cc-123">Adding Blur to a Specific Region of the Client Area</span></span>](#adding-blur-to-a-specific-region-of-the-client-area)
-   [<span data-ttu-id="9a9cc-124">Estendendo o quadro da janela para a área do cliente</span><span class="sxs-lookup"><span data-stu-id="9a9cc-124">Extending the Window Frame into the Client Area</span></span>](#extending-the-window-frame-into-the-client-area)
-   [<span data-ttu-id="9a9cc-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a9cc-125">Related topics</span></span>](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a><span data-ttu-id="9a9cc-126">Adicionando desfoque a uma região específica da área do cliente</span><span class="sxs-lookup"><span data-stu-id="9a9cc-126">Adding Blur to a Specific Region of the Client Area</span></span>

<span data-ttu-id="9a9cc-127">Um aplicativo pode aplicar o efeito de desfoque atrás de toda a região do cliente da janela ou de uma sub-região específica.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-127">An application can apply the blur effect behind the whole client region of the window or to a specific subregion.</span></span> <span data-ttu-id="9a9cc-128">Isso permite que os aplicativos adicionem um caminho com estilo e barras de pesquisa que são visualmente separadas do restante do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-128">This enables applications to add styled path and search bars that are visually separate from the rest of the application.</span></span>

<span data-ttu-id="9a9cc-129">A API usada neste cenário é a função [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) , que usa o [**DWM Blur por trás das constantes**](dwm-bb-constants.md) e a estrutura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) .</span><span class="sxs-lookup"><span data-stu-id="9a9cc-129">The API used in this scenario is the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function, which makes use of the [**DWM Blur Behind Constants**](dwm-bb-constants.md) and the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure.</span></span>

<span data-ttu-id="9a9cc-130">A função de exemplo a seguir, `EnableBlurBehind` , ilustra como aplicar o efeito desfoque-atrás à janela inteira.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-130">The following example function, `EnableBlurBehind`, illustrates how to apply the blur-behind effect to the whole window.</span></span>


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="9a9cc-131">Observe que **NULL** é especificado no parâmetro *hRgnBlur* .</span><span class="sxs-lookup"><span data-stu-id="9a9cc-131">Note that **NULL** is specified in the *hRgnBlur* parameter.</span></span> <span data-ttu-id="9a9cc-132">Isso informa ao DWM para aplicar o desfoque por trás de toda a janela.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-132">This tells the DWM to apply the blur behind the whole window.</span></span>

<span data-ttu-id="9a9cc-133">A imagem a seguir ilustra o efeito desfoque-atrás aplicado à janela inteira.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-133">The following image illustrates the blur-behind effect applied to the whole window.</span></span>

![o efeito de desfoque aplicado a uma janela](images/dwm-blurbehindwindow.png)

<span data-ttu-id="9a9cc-135">Para aplicar o desfoque por trás de uma subregião, aplique um identificador de região válido (HRGN) ao membro **hRgnBlur** da estrutura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) e adicione o sinalizador **DWM \_ BB \_ BLURREGION** ao membro **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="9a9cc-135">To apply the blur behind a subregion, apply a valid region handle (HRGN) to the **hRgnBlur** member of the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure and add the **DWM\_BB\_BLURREGION** flag to the **dwFlags** member.</span></span>

<span data-ttu-id="9a9cc-136">Quando você aplica o efeito desfoque-atrás a uma subregião da janela, o canal alfa da janela é usado para a área não borrada.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-136">When you apply the blur-behind effect to a subregion of the window, the alpha channel of the window is used for the nonblurred area.</span></span> <span data-ttu-id="9a9cc-137">Isso pode causar uma transparência inesperada na região não borrada de uma janela.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-137">This can cause an unexpected transparency in the nonblurred region of a window.</span></span> <span data-ttu-id="9a9cc-138">Portanto, tenha cuidado ao aplicar um efeito de desfoque a uma sub-região.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-138">Therefore, be careful when you apply a blur effect to a subregion.</span></span>

## <a name="extending-the-window-frame-into-the-client-area"></a><span data-ttu-id="9a9cc-139">Estendendo o quadro da janela para a área do cliente</span><span class="sxs-lookup"><span data-stu-id="9a9cc-139">Extending the Window Frame into the Client Area</span></span>

<span data-ttu-id="9a9cc-140">Um aplicativo pode estender o desfoque do quadro da janela para a área do cliente.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-140">An application can extend the blur of the window frame into the client area.</span></span> <span data-ttu-id="9a9cc-141">Isso é útil quando você aplica o efeito de desfoque por trás de uma janela com uma barra de ferramentas encaixada ou separa visualmente os controles do restante de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-141">This is useful when you apply the blur effect behind a window with a docked toolbar or visually separate controls from the rest of an application.</span></span> <span data-ttu-id="9a9cc-142">Essa funcionalidade é exposta pela função [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="9a9cc-142">This functionality is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span>

<span data-ttu-id="9a9cc-143">Para habilitar o desfoque usando [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), use a estrutura [**Margins**](/windows/win32/api/uxtheme/ns-uxtheme-margins) para indicar quanto estender para a área do cliente.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-143">To enable blur by using [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), use the [**MARGINS**](/windows/win32/api/uxtheme/ns-uxtheme-margins) structure to indicate how much to extend into the client area.</span></span> <span data-ttu-id="9a9cc-144">A função de exemplo a seguir, `ExtendIntoClientBottom` , alterna a extensão de desfoque na parte inferior do quadro de não cliente para a área do cliente.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-144">The following example function, `ExtendIntoClientBottom`, toggles the blur extension on the bottom of the non-client frame into the client area.</span></span>


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="9a9cc-145">A imagem a seguir ilustra o efeito de desfoque estendido na parte inferior da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-145">The following image illustrates the blur-behind effect extended into the bottom of the client area.</span></span>

![imagem que mostra o efeito de desfoque estendido na parte inferior de uma área do cliente](images/dwm-extendedbottom.png)

<span data-ttu-id="9a9cc-147">Também está disponível por meio do método [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) , o efeito de "folha de vidro", em que o efeito de desfoque é aplicado à superfície inteira da janela sem uma borda de janela visível.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-147">Also available through the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) method is the "sheet of glass" effect, where the blur effect is applied to the whole surface of the window without a visible window border.</span></span> <span data-ttu-id="9a9cc-148">O exemplo a seguir demonstra esse efeito em que a área do cliente é renderizada sem uma borda de janela.</span><span class="sxs-lookup"><span data-stu-id="9a9cc-148">The following example demonstrates this effect where the client area is rendered without a window border.</span></span>


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="9a9cc-149">A imagem a seguir ilustra o desfoque no estilo de janela "folha de vidro".</span><span class="sxs-lookup"><span data-stu-id="9a9cc-149">The following image illustrates the blur-behind in the "sheet of glass" window style.</span></span>

![imagem que ilustra o efeito desfoque-atrás no estilo de janela "folha de vidro"](images/dwm-sheetofglass.png)

## <a name="related-topics"></a><span data-ttu-id="9a9cc-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a9cc-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a9cc-152">Visão geral do Gerenciador de Janelas da Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="9a9cc-152">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="9a9cc-153">Habilitar e controlar a composição do DWM</span><span class="sxs-lookup"><span data-stu-id="9a9cc-153">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="9a9cc-154">Considerações sobre desempenho e práticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="9a9cc-154">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 