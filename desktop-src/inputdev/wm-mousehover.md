---
title: Mensagem de WM_MOUSEHOVER (WinUser. h)
description: Postado em uma janela quando o cursor passa sobre a área do cliente da janela pelo período de tempo especificado em uma chamada anterior para TrackMouseEvent.
ms.assetid: efba7f04-2d26-44f1-89df-a565c03ad944
keywords:
- Entrada de mouse e teclado de mensagem WM_MOUSEHOVER
topic_type:
- apiref
api_name:
- WM_MOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65747ade6bd2ec9456281ac02711de18675a411e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454956"
---
# <a name="wm_mousehover-message"></a><span data-ttu-id="ee788-104">Mensagem do WM \_ MOUSEHOVER</span><span class="sxs-lookup"><span data-stu-id="ee788-104">WM\_MOUSEHOVER message</span></span>

<span data-ttu-id="ee788-105">Postado em uma janela quando o cursor passa sobre a área do cliente da janela pelo período de tempo especificado em uma chamada anterior para [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="ee788-105">Posted to a window when the cursor hovers over the client area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="ee788-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ee788-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHOVER                   0x02A1
```



## <a name="parameters"></a><span data-ttu-id="ee788-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee788-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee788-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee788-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee788-109">Indica se várias chaves virtuais estão inativas.</span><span class="sxs-lookup"><span data-stu-id="ee788-109">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="ee788-110">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ee788-110">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="ee788-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ee788-111">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="ee788-112">Significado</span><span class="sxs-lookup"><span data-stu-id="ee788-112">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="ee788-113"><dt>**MK \_**</dt> <dt>0X0008</dt> de controle</span><span class="sxs-lookup"><span data-stu-id="ee788-113"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="ee788-114">A tecla CTRL é pressionada.</span><span class="sxs-lookup"><span data-stu-id="ee788-114">The CTRL key is depressed.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="ee788-115"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="ee788-115"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="ee788-116">O botão esquerdo do mouse é pressionado.</span><span class="sxs-lookup"><span data-stu-id="ee788-116">The left mouse button is depressed.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="ee788-117"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="ee788-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="ee788-118">O botão do meio do mouse é pressionado.</span><span class="sxs-lookup"><span data-stu-id="ee788-118">The middle mouse button is depressed.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="ee788-119"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="ee788-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="ee788-120">O botão direito do mouse é pressionado.</span><span class="sxs-lookup"><span data-stu-id="ee788-120">The right mouse button is depressed.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="ee788-121"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="ee788-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="ee788-122">A tecla SHIFT é pressionada.</span><span class="sxs-lookup"><span data-stu-id="ee788-122">The SHIFT key is depressed.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="ee788-123"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="ee788-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="ee788-124">O primeiro botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="ee788-124">The first X button is down.</span></span><br/>           |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="ee788-125"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="ee788-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="ee788-126">O segundo botão X está inoperante.</span><span class="sxs-lookup"><span data-stu-id="ee788-126">The second X button is down.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="ee788-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee788-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee788-128">A palavra de ordem inferior Especifica a coordenada x do cursor.</span><span class="sxs-lookup"><span data-stu-id="ee788-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="ee788-129">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="ee788-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="ee788-130">A palavra de ordem superior especifica a coordenada y do cursor.</span><span class="sxs-lookup"><span data-stu-id="ee788-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="ee788-131">A coordenada é relativa ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="ee788-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee788-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee788-132">Return value</span></span>

<span data-ttu-id="ee788-133">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="ee788-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee788-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee788-134">Remarks</span></span>

<span data-ttu-id="ee788-135">O controle de foco para quando o **WM \_ MOUSEHOVER** é gerado.</span><span class="sxs-lookup"><span data-stu-id="ee788-135">Hover tracking stops when **WM\_MOUSEHOVER** is generated.</span></span> <span data-ttu-id="ee788-136">O aplicativo deve chamar [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) novamente se precisar de mais controle sobre o comportamento de focalização do mouse.</span><span class="sxs-lookup"><span data-stu-id="ee788-136">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="ee788-137">Use o código a seguir para obter a posição horizontal e vertical:</span><span class="sxs-lookup"><span data-stu-id="ee788-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="ee788-138">Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores).</span><span class="sxs-lookup"><span data-stu-id="ee788-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="ee788-139">Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ee788-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="ee788-140">Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.</span><span class="sxs-lookup"><span data-stu-id="ee788-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee788-141">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="ee788-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="ee788-142">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="ee788-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee788-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee788-143">Requirements</span></span>



| <span data-ttu-id="ee788-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee788-144">Requirement</span></span> | <span data-ttu-id="ee788-145">Valor</span><span class="sxs-lookup"><span data-stu-id="ee788-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee788-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee788-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ee788-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee788-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ee788-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee788-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ee788-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee788-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ee788-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ee788-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee788-151"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee788-151"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee788-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee788-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee788-153">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ee788-153">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ee788-154">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="ee788-154">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="ee788-155">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="ee788-155">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="ee788-156">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="ee788-156">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="ee788-157">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="ee788-157">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="ee788-158">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="ee788-158">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="ee788-159">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="ee788-159">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

<span data-ttu-id="ee788-160">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ee788-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ee788-161">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="ee788-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="ee788-162">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="ee788-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ee788-163">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="ee788-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="ee788-164">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ee788-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

