---
title: Mensagem de WM_NCXBUTTONUP (WinUser. h)
description: Postado quando o usuário libera o primeiro ou o segundo botão X enquanto o cursor está na área não cliente de uma janela. Essa mensagem é postada na janela que contém o cursor. Se uma janela tiver capturado o mouse, essa mensagem não será postada.
ms.assetid: 07ab5d4e-9912-4867-9146-8abc5addc15d
keywords:
- Entrada de mouse e teclado de mensagem WM_NCXBUTTONUP
topic_type:
- apiref
api_name:
- WM_NCXBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6330849a433787dd09fad536f005d91f60376013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644861"
---
# <a name="wm_ncxbuttonup-message"></a><span data-ttu-id="ca6d4-106">Mensagem do WM \_ NCXBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="ca6d4-106">WM\_NCXBUTTONUP message</span></span>

<span data-ttu-id="ca6d4-107">Postado quando o usuário libera o primeiro ou o segundo botão X enquanto o cursor está na área não cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-107">Posted when the user releases the first or second X button while the cursor is in the nonclient area of a window.</span></span> <span data-ttu-id="ca6d4-108">Essa mensagem é postada na janela que contém o cursor.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="ca6d4-109">Se uma janela tiver capturado o mouse, essa mensagem *não* será postada.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-109">If a window has captured the mouse, this message is *not* posted.</span></span>

<span data-ttu-id="ca6d4-110">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ca6d4-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCXBUTTONUP                  0x00AC
```



## <a name="parameters"></a><span data-ttu-id="ca6d4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca6d4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca6d4-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca6d4-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca6d4-113">A palavra de ordem inferior Especifica o valor de teste de clique retornado pela função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) do processamento da mensagem do [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="ca6d4-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function from processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="ca6d4-114">Para obter uma lista de valores de teste de clique, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="ca6d4-115">A palavra de ordem superior indica qual botão foi liberado.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-115">The high-order word indicates which button was released.</span></span> <span data-ttu-id="ca6d4-116">Pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-116">It can be one of the following values.</span></span>



| <span data-ttu-id="ca6d4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ca6d4-117">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="ca6d4-118">Significado</span><span class="sxs-lookup"><span data-stu-id="ca6d4-118">Meaning</span></span>                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="ca6d4-119"><dt>**XButton1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="ca6d4-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="ca6d4-120">O primeiro botão X foi liberado.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-120">The first X button was released.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="ca6d4-121"><dt>**XButton2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="ca6d4-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="ca6d4-122">O segundo botão X foi liberado.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-122">The second X button was released.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ca6d4-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca6d4-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca6d4-124">Um ponteiro para uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) que contém as coordenadas x e y do cursor.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-124">A pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="ca6d4-125">As coordenadas são relativas ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-125">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca6d4-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca6d4-126">Return value</span></span>

<span data-ttu-id="ca6d4-127">Se um aplicativo processar essa mensagem, ele deverá retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-127">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="ca6d4-128">Para obter mais informações sobre como processar o valor de retorno, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-128">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca6d4-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca6d4-129">Remarks</span></span>

<span data-ttu-id="ca6d4-130">Use o código a seguir para obter as informações no parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="ca6d4-130">Use the following code to get the information in the *wParam* parameter.</span></span>


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



<span data-ttu-id="ca6d4-131">Você também pode usar o código a seguir para obter as coordenadas x e y do *lParam*:</span><span class="sxs-lookup"><span data-stu-id="ca6d4-131">You can also use the following code to get the x- and y-coordinates from *lParam*:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="ca6d4-132">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-132">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="ca6d4-133">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-133">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="ca6d4-134">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) testa o ponto especificado para obter a posição do cursor e executa a ação apropriada.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-134">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to get the position of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="ca6d4-135">Se apropriado, ele envia a [**mensagem \_ SYSCOMMAND do WM**](/windows/desktop/menurc/wm-syscommand) para a janela.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-135">If appropriate, it sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="ca6d4-136">Ao contrário das mensagens do [**WM \_ NCLBUTTONUP**](wm-nclbuttonup.md), do [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md)e do [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md) , um aplicativo deve retornar **true** dessa mensagem se a processar.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-136">Unlike the [**WM\_NCLBUTTONUP**](wm-nclbuttonup.md), [**WM\_NCMBUTTONUP**](wm-ncmbuttonup.md), and [**WM\_NCRBUTTONUP**](wm-ncrbuttonup.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="ca6d4-137">Isso permitirá que o software que simula essa mensagem em sistemas Windows anteriores ao Windows 2000 determine se o procedimento de janela processou a mensagem ou chamou [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para processá-la.</span><span class="sxs-lookup"><span data-stu-id="ca6d4-137">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca6d4-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca6d4-138">Requirements</span></span>



| <span data-ttu-id="ca6d4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca6d4-139">Requirement</span></span> | <span data-ttu-id="ca6d4-140">Valor</span><span class="sxs-lookup"><span data-stu-id="ca6d4-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca6d4-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca6d4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ca6d4-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ca6d4-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ca6d4-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca6d4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ca6d4-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ca6d4-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ca6d4-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ca6d4-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca6d4-146"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca6d4-146"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca6d4-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca6d4-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="ca6d4-148">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ca6d4-148">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ca6d4-149">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="ca6d4-149">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="ca6d4-150">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="ca6d4-150">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="ca6d4-151">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="ca6d4-151">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="ca6d4-152">**NCHITTEST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="ca6d4-152">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="ca6d4-153">**NCXBUTTONDBLCLK do WM \_**</span><span class="sxs-lookup"><span data-stu-id="ca6d4-153">**WM\_NCXBUTTONDBLCLK**</span></span>](wm-ncxbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="ca6d4-154">**NCXBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="ca6d4-154">**WM\_NCXBUTTONDOWN**</span></span>](wm-ncxbuttondown.md)
</dt> <dt>

[<span data-ttu-id="ca6d4-155">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="ca6d4-155">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="ca6d4-156">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ca6d4-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ca6d4-157">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="ca6d4-157">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="ca6d4-158">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="ca6d4-158">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ca6d4-159">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="ca6d4-159">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="ca6d4-160">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca6d4-160">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

