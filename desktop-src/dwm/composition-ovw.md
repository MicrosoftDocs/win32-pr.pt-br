---
title: Habilitar e controlar a composição do DWM
description: As APIs de composição do Gerenciador de Janelas da Área de Trabalho (DWM) fornecem várias funções para configurar e consultar informações básicas que são usadas pelo DWM.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), composição
- DWM (Gerenciador de Janelas da Área de Trabalho), composição
- composição
- composição de área de trabalho
- colorização
- renderização de região não cliente
- Gerenciador de Janelas da Área de Trabalho (DWM), colorização
- DWM (Gerenciador de Janelas da Área de Trabalho), colorização
- Gerenciador de Janelas da Área de Trabalho (DWM), renderização de região não cliente
- DWM (Gerenciador de Janelas da Área de Trabalho), renderização de região não cliente
- Gerenciador de Janelas da Área de Trabalho (DWM), mensagens
- DWM (Gerenciador de Janelas da Área de Trabalho), mensagens
- mensagens
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: 8d7654f479896002b4bc65df613fab9506caf2a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822940"
---
# <a name="enable-and-control-dwm-composition"></a><span data-ttu-id="edff6-116">Habilitar e controlar a composição do DWM</span><span class="sxs-lookup"><span data-stu-id="edff6-116">Enable and control DWM composition</span></span>

<span data-ttu-id="edff6-117">As APIs de composição do Gerenciador de Janelas da Área de Trabalho (DWM) fornecem várias funções para configurar e consultar informações básicas que são usadas pelo DWM.</span><span class="sxs-lookup"><span data-stu-id="edff6-117">The Desktop Window Manager (DWM) composition APIs provide several functions for setting and querying for basic information that is used by the DWM.</span></span> <span data-ttu-id="edff6-118">Essas APIs permitem consultar e alterar o estado de composição.</span><span class="sxs-lookup"><span data-stu-id="edff6-118">These APIs enable you to query and change the composition state.</span></span> <span data-ttu-id="edff6-119">Além disso, você pode definir e consultar a política de renderização para diferentes atributos de janela do DWM.</span><span class="sxs-lookup"><span data-stu-id="edff6-119">Additionally, you can set and query the rendering policy for different DWM window attributes.</span></span>

## <a name="retrieving-colorization-information"></a><span data-ttu-id="edff6-120">Recuperando informações de colorização</span><span class="sxs-lookup"><span data-stu-id="edff6-120">Retrieving colorization information</span></span>

<span data-ttu-id="edff6-121">A cor da região não cliente de uma janela é determinada pelo tema de cores do sistema atual.</span><span class="sxs-lookup"><span data-stu-id="edff6-121">The color of the non-client region of a window is determined by the current system color theme.</span></span> <span data-ttu-id="edff6-122">O valor de colorização é fornecido por meio das APIs do DWM para permitir que seu aplicativo corresponda a interface do usuário do cliente com o tema de cores do sistema.</span><span class="sxs-lookup"><span data-stu-id="edff6-122">The colorization value is provided through the DWM APIs to enable your application to match client UI with the system color theme.</span></span>

