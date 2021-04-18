---
title: WM_POINTERCAPTURECHANGED mensagem
description: Enviado para uma janela que está perdendo a captura de um ponteiro de entrada.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- Mensagens de entrada e notificações de WM_POINTERCAPTURECHANGED mensagem
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794015"
---
# <a name="wm_pointercapturechanged-message"></a><span data-ttu-id="3dc75-104">WM_POINTERCAPTURECHANGED mensagem</span><span class="sxs-lookup"><span data-stu-id="3dc75-104">WM_POINTERCAPTURECHANGED message</span></span>

<span data-ttu-id="3dc75-105">Enviado para uma janela que está perdendo a captura de um ponteiro de entrada.</span><span class="sxs-lookup"><span data-stu-id="3dc75-105">Sent to a window that is losing capture of an input pointer.</span></span>

<span data-ttu-id="3dc75-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3dc75-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a><span data-ttu-id="3dc75-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3dc75-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dc75-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3dc75-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3dc75-109">Contém informações sobre o ponteiro de entrada que está sendo perdido.</span><span class="sxs-lookup"><span data-stu-id="3dc75-109">Contains information about the input pointer that is being lost.</span></span> <span data-ttu-id="3dc75-110">Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para obter a ID do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3dc75-110">Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to get the pointer ID.</span></span>

</dd> <dt>

<span data-ttu-id="3dc75-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3dc75-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3dc75-112">Contém um identificador para a janela que está capturando o ponteiro de entrada.</span><span class="sxs-lookup"><span data-stu-id="3dc75-112">Contains a handle to the window that is capturing the input pointer.</span></span> <span data-ttu-id="3dc75-113">Esse valor pode ser nulo se o ponteiro não estiver mais sendo capturado pela janela.</span><span class="sxs-lookup"><span data-stu-id="3dc75-113">This value can be NULL if the pointer is no longer being captured by the window.</span></span>

<span data-ttu-id="3dc75-114">Se essa mensagem for gerada a partir do processamento interno, o valor poderá ser o identificador da janela que recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="3dc75-114">If this message is generated from internal processing, the value can be the handle of the window receiving the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dc75-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3dc75-115">Return value</span></span>

<span data-ttu-id="3dc75-116">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="3dc75-116">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="3dc75-117">Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="3dc75-117">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="3dc75-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dc75-118">Remarks</span></span>

<span data-ttu-id="3dc75-119">Uma janela deve usar essa notificação para interromper o processamento de mensagens subsequentes e iniciar qualquer limpeza necessária para que o ponteiro seja perdido.</span><span class="sxs-lookup"><span data-stu-id="3dc75-119">A window should use this notification to stop processing subsequent messages and initiate any cleanup required for the pointer being lost.</span></span> <span data-ttu-id="3dc75-120">O processamento de gestos associados ao ponteiro também deve ser encerrado (por exemplo, chamando [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) e os contatos restantes associados novamente à janela.</span><span class="sxs-lookup"><span data-stu-id="3dc75-120">Processing of gestures associated with the pointer should also be terminated (for example, by calling [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) and remaining contacts re-associated with the window.</span></span>

<span data-ttu-id="3dc75-121">Normalmente, se uma janela receber a notificação de **WM_POINTERCAPTURECHANGED** , não serão recebidas notificações subsequentes relacionadas ao ponteiro de entrada.</span><span class="sxs-lookup"><span data-stu-id="3dc75-121">Typically, if a window receives the **WM_POINTERCAPTURECHANGED** notification, no subsequent notifications related to the input pointer are received.</span></span> <span data-ttu-id="3dc75-122">Por isso, não dependa de notificações emparelhadas, como [**WM_POINTERENTER**](wm-pointerenter.md) e [**WM_POINTERLEAVE**](wm-pointerleave.md).</span><span class="sxs-lookup"><span data-stu-id="3dc75-122">Because of this, do not depend on paired notifications such as [**WM_POINTERENTER**](wm-pointerenter.md) and [**WM_POINTERLEAVE**](wm-pointerleave.md).</span></span>

<span data-ttu-id="3dc75-123">**WM_POINTERCAPTURECHANGED** não inclui dados de [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="3dc75-123">**WM_POINTERCAPTURECHANGED** does not include [**POINTER_INFO**](/previous-versions/windows/desktop/api) data.</span></span> <span data-ttu-id="3dc75-124">Além do sinalizador de [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) que está sendo definido, os dados retornados por [**GetPointerInfo**](/previous-versions/windows/desktop/api) (ou qualquer variante) são idênticos aos retornados antes da notificação.</span><span class="sxs-lookup"><span data-stu-id="3dc75-124">Other than the [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) flag being set, the data returned by [**GetPointerInfo**](/previous-versions/windows/desktop/api) (or any variant) is identical to that returned prior to the notification.</span></span>

<span data-ttu-id="3dc75-125">Se o aplicativo não processar essa notificação, o [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) poderá gerar uma ou mais mensagens de [**WM_GESTURE**](../wintouch/wm-gesture.md) ou, se um gesto não for reconhecido, o **DefWindowProc** poderá gerar a entrada do mouse.</span><span class="sxs-lookup"><span data-stu-id="3dc75-125">If the application does not process this notification, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages or, if a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="3dc75-126">Se um aplicativo consumir seletivamente alguma entrada de ponteiro e passar o resto para [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), o comportamento resultante será indefinido.</span><span class="sxs-lookup"><span data-stu-id="3dc75-126">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc75-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dc75-127">Requirements</span></span>



| <span data-ttu-id="3dc75-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dc75-128">Requirement</span></span> | <span data-ttu-id="3dc75-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3dc75-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc75-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dc75-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3dc75-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3dc75-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="3dc75-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dc75-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3dc75-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3dc75-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3dc75-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3dc75-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dc75-135"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3dc75-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dc75-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dc75-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc75-137">Mensagens</span><span class="sxs-lookup"><span data-stu-id="3dc75-137">Messages</span></span>](messages.md)
</dt> </dl>

 

