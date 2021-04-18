---
description: Postado na fila de mensagens do thread de instalação quando um temporizador expira. A mensagem é postada pela função GetMessage ou PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: Mensagem de WM_TIMER (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c99db67c9c9b3419e477ccd0a78133df453a7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171000"
---
# <a name="wm_timer-message"></a><span data-ttu-id="18ba5-104">Mensagem de timer do WM \_</span><span class="sxs-lookup"><span data-stu-id="18ba5-104">WM\_TIMER message</span></span>

<span data-ttu-id="18ba5-105">Postado na fila de mensagens do thread de instalação quando um temporizador expira.</span><span class="sxs-lookup"><span data-stu-id="18ba5-105">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="18ba5-106">A mensagem é postada pela função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="18ba5-106">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a><span data-ttu-id="18ba5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18ba5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ba5-108">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18ba5-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18ba5-109">O identificador do temporizador.</span><span class="sxs-lookup"><span data-stu-id="18ba5-109">The timer identifier.</span></span>

</dd> <dt>

<span data-ttu-id="18ba5-110">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18ba5-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18ba5-111">Um ponteiro para uma função de retorno de chamada definida pelo aplicativo que foi passada para a função [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) quando o temporizador foi instalado.</span><span class="sxs-lookup"><span data-stu-id="18ba5-111">A pointer to an application-defined callback function that was passed to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function when the timer was installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ba5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18ba5-112">Return value</span></span>

<span data-ttu-id="18ba5-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="18ba5-113">Type: **LRESULT**</span></span>

<span data-ttu-id="18ba5-114">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="18ba5-114">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="18ba5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="18ba5-115">Remarks</span></span>

<span data-ttu-id="18ba5-116">Você pode processar a mensagem fornecendo um caso **de \_ temporizador do WM** no procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="18ba5-116">You can process the message by providing a **WM\_TIMER** case in the window procedure.</span></span> <span data-ttu-id="18ba5-117">Caso contrário, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) chamará a função de retorno de chamada [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) especificada na chamada para a função [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) usada para instalar o temporizador.</span><span class="sxs-lookup"><span data-stu-id="18ba5-117">Otherwise, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) will call the [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) callback function specified in the call to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function used to install the timer.</span></span>

<span data-ttu-id="18ba5-118">A mensagem de **\_ temporizador do WM** é uma mensagem de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="18ba5-118">The **WM\_TIMER** message is a low-priority message.</span></span> <span data-ttu-id="18ba5-119">As funções [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) postam essa mensagem somente quando nenhuma outra mensagem de prioridade mais alta está na fila de mensagens do thread.</span><span class="sxs-lookup"><span data-stu-id="18ba5-119">The [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions post this message only when no other higher-priority messages are in the thread's message queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ba5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18ba5-120">Requirements</span></span>



| <span data-ttu-id="18ba5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="18ba5-121">Requirement</span></span> | <span data-ttu-id="18ba5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="18ba5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18ba5-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18ba5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="18ba5-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="18ba5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="18ba5-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18ba5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="18ba5-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="18ba5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="18ba5-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="18ba5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="18ba5-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18ba5-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ba5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="18ba5-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="18ba5-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="18ba5-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="18ba5-131">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="18ba5-131">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="18ba5-132">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="18ba5-132">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="18ba5-133">**SetTimer**</span><span class="sxs-lookup"><span data-stu-id="18ba5-133">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[<span data-ttu-id="18ba5-134">**TimerProc**</span><span class="sxs-lookup"><span data-stu-id="18ba5-134">**TimerProc**</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

<span data-ttu-id="18ba5-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="18ba5-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="18ba5-136">Temporizadores</span><span class="sxs-lookup"><span data-stu-id="18ba5-136">Timers</span></span>](timers.md)
</dt> </dl>

 

 
