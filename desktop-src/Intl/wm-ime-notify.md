---
description: Enviado a um aplicativo para notificá-lo de alterações na janela do IME. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 20e064b8-2baf-4b4c-8341-36c3e4643eff
title: Mensagem de WM_IME_NOTIFY (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5ab1b2a1fd62d159ab4f216bf9b1bb6892ed69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784109"
---
# <a name="wm_ime_notify-message"></a><span data-ttu-id="e4751-104">WM_IME_NOTIFY mensagem</span><span class="sxs-lookup"><span data-stu-id="e4751-104">WM_IME_NOTIFY message</span></span>

<span data-ttu-id="e4751-105">Enviado a um aplicativo para notificá-lo de alterações na janela do IME.</span><span class="sxs-lookup"><span data-stu-id="e4751-105">Sent to an application to notify it of changes to the IME window.</span></span> <span data-ttu-id="e4751-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e4751-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_NOTIFY,   
  WPARAM wParam,   
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="e4751-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4751-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4751-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="e4751-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e4751-109">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="e4751-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="e4751-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4751-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4751-111">O comando.</span><span class="sxs-lookup"><span data-stu-id="e4751-111">The command.</span></span> <span data-ttu-id="e4751-112">Esse parâmetro pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4751-112">This parameter can have one of the following values.</span></span>

<dl>
<dd><span data-ttu-id="e4751-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="e4751-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="e4751-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="e4751-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="e4751-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="e4751-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="e4751-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span><span class="sxs-lookup"><span data-stu-id="e4751-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span></span></dd> 
<dd><span data-ttu-id="e4751-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="e4751-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="e4751-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="e4751-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="e4751-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="e4751-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="e4751-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="e4751-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="e4751-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="e4751-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="e4751-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span><span class="sxs-lookup"><span data-stu-id="e4751-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span></span></dd> 
<dd><span data-ttu-id="e4751-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="e4751-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span></span></dd> 
<dd><span data-ttu-id="e4751-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span><span class="sxs-lookup"><span data-stu-id="e4751-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span></span></dd> 
<dd><span data-ttu-id="e4751-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="e4751-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="e4751-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4751-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4751-127">Dados específicos do comando, com formato dependente do valor do parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e4751-127">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="e4751-128">Para obter mais informações, consulte a documentação de cada comando.</span><span class="sxs-lookup"><span data-stu-id="e4751-128">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4751-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4751-129">Return value</span></span>

<span data-ttu-id="e4751-130">O valor de retorno depende do comando enviado.</span><span class="sxs-lookup"><span data-stu-id="e4751-130">The return value depends on the command sent.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4751-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4751-131">Remarks</span></span>

<span data-ttu-id="e4751-132">Um aplicativo processa essa mensagem se for responsável por gerenciar a janela do IME.</span><span class="sxs-lookup"><span data-stu-id="e4751-132">An application processes this message if it is responsible for managing the IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4751-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4751-133">Requirements</span></span>



| <span data-ttu-id="e4751-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4751-134">Requirement</span></span> | <span data-ttu-id="e4751-135">Valor</span><span class="sxs-lookup"><span data-stu-id="e4751-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4751-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4751-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e4751-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4751-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="e4751-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4751-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e4751-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4751-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e4751-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e4751-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4751-141"><dt>WinUser. h (incluir Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4751-141"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4751-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4751-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4751-143">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e4751-143">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e4751-144">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="e4751-144">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="e4751-145">IMN_CHANGECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="e4751-145">IMN_CHANGECANDIDATE</span></span>](imn-changecandidate.md)
</dt> <dt>

[<span data-ttu-id="e4751-146">IMN_CLOSECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="e4751-146">IMN_CLOSECANDIDATE</span></span>](imn-closecandidate.md)
</dt> <dt>

[<span data-ttu-id="e4751-147">IMN_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="e4751-147">IMN_CLOSESTATUSWINDOW</span></span>](imn-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="e4751-148">IMN_GUIDELINE</span><span class="sxs-lookup"><span data-stu-id="e4751-148">IMN_GUIDELINE</span></span>](imn-guideline.md)
</dt> <dt>

[<span data-ttu-id="e4751-149">IMN_OPENCANDIDATE</span><span class="sxs-lookup"><span data-stu-id="e4751-149">IMN_OPENCANDIDATE</span></span>](imn-opencandidate.md)
</dt> <dt>

[<span data-ttu-id="e4751-150">IMN_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="e4751-150">IMN_OPENSTATUSWINDOW</span></span>](imn-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="e4751-151">IMN_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="e4751-151">IMN_SETCANDIDATEPOS</span></span>](imn-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="e4751-152">IMN_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="e4751-152">IMN_SETCOMPOSITIONFONT</span></span>](imn-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="e4751-153">IMN_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="e4751-153">IMN_SETCOMPOSITIONWINDOW</span></span>](imn-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="e4751-154">IMN_SETCONVERSIONMODE</span><span class="sxs-lookup"><span data-stu-id="e4751-154">IMN_SETCONVERSIONMODE</span></span>](imn-setconversionmode.md)
</dt> <dt>

[<span data-ttu-id="e4751-155">IMN_SETOPENSTATUS</span><span class="sxs-lookup"><span data-stu-id="e4751-155">IMN_SETOPENSTATUS</span></span>](imn-setopenstatus.md)
</dt> <dt>

[<span data-ttu-id="e4751-156">IMN_SETSENTENCEMODE</span><span class="sxs-lookup"><span data-stu-id="e4751-156">IMN_SETSENTENCEMODE</span></span>](imn-setsentencemode.md)
</dt> <dt>

[<span data-ttu-id="e4751-157">IMN_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="e4751-157">IMN_SETSTATUSWINDOWPOS</span></span>](imn-setstatuswindowpos.md)
</dt> </dl>

 

 
