---
title: Mensagem de WM_NCMBUTTONDBLCLK (WinUser. h)
description: Postado quando o usuário clica duas vezes no botão do meio do mouse enquanto o cursor está dentro da área não cliente de uma janela. Essa mensagem é postada na janela que contém o cursor. Se uma janela tiver capturado o mouse, essa mensagem não será postada.
ms.assetid: 7c0f8d6e-eb37-4873-a3f8-777e8b0b22bc
keywords:
- Entrada de mouse e teclado de mensagem WM_NCMBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_NCMBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612a0a7ca0a5731691ec244df505e3d058216e2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644541"
---
# <a name="wm_ncmbuttondblclk-message"></a><span data-ttu-id="2f943-106">Mensagem do WM \_ NCMBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="2f943-106">WM\_NCMBUTTONDBLCLK message</span></span>

<span data-ttu-id="2f943-107">Postado quando o usuário clica duas vezes no botão do meio do mouse enquanto o cursor está dentro da área não cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="2f943-107">Posted when the user double-clicks the middle mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="2f943-108">Essa mensagem é postada na janela que contém o cursor.</span><span class="sxs-lookup"><span data-stu-id="2f943-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="2f943-109">Se uma janela tiver capturado o mouse, essa mensagem não será postada.</span><span class="sxs-lookup"><span data-stu-id="2f943-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="2f943-110">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2f943-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMBUTTONDBLCLK              0x00A9
```



## <a name="parameters"></a><span data-ttu-id="2f943-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f943-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f943-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f943-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f943-113">O valor de teste de clique retornado pela função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado do processamento da mensagem [**\_ NCHITTEST do WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="2f943-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="2f943-114">Para obter uma lista de valores de teste de clique, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="2f943-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="2f943-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f943-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f943-116">Uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) que contém as coordenadas x e y do cursor.</span><span class="sxs-lookup"><span data-stu-id="2f943-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="2f943-117">As coordenadas são relativas ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="2f943-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f943-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f943-118">Return value</span></span>

<span data-ttu-id="2f943-119">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="2f943-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f943-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f943-120">Remarks</span></span>

<span data-ttu-id="2f943-121">Uma janela não precisa ter o estilo **cs \_ DBLCLKS** para receber mensagens do **WM \_ NCMBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="2f943-121">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCMBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="2f943-122">O sistema gera uma mensagem do **WM \_ NCMBUTTONDBLCLK** quando o usuário pressiona, libera e novamente pressiona o botão do meio do mouse dentro do limite de tempo de clique duplo do sistema.</span><span class="sxs-lookup"><span data-stu-id="2f943-122">The system generates a **WM\_NCMBUTTONDBLCLK** message when the user presses, releases, and again presses the middle mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="2f943-123">Clicar duas vezes no botão do meio do mouse gera quatro mensagens [**: \_ WM NCMBUTTONDOWN**](wm-ncmbuttondown.md), [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md), **WM \_ NCMBUTTONDBLCLK** e **WM \_ NCMBUTTONUP** novamente.</span><span class="sxs-lookup"><span data-stu-id="2f943-123">Double-clicking the middle mouse button actually generates four messages: [**WM\_NCMBUTTONDOWN**](wm-ncmbuttondown.md), [**WM\_NCMBUTTONUP**](wm-ncmbuttonup.md), **WM\_NCMBUTTONDBLCLK**, and **WM\_NCMBUTTONUP** again.</span></span>

<span data-ttu-id="2f943-124">Você também pode usar as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair os valores das coordenadas X e y do *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2f943-124">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="2f943-125">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="2f943-125">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="2f943-126">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="2f943-126">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="2f943-127">Se for apropriado fazer isso, o sistema enviará a mensagem [**\_ SYSCOMMAND do WM**](/windows/desktop/menurc/wm-syscommand) para a janela.</span><span class="sxs-lookup"><span data-stu-id="2f943-127">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f943-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f943-128">Requirements</span></span>



| <span data-ttu-id="2f943-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f943-129">Requirement</span></span> | <span data-ttu-id="2f943-130">Valor</span><span class="sxs-lookup"><span data-stu-id="2f943-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f943-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f943-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2f943-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f943-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2f943-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f943-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2f943-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f943-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2f943-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2f943-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f943-136"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f943-136"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f943-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f943-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f943-138">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2f943-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2f943-139">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2f943-139">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2f943-140">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="2f943-140">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="2f943-141">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="2f943-141">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="2f943-142">**NCHITTEST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2f943-142">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="2f943-143">**NCMBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2f943-143">**WM\_NCMBUTTONDOWN**</span></span>](wm-ncmbuttondown.md)
</dt> <dt>

[<span data-ttu-id="2f943-144">**NCMBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2f943-144">**WM\_NCMBUTTONUP**</span></span>](wm-ncmbuttonup.md)
</dt> <dt>

[<span data-ttu-id="2f943-145">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2f943-145">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="2f943-146">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="2f943-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2f943-147">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="2f943-147">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="2f943-148">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="2f943-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2f943-149">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="2f943-149">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="2f943-150">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f943-150">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

