---
title: Mensagem de WM_DPICHANGED (WinUser. h)
description: Enviado quando os pontos em vigor por polegada (DPI) de uma janela forem alterados.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- DPI alta de mensagem de WM_DPICHANGED
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644733"
---
# <a name="wm_dpichanged-message"></a><span data-ttu-id="d6142-104">Mensagem do WM \_ DPICHANGED</span><span class="sxs-lookup"><span data-stu-id="d6142-104">WM\_DPICHANGED message</span></span>

<span data-ttu-id="d6142-105">Enviado quando os pontos em vigor por polegada (DPI) de uma janela forem alterados.</span><span class="sxs-lookup"><span data-stu-id="d6142-105">Sent when the effective dots per inch (dpi) for a window has changed.</span></span> <span data-ttu-id="d6142-106">O DPI é o fator de escala para uma janela.</span><span class="sxs-lookup"><span data-stu-id="d6142-106">The DPI is the scale factor for a window.</span></span> <span data-ttu-id="d6142-107">Há vários eventos que podem fazer com que o DPI seja alterado.</span><span class="sxs-lookup"><span data-stu-id="d6142-107">There are multiple events that can cause the DPI to change.</span></span> <span data-ttu-id="d6142-108">A lista a seguir indica as possíveis causas para a alteração em DPI.</span><span class="sxs-lookup"><span data-stu-id="d6142-108">The following list indicates the possible causes for the change in DPI.</span></span>

-   <span data-ttu-id="d6142-109">A janela é movida para um novo monitor que tem um DPI diferente.</span><span class="sxs-lookup"><span data-stu-id="d6142-109">The window is moved to a new monitor that has a different DPI.</span></span>
-   <span data-ttu-id="d6142-110">O DPI do monitor que hospeda as alterações da janela.</span><span class="sxs-lookup"><span data-stu-id="d6142-110">The DPI of the monitor hosting the window changes.</span></span>

<span data-ttu-id="d6142-111">O DPI atual para uma janela sempre é igual ao último DPI enviado pelo **WM \_ DPICHANGED**.</span><span class="sxs-lookup"><span data-stu-id="d6142-111">The current DPI for a window always equals the last DPI sent by **WM\_DPICHANGED**.</span></span> <span data-ttu-id="d6142-112">Esse é o fator de escala em que a janela deve ser dimensionada para os threads que reconhecem as alterações de DPI.</span><span class="sxs-lookup"><span data-stu-id="d6142-112">This is the scale factor that the window should be scaling to for threads that are aware of DPI changes.</span></span>


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a><span data-ttu-id="d6142-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6142-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6142-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6142-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6142-115">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) do *wParam* contém o valor do eixo Y do novo DPI da janela.</span><span class="sxs-lookup"><span data-stu-id="d6142-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the *wParam* contains the Y-axis value of the new dpi of the window.</span></span> <span data-ttu-id="d6142-116">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) do *wParam* contém o valor do eixo X do novo DPI da janela.</span><span class="sxs-lookup"><span data-stu-id="d6142-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the *wParam* contains the X-axis value of the new DPI of the window.</span></span> <span data-ttu-id="d6142-117">Por exemplo, 96, 120, 144 ou 192.</span><span class="sxs-lookup"><span data-stu-id="d6142-117">For example, 96, 120, 144, or 192.</span></span> <span data-ttu-id="d6142-118">Os valores dos eixos X e Y são idênticos aos aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="d6142-118">The values of the X-axis and the Y-axis are identical for Windows apps.</span></span>

</dd> <dt>

<span data-ttu-id="d6142-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6142-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6142-120">Um ponteiro para uma estrutura [**Rect**](/windows/desktop/api/windef/ns-windef-rect) que fornece um tamanho sugerido e a posição da janela atual dimensionada para o novo dpi.</span><span class="sxs-lookup"><span data-stu-id="d6142-120">A pointer to a [**RECT**](/windows/desktop/api/windef/ns-windef-rect) structure that provides a suggested size and position of the current window scaled for the new DPI.</span></span> <span data-ttu-id="d6142-121">A expectativa é de que os aplicativos reposicionem e redimensionem o Windows com base nas sugestões fornecidas pelo *lParam* ao lidar com essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="d6142-121">The expectation is that apps will reposition and resize windows based on the suggestions provided by *lParam* when handling this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6142-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6142-122">Return value</span></span>