<span data-ttu-id="edff6-123">Para acessar esse valor de colorização e monitorar a alteração de cor, use a função [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) e a mensagem de [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="edff6-123">To access this colorization value, and monitor the color change, use the [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) function and the [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) message.</span></span>

<span data-ttu-id="edff6-124">Este exemplo demonstra como manipular a mensagem de alteração de cor e acessar a nova cor.</span><span class="sxs-lookup"><span data-stu-id="edff6-124">This example demonstrates how to handle the color changed message and access the new color.</span></span>

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a><span data-ttu-id="edff6-125">Controlando a renderização de região não cliente</span><span class="sxs-lookup"><span data-stu-id="edff6-125">Controlling non-client region rendering</span></span>

<span data-ttu-id="edff6-126">Dois dos efeitos visuais que o DWM permite são transparências da região não cliente de uma janela e efeitos de transição.</span><span class="sxs-lookup"><span data-stu-id="edff6-126">Two of the visual effects that DWM enables are transparency of the non-client region of a window, and transition effects.</span></span> <span data-ttu-id="edff6-127">Seu aplicativo pode ter que desabilitar ou reabilitar esses efeitos para estilos ou motivos de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="edff6-127">Your application might have to disable or re-enable these effects for styling or compatibility reasons.</span></span> <span data-ttu-id="edff6-128">As funções a seguir são usadas para gerenciar o comportamento de efeito de transição e transparência.</span><span class="sxs-lookup"><span data-stu-id="edff6-128">The following functions are used to manage transparency and transition effect behavior.</span></span>

- [<span data-ttu-id="edff6-129">**DwmGetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="edff6-129">**DwmGetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [<span data-ttu-id="edff6-130">**DwmSetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="edff6-130">**DwmSetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

<span data-ttu-id="edff6-131">Para recuperar o estado de renderização não cliente atual para a janela de um aplicativo, chame [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) com *dwAttribute* definido como [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span><span class="sxs-lookup"><span data-stu-id="edff6-131">To retrieve the current non-client rendering state for an application's window, call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with *dwAttribute* set to [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span></span> <span data-ttu-id="edff6-132">Como você pode ver na documentação para [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), quando você passa esse sinalizador para **DwmGetWindowAttribute**, o valor do atributo recuperado é do tipo **bool**.</span><span class="sxs-lookup"><span data-stu-id="edff6-132">As you can see from the documentation for [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), when you pass that flag to **DwmGetWindowAttribute**, the retrieved attribute value is of type **BOOL**.</span></span> <span data-ttu-id="edff6-133">Sinalizadores diferentes fazem com que o **DwmGetWindowAttribute** retorne valores de tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="edff6-133">Different flags cause **DwmGetWindowAttribute** to return values of different types.</span></span> <span data-ttu-id="edff6-134">Aqui está um exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="edff6-134">Here's a code example.</span></span>

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

<span data-ttu-id="edff6-135">Este exemplo a seguir mostra como usar o sinalizador [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) com **DwmGetWindowAttribute** para recuperar o retângulo de limites de quadro estendido de uma janela.</span><span class="sxs-lookup"><span data-stu-id="edff6-135">This next example shows how to use the [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) flag with **DwmGetWindowAttribute** to retrieve the extended frame bounds rectangle of a window.</span></span> <span data-ttu-id="edff6-136">A documentação para esse sinalizador nos informa que o valor do atributo recuperado é do tipo **Rect**.</span><span class="sxs-lookup"><span data-stu-id="edff6-136">The documentation for that flag tells us that the retrieved attribute value is of type **RECT**.</span></span>

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> <span data-ttu-id="edff6-137">Siga o mesmo padrão de programação mostrado acima ao chamar [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) com sinalizadores para atributos diferentes.</span><span class="sxs-lookup"><span data-stu-id="edff6-137">Follow the same programming pattern shown above when you call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with flags for different attributes.</span></span> <span data-ttu-id="edff6-138">O tópico de enumeração [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) indica, na linha para cada sinalizador, a qual tipo de valor você deve passar um ponteiro no parâmetro *pvAttribute* para **DwmGetWindowAttribute**.</span><span class="sxs-lookup"><span data-stu-id="edff6-138">The [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) enumeration topic indicates, in the row for each flag, what type of value you should pass a pointer to in the *pvAttribute* parameter for **DwmGetWindowAttribute**.</span></span> <span data-ttu-id="edff6-139">O parâmetro *cbAttribute* contém o tamanho, em bytes, desse objeto.</span><span class="sxs-lookup"><span data-stu-id="edff6-139">The *cbAttribute* parameter contains the size, in bytes, of that object.</span></span>

<span data-ttu-id="edff6-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) permite que seu aplicativo defina a política de renderização de área não cliente.</span><span class="sxs-lookup"><span data-stu-id="edff6-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) enables your application to set the non-client area rendering policy.</span></span> <span data-ttu-id="edff6-141">Essa função também determina como seu aplicativo deve tratar os efeitos de transição do DWM.</span><span class="sxs-lookup"><span data-stu-id="edff6-141">That function also determines how your application should handle DWM transition effects.</span></span>

<span data-ttu-id="edff6-142">Este próximo exemplo desabilita a renderização de área que não é do cliente.</span><span class="sxs-lookup"><span data-stu-id="edff6-142">This next example disables non-client area rendering.</span></span> <span data-ttu-id="edff6-143">Isso faz com que todas as chamadas anteriores para [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) ou [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) sejam desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="edff6-143">This causes any previous calls to [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) or to [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to be disabled.</span></span>

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

<span data-ttu-id="edff6-144">Além de controlar a renderização de área de não cliente, o [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) também pode controlar os efeitos de transição do DWM.</span><span class="sxs-lookup"><span data-stu-id="edff6-144">In addition to controlling the non-client area rendering, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) can also control DWM transition effects.</span></span> <span data-ttu-id="edff6-145">Você pode definir o comportamento de transição **usando \_ transições DWMWA \_ FORCEDISABLED** como o parâmetro *dwAttribute* .</span><span class="sxs-lookup"><span data-stu-id="edff6-145">You can set transition behavior by using **DWMWA\_TRANSITIONS\_FORCEDISABLED** as the *dwAttribute* parameter.</span></span>

## <a name="messages"></a><span data-ttu-id="edff6-146">Mensagens</span><span class="sxs-lookup"><span data-stu-id="edff6-146">Messages</span></span>

<span data-ttu-id="edff6-147">As mensagens a seguir fornecem notificação de eventos do DWM.</span><span class="sxs-lookup"><span data-stu-id="edff6-147">The following messages provide notification of DWM events.</span></span> <span data-ttu-id="edff6-148">Essas mensagens podem ser usadas para monitorar alterações, como alterações de estado de composição e alterações de tema de cores do sistema.</span><span class="sxs-lookup"><span data-stu-id="edff6-148">These messages can be used to monitor changes such as composition state changes and system color theme changes.</span></span>

- [<span data-ttu-id="edff6-149">**DWMCOLORIZATIONCOLORCHANGED do WM \_**</span><span class="sxs-lookup"><span data-stu-id="edff6-149">**WM\_DWMCOLORIZATIONCOLORCHANGED**</span></span>](wm-dwmcolorizationcolorchanged.md)
- [<span data-ttu-id="edff6-150">**DWMCOMPOSITIONCHANGED do WM \_**</span><span class="sxs-lookup"><span data-stu-id="edff6-150">**WM\_DWMCOMPOSITIONCHANGED**</span></span>](wm-dwmcompositionchanged.md)
- [<span data-ttu-id="edff6-151">**DWMNCRENDERINGCHANGED do WM \_**</span><span class="sxs-lookup"><span data-stu-id="edff6-151">**WM\_DWMNCRENDERINGCHANGED**</span></span>](wm-dwmncrenderingchanged.md)
- [<span data-ttu-id="edff6-152">**DWMWINDOWMAXIMIZEDCHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="edff6-152">**WM\_DWMWINDOWMAXIMIZEDCHANGE**</span></span>](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a><span data-ttu-id="edff6-153">Desabilitando a composição do DWM (Windows 7 e anterior)</span><span class="sxs-lookup"><span data-stu-id="edff6-153">Disabling DWM composition (Windows 7 and earlier)</span></span>

> [!WARNING]
> <span data-ttu-id="edff6-154">As informações nesta seção aplicam-se somente ao Windows 7 e aos sistemas anteriores.</span><span class="sxs-lookup"><span data-stu-id="edff6-154">The info in this section applies only to Windows 7 and earlier systems.</span></span>

<span data-ttu-id="edff6-155">Como o DWM usa a GPU (unidade de processamento gráfico) para composição de área de trabalho, seu aplicativo pode ter que desabilitar o DWM para compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="edff6-155">Because DWM uses the graphics processing unit (GPU) for desktop composition, your application might have to disable DWM for compatibility.</span></span> <span data-ttu-id="edff6-156">Os aplicativos que assumem controle total da área de trabalho, como jogos executados no modo de tela inteira, devem determinar se o DWM está habilitado e, se estiver, desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="edff6-156">Applications that take full control of the desktop, such as games that run in full-screen mode, must determine whether the DWM is enabled and if it is, disable it.</span></span> <span data-ttu-id="edff6-157">Para fazer isso, são necessárias duas funções.</span><span class="sxs-lookup"><span data-stu-id="edff6-157">To do this, two functions are needed.</span></span>

- [<span data-ttu-id="edff6-158">**DwmIsCompositionEnabled**</span><span class="sxs-lookup"><span data-stu-id="edff6-158">**DwmIsCompositionEnabled**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [<span data-ttu-id="edff6-159">**DwmEnableComposition**</span><span class="sxs-lookup"><span data-stu-id="edff6-159">**DwmEnableComposition**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

<span data-ttu-id="edff6-160">Uma chamada para [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) com *FEnable* definido como **DWM \_ EC \_ DISABLECOMPOSITION** desabilita a composição do DWM até que o processo de chamada tenha sido desligado ou a composição tenha sido reabilitada chamando **DwmEnableComposition** com *fEnable* definido como **DWM \_ EC \_ ENABLECOMPOSITION**.</span><span class="sxs-lookup"><span data-stu-id="edff6-160">A call to [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) with *fEnable* set to **DWM\_EC\_DISABLECOMPOSITION** disables DWM composition until either the calling process has shut down, or composition has been re-enabled by calling **DwmEnableComposition** with *fEnable* set to **DWM\_EC\_ENABLECOMPOSITION**.</span></span> <span data-ttu-id="edff6-161">A composição do DWM é reiniciada automaticamente assim que todos os aplicativos que têm a composição desabilitada são desligados ou reativados manualmente por meio da chamada de **DwmEnableComposition**.</span><span class="sxs-lookup"><span data-stu-id="edff6-161">DWM composition restarts automatically as soon as all applications that have disabled composition have either shut down or have manually re-enabled composition by calling **DwmEnableComposition**.</span></span>

> [!NOTE]  
> <span data-ttu-id="edff6-162">O DWM desabilita automaticamente a composição quando um aplicativo tenta desenhar diretamente na superfície de exibição primária.</span><span class="sxs-lookup"><span data-stu-id="edff6-162">The DWM automatically disables composition when an application attempts to draw directly to the primary display surface.</span></span> <span data-ttu-id="edff6-163">A composição será desabilitada até que a superfície do dispositivo primário seja liberada por esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edff6-163">Composition will be disabled until the primary device surface is released by that application.</span></span>
