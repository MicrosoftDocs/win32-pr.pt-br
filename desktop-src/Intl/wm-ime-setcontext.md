---
description: Enviado a um aplicativo quando uma janela é ativada. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: Mensagem de WM_IME_SETCONTEXT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164512"
---
# <a name="wm_ime_setcontext-message"></a><span data-ttu-id="1de3c-104">\_Mensagem de contexto IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="1de3c-104">WM\_IME\_SETCONTEXT message</span></span>

<span data-ttu-id="1de3c-105">Enviado a um aplicativo quando uma janela é ativada.</span><span class="sxs-lookup"><span data-stu-id="1de3c-105">Sent to an application when a window is activated.</span></span> <span data-ttu-id="1de3c-106">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1de3c-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="1de3c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1de3c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1de3c-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="1de3c-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1de3c-109">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="1de3c-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="1de3c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1de3c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1de3c-111">**True** se a janela estiver ativa e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="1de3c-111">**TRUE** if the window is active, and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="1de3c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1de3c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1de3c-113">Opções de exibição.</span><span class="sxs-lookup"><span data-stu-id="1de3c-113">Display options.</span></span> <span data-ttu-id="1de3c-114">Esse parâmetro pode ter um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1de3c-114">This parameter can have one or more of the following values.</span></span>



| <span data-ttu-id="1de3c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1de3c-115">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="1de3c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1de3c-116">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <span data-ttu-id="1de3c-117"><dt>**SHOWUICOMPOSITIONWINDOW da ISC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1de3c-117"><dt>**ISC\_SHOWUICOMPOSITIONWINDOW**</dt></span></span> </dl> | <span data-ttu-id="1de3c-118">Mostrar a janela de composição por janela de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1de3c-118">Show the composition window by user interface window.</span></span><br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <span data-ttu-id="1de3c-119"><dt>**SHOWUIGUIDWINDOW da ISC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1de3c-119"><dt>**ISC\_SHOWUIGUIDWINDOW**</dt></span></span> </dl>                      | <span data-ttu-id="1de3c-120">Mostrar a janela de guia por janela de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1de3c-120">Show the guide window by user interface window.</span></span><br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <span data-ttu-id="1de3c-121"><dt>**SHOWUISOFTKBD da ISC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1de3c-121"><dt>**ISC\_SHOWUISOFTKBD**</dt></span></span> </dl>                               | <span data-ttu-id="1de3c-122">Mostrar o teclado virtual por janela de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1de3c-122">Show the soft keyboard by user interface window.</span></span><br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <span data-ttu-id="1de3c-123"><dt>**SHOWUICANDIDATEWINDOW da ISC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1de3c-123"><dt>**ISC\_SHOWUICANDIDATEWINDOW**</dt></span></span> </dl>       | <span data-ttu-id="1de3c-124">Mostrar a janela candidata da janela do índice 0 por interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1de3c-124">Show the candidate window of index 0 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="1de3c-125"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 1</dt></span><span class="sxs-lookup"><span data-stu-id="1de3c-125"><dt>ISC\_SHOWUICANDIDATEWINDOW << 1</dt></span></span> </dl>                                                                                        | <span data-ttu-id="1de3c-126">Mostrar a janela candidata do índice 1 pela janela da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1de3c-126">Show the candidate window of index 1 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="1de3c-127"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 2</dt></span><span class="sxs-lookup"><span data-stu-id="1de3c-127"><dt>ISC\_SHOWUICANDIDATEWINDOW << 2</dt></span></span> </dl>                                                                                        | <span data-ttu-id="1de3c-128">Mostrar a janela de candidato do índice 2 pela janela de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1de3c-128">Show the candidate window of index 2 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="1de3c-129"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 3</dt></span><span class="sxs-lookup"><span data-stu-id="1de3c-129"><dt>ISC\_SHOWUICANDIDATEWINDOW << 3</dt></span></span> </dl>                                                                                        | <span data-ttu-id="1de3c-130">Mostrar a janela candidata do índice 3 pela janela da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1de3c-130">Show the candidate window of index 3 by user interface window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1de3c-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1de3c-131">Return value</span></span>

<span data-ttu-id="1de3c-132">Retorna o valor retornado por [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="1de3c-132">Returns the value returned by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span>

## <a name="remarks"></a><span data-ttu-id="1de3c-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="1de3c-133">Remarks</span></span>

<span data-ttu-id="1de3c-134">Se o aplicativo tiver criado uma janela IME, ele deverá chamar [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="1de3c-134">If the application has created an IME window, it should call [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="1de3c-135">Caso contrário, ele deve passar essa mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="1de3c-135">Otherwise, it should pass this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="1de3c-136">Se o aplicativo desenhar a janela de composição, a janela padrão do IME não precisará mostrar sua janela de composição.</span><span class="sxs-lookup"><span data-stu-id="1de3c-136">If the application draws the composition window, the default IME window does not have to show its composition window.</span></span> <span data-ttu-id="1de3c-137">Nesse caso, o aplicativo deve limpar o valor **de \_ SHOWUICOMPOSITIONWINDOW do ISC** do *parâmetro lParam* antes de passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="1de3c-137">In this case, the application must clear the **ISC\_SHOWUICOMPOSITIONWINDOW** value from the *lParam* parameter before passing the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="1de3c-138">Para exibir uma determinada janela de interface do usuário, um aplicativo deve remover o valor correspondente para que o IME não o exiba.</span><span class="sxs-lookup"><span data-stu-id="1de3c-138">To display a certain user interface window, an application should remove the corresponding value so that the IME will not display it.</span></span>

## <a name="requirements"></a><span data-ttu-id="1de3c-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1de3c-139">Requirements</span></span>



| <span data-ttu-id="1de3c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1de3c-140">Requirement</span></span> | <span data-ttu-id="1de3c-141">Valor</span><span class="sxs-lookup"><span data-stu-id="1de3c-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1de3c-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1de3c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1de3c-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1de3c-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="1de3c-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1de3c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1de3c-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1de3c-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="1de3c-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1de3c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="1de3c-147"><dt>WinUser. h (incluir Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1de3c-147"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1de3c-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="1de3c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1de3c-149">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="1de3c-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="1de3c-150">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="1de3c-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="1de3c-151">**ImmIsUIMessage**</span><span class="sxs-lookup"><span data-stu-id="1de3c-151">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
