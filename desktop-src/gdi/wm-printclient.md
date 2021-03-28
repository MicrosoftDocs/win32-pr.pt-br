---
description: A mensagem do WM \_ fileclient é enviada a uma janela para solicitar que ela Desenhe sua área de cliente no contexto do dispositivo especificado, mais comumente em um contexto de dispositivo de impressora.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: Mensagem de WM_PRINTCLIENT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52aca68695964a35ab9a2c4e309cd71c2e9f7eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968082"
---
# <a name="wm_printclient-message"></a><span data-ttu-id="63916-103">Mensagem do WM \_ FILEclient</span><span class="sxs-lookup"><span data-stu-id="63916-103">WM\_PRINTCLIENT message</span></span>

<span data-ttu-id="63916-104">A mensagem do **WM \_ fileclient** é enviada a uma janela para solicitar que ela Desenhe sua área de cliente no contexto do dispositivo especificado, mais comumente em um contexto de dispositivo de impressora.</span><span class="sxs-lookup"><span data-stu-id="63916-104">The **WM\_PRINTCLIENT** message is sent to a window to request that it draw its client area in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="63916-105">Diferentemente do [**WM \_ Print**](wm-print.md), o **WM \_ fileclient** não é processado pelo [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="63916-105">Unlike [**WM\_PRINT**](wm-print.md), **WM\_PRINTCLIENT** is not processed by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="63916-106">Uma janela deve processar a mensagem do **WM \_ fileclient** por meio de uma função do [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) definida pelo aplicativo para que ela seja usada corretamente.</span><span class="sxs-lookup"><span data-stu-id="63916-106">A window should process the **WM\_PRINTCLIENT** message through an application-defined [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function for it to be used properly.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="63916-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63916-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63916-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63916-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63916-109">Um identificador para o contexto do dispositivo para desenhar.</span><span class="sxs-lookup"><span data-stu-id="63916-109">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="63916-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63916-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63916-111">As opções de desenho.</span><span class="sxs-lookup"><span data-stu-id="63916-111">The drawing options.</span></span> <span data-ttu-id="63916-112">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="63916-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="63916-113">Valor</span><span class="sxs-lookup"><span data-stu-id="63916-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="63916-114">Significado</span><span class="sxs-lookup"><span data-stu-id="63916-114">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="63916-115"><dt>**\_CHECKVISIBLE PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="63916-115"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="63916-116">Desenha a janela somente se ela estiver visível.</span><span class="sxs-lookup"><span data-stu-id="63916-116">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="63916-117"><dt>**filhos de PRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63916-117"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="63916-118">Desenha todas as janelas filhas visíveis.</span><span class="sxs-lookup"><span data-stu-id="63916-118">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="63916-119"><dt>**\_cliente PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="63916-119"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="63916-120">Desenha a área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="63916-120">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="63916-121"><dt>**\_ERASEBKGND PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="63916-121"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="63916-122">Apaga o plano de fundo antes de desenhar a janela.</span><span class="sxs-lookup"><span data-stu-id="63916-122">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="63916-123"><dt>**Não \_ cliente PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="63916-123"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="63916-124">Desenha a área não cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="63916-124">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="63916-125"><dt>**Propriedade do PRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63916-125"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="63916-126">Desenha todas as janelas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="63916-126">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63916-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="63916-127">Remarks</span></span>

<span data-ttu-id="63916-128">Uma janela pode processar essa mensagem da mesma maneira que o [**WM \_ Paint**](./wm-paint.md), exceto que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) não precisam ser chamados (um contexto de dispositivo é fornecido) e a janela deve desenhar toda a área do cliente em vez de apenas a região inválida.</span><span class="sxs-lookup"><span data-stu-id="63916-128">A window can process this message in much the same manner as [**WM\_PAINT**](./wm-paint.md), except that [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) need not be called (a device context is provided), and the window should draw its entire client area rather than just the invalid region.</span></span>

<span data-ttu-id="63916-129">As janelas que podem ser usadas em qualquer lugar no sistema, como controles, devem processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="63916-129">Windows that can be used anywhere in the system, such as controls, should process this message.</span></span> <span data-ttu-id="63916-130">Provavelmente vale a pena que outras janelas processem essa mensagem também porque é relativamente fácil de implementar.</span><span class="sxs-lookup"><span data-stu-id="63916-130">It is probably worthwhile for other windows to process this message as well because it is relatively easy to implement.</span></span>

<span data-ttu-id="63916-131">A função [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) requer que a janela que está sendo animada implemente a mensagem do **WM \_ fileclient** .</span><span class="sxs-lookup"><span data-stu-id="63916-131">The [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) function requires that the window being animated implements the **WM\_PRINTCLIENT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="63916-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63916-132">Requirements</span></span>



| <span data-ttu-id="63916-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="63916-133">Requirement</span></span> | <span data-ttu-id="63916-134">Valor</span><span class="sxs-lookup"><span data-stu-id="63916-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63916-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63916-135">Minimum supported client</span></span><br/> | <span data-ttu-id="63916-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="63916-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="63916-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63916-137">Minimum supported server</span></span><br/> | <span data-ttu-id="63916-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="63916-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="63916-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="63916-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="63916-140"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63916-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63916-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="63916-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63916-142">Visão geral de pintura e desenho</span><span class="sxs-lookup"><span data-stu-id="63916-142">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="63916-143">Pintura e desenho de mensagens</span><span class="sxs-lookup"><span data-stu-id="63916-143">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="63916-144">**AnimateWindow**</span><span class="sxs-lookup"><span data-stu-id="63916-144">**AnimateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[<span data-ttu-id="63916-145">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="63916-145">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="63916-146">**EndPaint**</span><span class="sxs-lookup"><span data-stu-id="63916-146">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="63916-147">**pintura do WM \_**</span><span class="sxs-lookup"><span data-stu-id="63916-147">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
