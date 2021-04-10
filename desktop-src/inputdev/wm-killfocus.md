---
title: Mensagem de WM_KILLFOCUS (WinUser. h)
description: Enviado a uma janela imediatamente antes de perder o foco do teclado.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- Entrada de mouse e teclado de mensagem WM_KILLFOCUS
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e3bba54f2cdb500ba2ba691ffd30419d5beff1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009231"
---
# <a name="wm_killfocus-message"></a><span data-ttu-id="56596-104">Mensagem do WM \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="56596-104">WM\_KILLFOCUS message</span></span>

<span data-ttu-id="56596-105">Enviado a uma janela imediatamente antes de perder o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="56596-105">Sent to a window immediately before it loses the keyboard focus.</span></span>


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a><span data-ttu-id="56596-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56596-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56596-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56596-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56596-108">Um identificador para a janela que recebe o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="56596-108">A handle to the window that receives the keyboard focus.</span></span> <span data-ttu-id="56596-109">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="56596-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="56596-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56596-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56596-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="56596-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56596-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56596-112">Return value</span></span>

<span data-ttu-id="56596-113">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="56596-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="56596-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="56596-114">Remarks</span></span>

<span data-ttu-id="56596-115">Se um aplicativo estiver exibindo um cursor, o cursor deverá ser destruído neste ponto.</span><span class="sxs-lookup"><span data-stu-id="56596-115">If an application is displaying a caret, the caret should be destroyed at this point.</span></span>

<span data-ttu-id="56596-116">Ao processar essa mensagem, não faça nenhuma chamada de função que exiba ou ative uma janela.</span><span class="sxs-lookup"><span data-stu-id="56596-116">While processing this message, do not make any function calls that display or activate a window.</span></span> <span data-ttu-id="56596-117">Isso faz com que o thread gere controle e pode fazer com que o aplicativo pare de responder às mensagens.</span><span class="sxs-lookup"><span data-stu-id="56596-117">This causes the thread to yield control and can cause the application to stop responding to messages.</span></span> <span data-ttu-id="56596-118">Para obter mais informações, consulte [deadlocks de mensagem](/windows/desktop/winmsg/about-messages-and-message-queues).</span><span class="sxs-lookup"><span data-stu-id="56596-118">For more information, see [Message Deadlocks](/windows/desktop/winmsg/about-messages-and-message-queues).</span></span>

## <a name="requirements"></a><span data-ttu-id="56596-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56596-119">Requirements</span></span>



| <span data-ttu-id="56596-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="56596-120">Requirement</span></span> | <span data-ttu-id="56596-121">Valor</span><span class="sxs-lookup"><span data-stu-id="56596-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56596-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56596-122">Minimum supported client</span></span><br/> | <span data-ttu-id="56596-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="56596-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="56596-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56596-124">Minimum supported server</span></span><br/> | <span data-ttu-id="56596-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="56596-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="56596-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="56596-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="56596-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56596-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56596-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="56596-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="56596-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="56596-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="56596-130">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="56596-130">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="56596-131">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="56596-131">**WM\_SETFOCUS**</span></span>](wm-setfocus.md)
</dt> <dt>

<span data-ttu-id="56596-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="56596-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="56596-133">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="56596-133">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

