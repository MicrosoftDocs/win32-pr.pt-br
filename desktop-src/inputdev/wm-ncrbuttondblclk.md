---
title: Mensagem de WM_NCRBUTTONDBLCLK (WinUser. h)
description: Postado quando o usuário clica duas vezes com o botão direito do mouse enquanto o cursor está dentro da área não cliente de uma janela. Essa mensagem é postada na janela que contém o cursor. Se uma janela tiver capturado o mouse, essa mensagem não será postada.
ms.assetid: 20d62b05-07de-49da-b160-29fa1f5067fa
keywords:
- Entrada de mouse e teclado de mensagem WM_NCRBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_NCRBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee33d9b31f99a00181427c9a715df792d95fe55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499558"
---
# <a name="wm_ncrbuttondblclk-message"></a><span data-ttu-id="e7c06-106">Mensagem do WM \_ NCRBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="e7c06-106">WM\_NCRBUTTONDBLCLK message</span></span>

<span data-ttu-id="e7c06-107">Postado quando o usuário clica duas vezes com o botão direito do mouse enquanto o cursor está dentro da área não cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="e7c06-107">Posted when the user double-clicks the right mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="e7c06-108">Essa mensagem é postada na janela que contém o cursor.</span><span class="sxs-lookup"><span data-stu-id="e7c06-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="e7c06-109">Se uma janela tiver capturado o mouse, essa mensagem não será postada.</span><span class="sxs-lookup"><span data-stu-id="e7c06-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="e7c06-110">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e7c06-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCRBUTTONDBLCLK              0x00A6
```



## <a name="parameters"></a><span data-ttu-id="e7c06-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7c06-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7c06-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7c06-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7c06-113">O valor de teste de clique retornado pela função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado do processamento da mensagem [**\_ NCHITTEST do WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="e7c06-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="e7c06-114">Para obter uma lista de valores de teste de clique, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="e7c06-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="e7c06-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7c06-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7c06-116">Uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) que contém as coordenadas x e y do cursor.</span><span class="sxs-lookup"><span data-stu-id="e7c06-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="e7c06-117">As coordenadas são relativas ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="e7c06-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7c06-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7c06-118">Return value</span></span>

<span data-ttu-id="e7c06-119">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="e7c06-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7c06-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7c06-120">Remarks</span></span>

<span data-ttu-id="e7c06-121">Uma janela não precisa ter o estilo **cs \_ DBLCLKS** para receber mensagens do **WM \_ NCRBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="e7c06-121">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCRBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="e7c06-122">O sistema gera uma mensagem do **WM \_ NCRBUTTONDBLCLK** quando o usuário pressiona, libera e novamente pressiona o botão direito do mouse dentro do limite de tempo de clique duplo do sistema.</span><span class="sxs-lookup"><span data-stu-id="e7c06-122">The system generates a **WM\_NCRBUTTONDBLCLK** message when the user presses, releases, and again presses the right mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="e7c06-123">Clicar duas vezes no botão direito do mouse gera quatro mensagens: [**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md), [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md), **WM \_ NCRBUTTONDBLCLK** e **WM \_ NCRBUTTONUP** novamente.</span><span class="sxs-lookup"><span data-stu-id="e7c06-123">Double-clicking the right mouse button actually generates four messages: [**WM\_NCRBUTTONDOWN**](wm-ncrbuttondown.md), [**WM\_NCRBUTTONUP**](wm-ncrbuttonup.md), **WM\_NCRBUTTONDBLCLK**, and **WM\_NCRBUTTONUP** again.</span></span>

<span data-ttu-id="e7c06-124">Você também pode usar as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair os valores das coordenadas X e y do *lParam*.</span><span class="sxs-lookup"><span data-stu-id="e7c06-124">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="e7c06-125">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="e7c06-125">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="e7c06-126">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="e7c06-126">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="e7c06-127">Se for apropriado fazer isso, o sistema enviará a mensagem [**\_ SYSCOMMAND do WM**](/windows/desktop/menurc/wm-syscommand) para a janela.</span><span class="sxs-lookup"><span data-stu-id="e7c06-127">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7c06-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7c06-128">Requirements</span></span>



| <span data-ttu-id="e7c06-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7c06-129">Requirement</span></span> | <span data-ttu-id="e7c06-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e7c06-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c06-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7c06-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e7c06-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7c06-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e7c06-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7c06-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e7c06-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7c06-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e7c06-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e7c06-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7c06-136"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7c06-136"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7c06-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7c06-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7c06-138">**Referência**</span><span class="sxs-lookup"><span data-stu-id="e7c06-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e7c06-139">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="e7c06-139">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="e7c06-140">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="e7c06-140">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="e7c06-141">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="e7c06-141">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="e7c06-142">**NCHITTEST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="e7c06-142">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="e7c06-143">**NCRBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="e7c06-143">**WM\_NCRBUTTONDOWN**</span></span>](wm-ncrbuttondown.md)
</dt> <dt>

[<span data-ttu-id="e7c06-144">**NCRBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="e7c06-144">**WM\_NCRBUTTONUP**</span></span>](wm-ncrbuttonup.md)
</dt> <dt>

[<span data-ttu-id="e7c06-145">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="e7c06-145">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="e7c06-146">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="e7c06-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e7c06-147">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="e7c06-147">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="e7c06-148">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="e7c06-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e7c06-149">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="e7c06-149">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="e7c06-150">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7c06-150">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

