---
description: Notifica uma janela de que sua área não cliente está sendo destruída. A função DestroyWindow envia a mensagem do WM \_ NCDESTROY para a janela após a \_ mensagem do WM Destroy.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: Mensagem de WM_NCDESTROY (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921793"
---
# <a name="wm_ncdestroy-message"></a><span data-ttu-id="6c679-104">Mensagem do WM \_ NCDESTROY</span><span class="sxs-lookup"><span data-stu-id="6c679-104">WM\_NCDESTROY message</span></span>

<span data-ttu-id="6c679-105">Notifica uma janela de que sua área não cliente está sendo destruída.</span><span class="sxs-lookup"><span data-stu-id="6c679-105">Notifies a window that its nonclient area is being destroyed.</span></span> <span data-ttu-id="6c679-106">A função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envia a mensagem do **WM \_ NCDESTROY** para a janela após a mensagem do [**WM \_ Destroy**](wm-destroy.md) .[**O WM \_ Destroy**](wm-destroy.md) é usado para liberar o objeto de memória alocado associado à janela.</span><span class="sxs-lookup"><span data-stu-id="6c679-106">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function sends the **WM\_NCDESTROY** message to the window following the [**WM\_DESTROY**](wm-destroy.md) message.[**WM\_DESTROY**](wm-destroy.md) is used to free the allocated memory object associated with the window.</span></span>

<span data-ttu-id="6c679-107">A mensagem do **WM \_ NCDESTROY** é enviada depois que as janelas filhas são destruídas.</span><span class="sxs-lookup"><span data-stu-id="6c679-107">The **WM\_NCDESTROY** message is sent after the child windows have been destroyed.</span></span> <span data-ttu-id="6c679-108">Por outro lado, o [**WM \_ Destroy**](wm-destroy.md) é enviado antes que as janelas filhas sejam destruídas.</span><span class="sxs-lookup"><span data-stu-id="6c679-108">In contrast, [**WM\_DESTROY**](wm-destroy.md) is sent before the child windows are destroyed.</span></span>

<span data-ttu-id="6c679-109">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6c679-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCDESTROY                    0x0082
```



## <a name="parameters"></a><span data-ttu-id="6c679-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c679-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c679-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c679-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c679-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6c679-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6c679-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c679-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c679-114">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6c679-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c679-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c679-115">Return value</span></span>

<span data-ttu-id="6c679-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="6c679-116">Type: **LRESULT**</span></span>

<span data-ttu-id="6c679-117">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="6c679-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c679-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c679-118">Remarks</span></span>

<span data-ttu-id="6c679-119">Essa mensagem libera qualquer memória alocada internamente para a janela.</span><span class="sxs-lookup"><span data-stu-id="6c679-119">This message frees any memory internally allocated for the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c679-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c679-120">Requirements</span></span>



| <span data-ttu-id="6c679-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c679-121">Requirement</span></span> | <span data-ttu-id="6c679-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6c679-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c679-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c679-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6c679-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6c679-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6c679-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c679-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6c679-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6c679-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c679-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6c679-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c679-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c679-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c679-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c679-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c679-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6c679-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6c679-131">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="6c679-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="6c679-132">**destruição do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6c679-132">**WM\_DESTROY**</span></span>](wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="6c679-133">**NCCREATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6c679-133">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="6c679-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6c679-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6c679-135">Windows</span><span class="sxs-lookup"><span data-stu-id="6c679-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