<span data-ttu-id="d6142-123">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="d6142-123">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6142-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6142-124">Remarks</span></span>

<span data-ttu-id="d6142-125">Essa mensagem só é relevante para processos por thread com reconhecimento de **\_ \_ \_ dpi \_ de monitor** ou **reconhecimento de DPI por segmentos com \_ \_ \_ \_ reconhecimento de monitor** .</span><span class="sxs-lookup"><span data-stu-id="d6142-125">This message is only relevant for **PROCESS\_PER\_MONITOR\_DPI\_AWARE** applications or **DPI\_AWARENESS\_PER\_MONITOR\_AWARE** threads.</span></span> <span data-ttu-id="d6142-126">Ele poderá ser recebido em determinadas alterações de DPI se a janela de nível superior ou o processo estiver sendo executado como **dpi** ou **reconhecimento de dpi de sistema**, mas nessas situações poderá ser ignorado com segurança.</span><span class="sxs-lookup"><span data-stu-id="d6142-126">It may be received on certain DPI changes if your top-level window or process is running as **DPI unaware** or **system DPI aware**, but in those situations it can be safely ignored.</span></span> <span data-ttu-id="d6142-127">Para obter mais informações sobre os diferentes tipos de conscientização, consulte reconhecimento de [**dpi de processo \_ \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) e [**\_ reconhecimento de DPI**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span><span class="sxs-lookup"><span data-stu-id="d6142-127">For more information about the different types of awareness, see [**PROCESS\_DPI\_AWARENESS**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) and [**DPI\_AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span></span> <span data-ttu-id="d6142-128">As versões mais antigas do Windows exigiam reconhecimento de DPI para serem ligadas no nível de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6142-128">Older versions of Windows required DPI awareness to be tied at the level of an application.</span></span> <span data-ttu-id="d6142-129">Esses aplicativos usam **\_ \_ reconhecimento de dpi de processo**.</span><span class="sxs-lookup"><span data-stu-id="d6142-129">Those apps use **PROCESS\_DPI\_AWARENESS**.</span></span> <span data-ttu-id="d6142-130">Atualmente, o reconhecimento de DPI está vinculado a threads e a janelas individuais, e não a todo o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6142-130">Currently, DPI awareness is tied to threads and individual windows rather than the entire application.</span></span> <span data-ttu-id="d6142-131">Esses aplicativos usam **\_ reconhecimento de DPI**.</span><span class="sxs-lookup"><span data-stu-id="d6142-131">These apps use **DPI\_AWARENESS**.</span></span>

<span data-ttu-id="d6142-132">Você só precisa usar o eixo X ou o valor do eixo Y ao dimensionar seu aplicativo, pois eles são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="d6142-132">You only need to use either the X-axis or the Y-axis value when scaling your application since they are the same.</span></span>

<span data-ttu-id="d6142-133">Para tratar essa mensagem corretamente, você precisará redimensionar e reposicionar sua janela com base nas sugestões fornecidas pelo *lParam* e usando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="d6142-133">In order to handle this message correctly, you will need to resize and reposition your window based on the suggestions provided by *lParam* and using [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="d6142-134">Se você não fizer isso, sua janela aumentará ou diminuirá em relação a todo o resto do novo monitor.</span><span class="sxs-lookup"><span data-stu-id="d6142-134">If you do not do this, your window will grow or shrink with respect to everything else on the new monitor.</span></span> <span data-ttu-id="d6142-135">Por exemplo, se um usuário estiver usando vários monitores e arrastar a janela de um monitor de 96 DPI para um monitor de 192 DPI, sua janela parecerá ser a metade grande em relação a outros itens no monitor de 192 DPI.</span><span class="sxs-lookup"><span data-stu-id="d6142-135">For example, if a user is using multiple monitors and drags your window from a 96 DPI monitor to a 192 DPI monitor, your window will appear to be half as large with respect to other items on the 192 DPI monitor.</span></span>

<span data-ttu-id="d6142-136">O valor base de DPI é definido como **\_ dpi de \_ tela \_ padrão do usuário** , que é definido como 96.</span><span class="sxs-lookup"><span data-stu-id="d6142-136">The base value of DPI is defined as **USER\_DEFAULT\_SCREEN\_DPI** which is set to 96.</span></span> <span data-ttu-id="d6142-137">Para determinar o fator de dimensionamento de um monitor, pegue o valor de DPI e divida por **\_ \_ \_ dpi de tela padrão do usuário**.</span><span class="sxs-lookup"><span data-stu-id="d6142-137">To determine the scaling factor for a monitor, take the DPI value and divide by **USER\_DEFAULT\_SCREEN\_DPI**.</span></span> <span data-ttu-id="d6142-138">A tabela a seguir fornece alguns valores de DPI de exemplo e fatores de dimensionamento associados.</span><span class="sxs-lookup"><span data-stu-id="d6142-138">The following table provides some sample DPI values and associated scaling factors.</span></span>



| <span data-ttu-id="d6142-139">Valor de DPI</span><span class="sxs-lookup"><span data-stu-id="d6142-139">DPI value</span></span> | <span data-ttu-id="d6142-140">Porcentagem de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="d6142-140">Scaling percentage</span></span> |
|-----------|--------------------|
| <span data-ttu-id="d6142-141">96</span><span class="sxs-lookup"><span data-stu-id="d6142-141">96</span></span>        | <span data-ttu-id="d6142-142">100%</span><span class="sxs-lookup"><span data-stu-id="d6142-142">100%</span></span>               |
| <span data-ttu-id="d6142-143">120</span><span class="sxs-lookup"><span data-stu-id="d6142-143">120</span></span>       | <span data-ttu-id="d6142-144">125%</span><span class="sxs-lookup"><span data-stu-id="d6142-144">125%</span></span>               |
| <span data-ttu-id="d6142-145">144</span><span class="sxs-lookup"><span data-stu-id="d6142-145">144</span></span>       | <span data-ttu-id="d6142-146">150%</span><span class="sxs-lookup"><span data-stu-id="d6142-146">150%</span></span>               |
| <span data-ttu-id="d6142-147">192</span><span class="sxs-lookup"><span data-stu-id="d6142-147">192</span></span>       | <span data-ttu-id="d6142-148">200%</span><span class="sxs-lookup"><span data-stu-id="d6142-148">200%</span></span>               |



 

<span data-ttu-id="d6142-149">O exemplo a seguir fornece um exemplo de manipulador de alterações de DPI.</span><span class="sxs-lookup"><span data-stu-id="d6142-149">The following example provides a sample DPI change handler.</span></span>


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



<span data-ttu-id="d6142-150">O código a seguir dimensiona linearmente um valor de 100% (96 DPI) para um DPI arbitrário definido por *g \_ dpi*.</span><span class="sxs-lookup"><span data-stu-id="d6142-150">The following code linearly scales a value from 100% (96 DPI) to an arbitrary DPI defined by *g\_dpi*.</span></span>


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



<span data-ttu-id="d6142-151">Uma maneira alternativa de dimensionar um valor é converter o valor de DPI em um fator de escala e usá-lo.</span><span class="sxs-lookup"><span data-stu-id="d6142-151">An alternative way to scale a value is to convert the DPI value into a scale factor and use that.</span></span>


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a><span data-ttu-id="d6142-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6142-152">Requirements</span></span>



| <span data-ttu-id="d6142-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6142-153">Requirement</span></span> | <span data-ttu-id="d6142-154">Valor</span><span class="sxs-lookup"><span data-stu-id="d6142-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d6142-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6142-155">Minimum supported client</span></span><br/> | <span data-ttu-id="d6142-156">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d6142-156">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d6142-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6142-157">Minimum supported server</span></span><br/> | <span data-ttu-id="d6142-158">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="d6142-158">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d6142-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6142-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6142-160"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6142-160"><dt>WinUser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6142-161">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d6142-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6142-162">**reconhecimento de DPI \_**</span><span class="sxs-lookup"><span data-stu-id="d6142-162">**DPI\_AWARENESS**</span></span>](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[<span data-ttu-id="d6142-163">**\_reconhecimento de dpi de processo \_**</span><span class="sxs-lookup"><span data-stu-id="d6142-163">**PROCESS\_DPI\_AWARENESS**</span></span>](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

