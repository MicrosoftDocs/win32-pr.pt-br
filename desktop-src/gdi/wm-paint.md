---
Description: A mensagem de pintura do WM \_ é enviada quando o sistema ou outro aplicativo faz uma solicitação para pintar uma parte da janela de um aplicativo.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: Mensagem de WM_PAINT (WinUser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104968792"
---
# <a name="wm_paint-message"></a><span data-ttu-id="6c459-103">Mensagem de pintura do WM \_</span><span class="sxs-lookup"><span data-stu-id="6c459-103">WM\_PAINT message</span></span>

<span data-ttu-id="6c459-104">A mensagem de **\_ pintura do WM** é enviada quando o sistema ou outro aplicativo faz uma solicitação para pintar uma parte da janela de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c459-104">The **WM\_PAINT** message is sent when the system or another application makes a request to paint a portion of an application's window.</span></span> <span data-ttu-id="6c459-105">A mensagem é enviada quando a função [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) ou [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) é chamada ou pela função [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) quando o aplicativo obtém uma mensagem de **\_ pintura do WM** usando a função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="6c459-105">The message is sent when the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) or [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) function is called, or by the [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) function when the application obtains a **WM\_PAINT** message by using the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>

<span data-ttu-id="6c459-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6c459-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="6c459-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c459-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c459-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c459-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c459-109">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6c459-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6c459-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c459-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c459-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6c459-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c459-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c459-112">Return value</span></span>

<span data-ttu-id="6c459-113">Um aplicativo retornará zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="6c459-113">An application returns zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="6c459-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6c459-114">Example</span></span>

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

<span data-ttu-id="6c459-115">Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) no github.</span><span class="sxs-lookup"><span data-stu-id="6c459-115">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c459-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c459-116">Remarks</span></span>

<span data-ttu-id="6c459-117">A mensagem de **\_ pintura do WM** é gerada pelo sistema e não deve ser enviada por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c459-117">The **WM\_PAINT** message is generated by the system and should not be sent by an application.</span></span> <span data-ttu-id="6c459-118">Para forçar uma janela a desenhar em um contexto de dispositivo específico, use a mensagem do [**WM \_ Print**](wm-print.md) ou [**WM \_ fileclient**](wm-printclient.md) .</span><span class="sxs-lookup"><span data-stu-id="6c459-118">To force a window to draw into a specific device context, use the [**WM\_PRINT**](wm-print.md) or [**WM\_PRINTCLIENT**](wm-printclient.md) message.</span></span> <span data-ttu-id="6c459-119">Observe que isso requer que a janela de destino dê suporte à mensagem do **WM \_ fileclient** .</span><span class="sxs-lookup"><span data-stu-id="6c459-119">Note that this requires the target window to support the **WM\_PRINTCLIENT** message.</span></span> <span data-ttu-id="6c459-120">Os controles mais comuns dão suporte à mensagem do **WM \_ fileclient** .</span><span class="sxs-lookup"><span data-stu-id="6c459-120">Most common controls support the **WM\_PRINTCLIENT** message.</span></span>

