---
title: Mensagem de WM_NCLBUTTONDBLCLK (WinUser. h)
description: Postado quando o usuário clica duas vezes com o botão esquerdo do mouse enquanto o cursor está dentro da área não cliente de uma janela. Essa mensagem é postada na janela que contém o cursor. Se uma janela tiver capturado o mouse, essa mensagem não será postada.
ms.assetid: fc655631-64d0-4cc5-b85e-25d274182994
keywords:
- Entrada de mouse e teclado de mensagem WM_NCLBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_NCLBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db66edcb3b1645c6c34c72e35df53afc516dafc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085422"
---
# <a name="wm_nclbuttondblclk-message"></a><span data-ttu-id="b19db-106">Mensagem do WM \_ NCLBUTTONDBLCLK</span><span class="sxs-lookup"><span data-stu-id="b19db-106">WM\_NCLBUTTONDBLCLK message</span></span>

<span data-ttu-id="b19db-107">Postado quando o usuário clica duas vezes com o botão esquerdo do mouse enquanto o cursor está dentro da área não cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="b19db-107">Posted when the user double-clicks the left mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="b19db-108">Essa mensagem é postada na janela que contém o cursor.</span><span class="sxs-lookup"><span data-stu-id="b19db-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="b19db-109">Se uma janela tiver capturado o mouse, essa mensagem não será postada.</span><span class="sxs-lookup"><span data-stu-id="b19db-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="b19db-110">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b19db-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCLBUTTONDBLCLK              0x00A3
```



## <a name="parameters"></a><span data-ttu-id="b19db-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b19db-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b19db-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b19db-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b19db-113">O valor de teste de clique retornado pela função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado do processamento da mensagem [**\_ NCHITTEST do WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="b19db-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="b19db-114">Para obter uma lista de valores de teste de clique, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="b19db-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="b19db-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b19db-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b19db-116">Uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) que contém as coordenadas x e y do cursor.</span><span class="sxs-lookup"><span data-stu-id="b19db-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="b19db-117">As coordenadas são relativas ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="b19db-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b19db-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b19db-118">Return value</span></span>

<span data-ttu-id="b19db-119">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="b19db-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b19db-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b19db-120">Remarks</span></span>

<span data-ttu-id="b19db-121">Você também pode usar as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair os valores das coordenadas X e y do *lParam*.</span><span class="sxs-lookup"><span data-stu-id="b19db-121">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="b19db-122">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="b19db-122">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="b19db-123">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="b19db-123">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="b19db-124">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) testa o ponto especificado para descobrir o local do cursor e executa a ação apropriada.</span><span class="sxs-lookup"><span data-stu-id="b19db-124">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to find out the location of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="b19db-125">Se apropriado, **DefWindowProc** envia a mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) para a janela.</span><span class="sxs-lookup"><span data-stu-id="b19db-125">If appropriate, **DefWindowProc** sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="b19db-126">Uma janela não precisa ter o estilo **cs \_ DBLCLKS** para receber mensagens do **WM \_ NCLBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="b19db-126">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCLBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="b19db-127">O sistema gera uma mensagem do **WM \_ NCLBUTTONDBLCLK** quando o usuário pressiona, libera e novamente pressiona o botão esquerdo do mouse dentro do limite de tempo de clique duplo do sistema.</span><span class="sxs-lookup"><span data-stu-id="b19db-127">The system generates a **WM\_NCLBUTTONDBLCLK** message when the user presses, releases, and again presses the left mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="b19db-128">Clicar duas vezes no botão esquerdo do mouse gera quatro mensagens: [**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM \_ NCLBUTTONUP**](wm-nclbuttonup.md), **WM \_ NCLBUTTONDBLCLK** e **WM \_ NCLBUTTONUP** novamente.</span><span class="sxs-lookup"><span data-stu-id="b19db-128">Double-clicking the left mouse button actually generates four messages: [**WM\_NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM\_NCLBUTTONUP**](wm-nclbuttonup.md), **WM\_NCLBUTTONDBLCLK**, and **WM\_NCLBUTTONUP** again.</span></span>

## <a name="requirements"></a><span data-ttu-id="b19db-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b19db-129">Requirements</span></span>



| <span data-ttu-id="b19db-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b19db-130">Requirement</span></span> | <span data-ttu-id="b19db-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b19db-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b19db-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b19db-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b19db-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b19db-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b19db-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b19db-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b19db-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b19db-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b19db-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b19db-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b19db-137"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b19db-137"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b19db-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="b19db-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="b19db-139">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b19db-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b19db-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="b19db-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b19db-141">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="b19db-141">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="b19db-142">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="b19db-142">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="b19db-143">**NCHITTEST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="b19db-143">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="b19db-144">**NCLBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="b19db-144">**WM\_NCLBUTTONDOWN**</span></span>](wm-nclbuttondown.md)
</dt> <dt>

[<span data-ttu-id="b19db-145">**NCLBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="b19db-145">**WM\_NCLBUTTONUP**</span></span>](wm-nclbuttonup.md)
</dt> <dt>

[<span data-ttu-id="b19db-146">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="b19db-146">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="b19db-147">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b19db-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b19db-148">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="b19db-148">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="b19db-149">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="b19db-149">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b19db-150">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="b19db-150">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="b19db-151">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b19db-151">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

