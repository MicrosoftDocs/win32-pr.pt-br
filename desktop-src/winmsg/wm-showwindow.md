---
description: Enviado a uma janela quando a janela está prestes a ser ocultada ou exibida.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: Mensagem de WM_SHOWWINDOW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296763"
---
# <a name="wm_showwindow-message"></a><span data-ttu-id="e9ae0-103">Mensagem de janela do WM \_</span><span class="sxs-lookup"><span data-stu-id="e9ae0-103">WM\_SHOWWINDOW message</span></span>

<span data-ttu-id="e9ae0-104">Enviado a uma janela quando a janela está prestes a ser ocultada ou exibida.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-104">Sent to a window when the window is about to be hidden or shown.</span></span>

<span data-ttu-id="e9ae0-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e9ae0-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a><span data-ttu-id="e9ae0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9ae0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ae0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9ae0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ae0-108">Indica se uma janela está sendo mostrada.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-108">Indicates whether a window is being shown.</span></span> <span data-ttu-id="e9ae0-109">Se *wParam* for **true**, a janela será mostrada.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-109">If *wParam* is **TRUE**, the window is being shown.</span></span> <span data-ttu-id="e9ae0-110">Se *wParam* for **false**, a janela estará sendo ocultada.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-110">If *wParam* is **FALSE**, the window is being hidden.</span></span>

</dd> <dt>

<span data-ttu-id="e9ae0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9ae0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ae0-112">O status da janela que está sendo mostrada.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-112">The status of the window being shown.</span></span> <span data-ttu-id="e9ae0-113">Se *lParam* for zero, a mensagem foi enviada devido a uma chamada para a função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) . caso contrário, *lParam* será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-113">If *lParam* is zero, the message was sent because of a call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function; otherwise, *lParam* is one of the following values.</span></span>



| <span data-ttu-id="e9ae0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e9ae0-114">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="e9ae0-115">Significado</span><span class="sxs-lookup"><span data-stu-id="e9ae0-115">Meaning</span></span>                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <span data-ttu-id="e9ae0-116"><dt>**SW \_ OTHERUNZOOM**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae0-116"><dt>**SW\_OTHERUNZOOM**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="e9ae0-117">A janela está sendo descoberta porque uma janela maximizada foi restaurada ou minimizada.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-117">The window is being uncovered because a maximize window was restored or minimized.</span></span><br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <span data-ttu-id="e9ae0-118"><dt>**SW \_ OTHERZOOM**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae0-118"><dt>**SW\_OTHERZOOM**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="e9ae0-119">A janela está sendo coberta por outra janela que foi maximizada.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-119">The window is being covered by another window that has been maximized.</span></span><br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <span data-ttu-id="e9ae0-120"><dt>**SW \_ PARENTCLOSING**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae0-120"><dt>**SW\_PARENTCLOSING**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e9ae0-121">A janela do proprietário da janela está sendo minimizada.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-121">The window's owner window is being minimized.</span></span><br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <span data-ttu-id="e9ae0-122"><dt>**SW \_ PARENTOPENING**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae0-122"><dt>**SW\_PARENTOPENING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e9ae0-123">A janela do proprietário da janela está sendo restaurada.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-123">The window's owner window is being restored.</span></span><br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ae0-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9ae0-124">Return value</span></span>

<span data-ttu-id="e9ae0-125">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e9ae0-125">Type: **LRESULT**</span></span>

<span data-ttu-id="e9ae0-126">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-126">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9ae0-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9ae0-127">Remarks</span></span>

<span data-ttu-id="e9ae0-128">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oculta ou mostra a janela, conforme especificado pela mensagem.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-128">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function hides or shows the window, as specified by the message.</span></span> <span data-ttu-id="e9ae0-129">Se uma janela tiver o estilo do [**WS \_ visível**](window-styles.md) quando for criada, a janela receberá essa mensagem depois que ela for criada, mas antes de ser exibida.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-129">If a window has the [**WS\_VISIBLE**](window-styles.md) style when it is created, the window receives this message after it is created, but before it is displayed.</span></span> <span data-ttu-id="e9ae0-130">Uma janela também recebe essa mensagem quando seu estado de visibilidade é alterado pela [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) ou função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="e9ae0-130">A window also receives this message when its visibility state is changed by the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) or [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) function.</span></span>

<span data-ttu-id="e9ae0-131">A mensagem de **\_ janela do WM** não é enviada nas seguintes circunstâncias:</span><span class="sxs-lookup"><span data-stu-id="e9ae0-131">The **WM\_SHOWWINDOW** message is not sent under the following circumstances:</span></span>

-   <span data-ttu-id="e9ae0-132">Quando uma janela de nível superior sobreposta é criada com o estilo [**WS \_ Maxim**](window-styles.md) ou **WS \_ minimize** .</span><span class="sxs-lookup"><span data-stu-id="e9ae0-132">When a top-level, overlapped window is created with the [**WS\_MAXIMIZE**](window-styles.md) or **WS\_MINIMIZE** style.</span></span>
-   <span data-ttu-id="e9ae0-133">Quando o sinalizador de **SW \_ innormal** é especificado na chamada para a função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="e9ae0-133">When the **SW\_SHOWNORMAL** flag is specified in the call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ae0-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9ae0-134">Requirements</span></span>



| <span data-ttu-id="e9ae0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9ae0-135">Requirement</span></span> | <span data-ttu-id="e9ae0-136">Valor</span><span class="sxs-lookup"><span data-stu-id="e9ae0-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ae0-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9ae0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ae0-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e9ae0-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e9ae0-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9ae0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ae0-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e9ae0-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9ae0-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e9ae0-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ae0-142"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae0-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ae0-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9ae0-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9ae0-144">**Referência**</span><span class="sxs-lookup"><span data-stu-id="e9ae0-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e9ae0-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="e9ae0-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="e9ae0-146">**ShowOwnedPopups**</span><span class="sxs-lookup"><span data-stu-id="e9ae0-146">**ShowOwnedPopups**</span></span>](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[<span data-ttu-id="e9ae0-147">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="e9ae0-147">**ShowWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

<span data-ttu-id="e9ae0-148">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="e9ae0-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e9ae0-149">Windows</span><span class="sxs-lookup"><span data-stu-id="e9ae0-149">Windows</span></span>](windows.md)
</dt> </dl>

 

 