<span data-ttu-id="6c459-121">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  valida a região de atualização.</span><span class="sxs-lookup"><span data-stu-id="6c459-121">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function validates the update region.</span></span> <span data-ttu-id="6c459-122">A função também pode enviar a mensagem do [**WM \_ NCPAINT**](wm-ncpaint.md) para o procedimento de janela se o quadro da janela deve ser pintado e enviar a mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) se o plano de fundo da janela precisar ser apagado.</span><span class="sxs-lookup"><span data-stu-id="6c459-122">The function may also send the [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

<span data-ttu-id="6c459-123">O sistema envia essa mensagem quando não há nenhuma outra mensagem na fila de mensagens do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c459-123">The system sends this message when there are no other messages in the application's message queue.</span></span> <span data-ttu-id="6c459-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determina para onde enviar a mensagem; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determina qual mensagem deve ser expedida.</span><span class="sxs-lookup"><span data-stu-id="6c459-124">[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determines where to send the message; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determines which message to dispatch.</span></span> <span data-ttu-id="6c459-125">**GetMessage** retorna a mensagem de **\_ pintura do WM** quando não há nenhuma outra mensagem na fila de mensagens do aplicativo e **DispatchMessage** envia a mensagem para o procedimento de janela apropriado.</span><span class="sxs-lookup"><span data-stu-id="6c459-125">**GetMessage** returns the **WM\_PAINT** message when there are no other messages in the application's message queue, and **DispatchMessage** sends the message to the appropriate window procedure.</span></span>

<span data-ttu-id="6c459-126">Uma janela pode receber mensagens de pintura internas como resultado da chamada de [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) com o \_ sinalizador RDW INTERNALPAINT definido.</span><span class="sxs-lookup"><span data-stu-id="6c459-126">A window may receive internal paint messages as a result of calling [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span> <span data-ttu-id="6c459-127">Nesse caso, a janela pode não ter uma região de atualização.</span><span class="sxs-lookup"><span data-stu-id="6c459-127">In this case, the window may not have an update region.</span></span> <span data-ttu-id="6c459-128">Um aplicativo pode chamar a função [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) para determinar se a janela tem uma região de atualização.</span><span class="sxs-lookup"><span data-stu-id="6c459-128">An application may call the [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) function to determine whether the window has an update region.</span></span> <span data-ttu-id="6c459-129">Se **GetUpdateRect** retornar zero, o aplicativo não precisará chamar as funções [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) e [**endpaintt**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="6c459-129">If **GetUpdateRect** returns zero, the application need not call the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) functions.</span></span>

<span data-ttu-id="6c459-130">Um aplicativo deve verificar se há qualquer pintura interna necessária examinando suas estruturas de dados internas para cada mensagem de **\_ pintura do WM** , pois uma mensagem de **\_ pintura do WM** pode ter sido causada por uma região de atualização não nula e uma chamada para [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) com o \_ sinalizador RDW INTERNALPAINT definido.</span><span class="sxs-lookup"><span data-stu-id="6c459-130">An application must check for any necessary internal painting by looking at its internal data structures for each **WM\_PAINT** message, because a **WM\_PAINT** message may have been caused by both a non-NULL update region and a call to [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="6c459-131">O sistema envia uma mensagem **de \_ pintura do WM** interno apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="6c459-131">The system sends an internal **WM\_PAINT** message only once.</span></span> <span data-ttu-id="6c459-132">Depois que uma mensagem de **\_ pintura do WM** interno for retornada de [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) ou for enviada para uma janela pelo [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), o sistema não publicará nem enviará mais mensagens de **\_ pintura do WM** até que a janela seja invalidada ou até que [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) seja chamado novamente com o \_ sinalizador RDW INTERNALPAINT definido.</span><span class="sxs-lookup"><span data-stu-id="6c459-132">After an internal **WM\_PAINT** message is returned from [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) or is sent to a window by [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), the system does not post or send further **WM\_PAINT** messages until the window is invalidated or until [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) is called again with the RDW\_INTERNALPAINT flag set.</span></span>

<span data-ttu-id="6c459-133">Para alguns controles comuns, o processamento de mensagem padrão do **WM \_ Paint** verifica o parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="6c459-133">For some common controls, the default **WM\_PAINT** message processing checks the *wParam* parameter.</span></span> <span data-ttu-id="6c459-134">Se *wParam* for não nulo, o controle assumirá que o valor é um hDC e pinta usando esse contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c459-134">If *wParam* is non-NULL, the control assumes that the value is an HDC and paints using that device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c459-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c459-135">Requirements</span></span>



| <span data-ttu-id="6c459-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c459-136">Requirement</span></span> | <span data-ttu-id="6c459-137">Valor</span><span class="sxs-lookup"><span data-stu-id="6c459-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c459-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c459-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6c459-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6c459-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6c459-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c459-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6c459-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6c459-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c459-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6c459-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c459-143"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c459-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c459-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c459-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c459-145">Visão geral de pintura e desenho</span><span class="sxs-lookup"><span data-stu-id="6c459-145">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="6c459-146">Pintura e desenho de mensagens</span><span class="sxs-lookup"><span data-stu-id="6c459-146">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="6c459-147">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="6c459-147">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="6c459-148">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="6c459-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="6c459-149">**DispatchMessage**</span><span class="sxs-lookup"><span data-stu-id="6c459-149">**DispatchMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[<span data-ttu-id="6c459-150">**EndPaint**</span><span class="sxs-lookup"><span data-stu-id="6c459-150">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="6c459-151">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="6c459-151">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="6c459-152">**GetUpdateRect**</span><span class="sxs-lookup"><span data-stu-id="6c459-152">**GetUpdateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[<span data-ttu-id="6c459-153">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="6c459-153">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="6c459-154">**RedrawWindow**</span><span class="sxs-lookup"><span data-stu-id="6c459-154">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[<span data-ttu-id="6c459-155">**UpdateWindow**</span><span class="sxs-lookup"><span data-stu-id="6c459-155">**UpdateWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[<span data-ttu-id="6c459-156">**ERASEBKGND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6c459-156">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="6c459-157">**NCPAINT do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6c459-157">**WM\_NCPAINT**</span></span>](wm-ncpaint.md)
</dt> <dt>

[<span data-ttu-id="6c459-158">**impressão do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6c459-158">**WM\_PRINT**</span></span>](wm-print.md)
</dt> <dt>

[<span data-ttu-id="6c459-159">**WM \_ FILEclient**</span><span class="sxs-lookup"><span data-stu-id="6c459-159">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
