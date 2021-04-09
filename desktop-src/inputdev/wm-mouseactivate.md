---
title: Mensagem de WM_MOUSEACTIVATE (WinUser. h)
description: Enviado quando o cursor está em uma janela inativa e o usuário pressiona um botão do mouse. A janela pai receberá essa mensagem somente se a janela filho a passar para a função DefWindowProc.
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- Entrada de mouse e teclado de mensagem WM_MOUSEACTIVATE
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085424"
---
# <a name="wm_mouseactivate-message"></a><span data-ttu-id="44bd2-105">Mensagem do WM \_ MOUSEACTIVATE</span><span class="sxs-lookup"><span data-stu-id="44bd2-105">WM\_MOUSEACTIVATE message</span></span>

<span data-ttu-id="44bd2-106">Enviado quando o cursor está em uma janela inativa e o usuário pressiona um botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="44bd2-106">Sent when the cursor is in an inactive window and the user presses a mouse button.</span></span> <span data-ttu-id="44bd2-107">A janela pai receberá essa mensagem somente se a janela filho a passar para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="44bd2-107">The parent window receives this message only if the child window passes it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="44bd2-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="44bd2-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a><span data-ttu-id="44bd2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44bd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44bd2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44bd2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44bd2-111">Um identificador para a janela pai de nível superior da janela que está sendo ativada.</span><span class="sxs-lookup"><span data-stu-id="44bd2-111">A handle to the top-level parent window of the window being activated.</span></span>

</dd> <dt>

<span data-ttu-id="44bd2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44bd2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44bd2-113">A palavra de ordem inferior Especifica o valor de teste de clique retornado pela função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado do processamento da mensagem [**\_ NCHITTEST do WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="44bd2-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="44bd2-114">Para obter uma lista de valores de teste de clique, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="44bd2-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="44bd2-115">A palavra de ordem superior especifica o identificador da mensagem do mouse gerada quando o usuário pressionou um botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="44bd2-115">The high-order word specifies the identifier of the mouse message generated when the user pressed a mouse button.</span></span> <span data-ttu-id="44bd2-116">A mensagem do mouse é descartada ou postada na janela, dependendo do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="44bd2-116">The mouse message is either discarded or posted to the window, depending on the return value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44bd2-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44bd2-117">Return value</span></span>

<span data-ttu-id="44bd2-118">O valor de retorno especifica se a janela deve ser ativada e se o identificador da mensagem do mouse deve ser Descartado.</span><span class="sxs-lookup"><span data-stu-id="44bd2-118">The return value specifies whether the window should be activated and whether the identifier of the mouse message should be discarded.</span></span> <span data-ttu-id="44bd2-119">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="44bd2-119">It must be one of the following values.</span></span>



| <span data-ttu-id="44bd2-120">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="44bd2-120">Return code/value</span></span>                                                                                                                                          | <span data-ttu-id="44bd2-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="44bd2-121">Description</span></span>                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="44bd2-122"><dt>**Ma \_ ATIVAR**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="44bd2-122"><dt>**MA\_ACTIVATE**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="44bd2-123">Ativa a janela e não descarta a mensagem do mouse.</span><span class="sxs-lookup"><span data-stu-id="44bd2-123">Activates the window, and does not discard the mouse message.</span></span><br/>         |
| <dl> <span data-ttu-id="44bd2-124"><dt>**Ma \_ ACTIVATEANDEAT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="44bd2-124"><dt>**MA\_ACTIVATEANDEAT**</dt> <dt>2</dt></span></span> </dl>   | <span data-ttu-id="44bd2-125">Ativa a janela e descarta a mensagem do mouse.</span><span class="sxs-lookup"><span data-stu-id="44bd2-125">Activates the window, and discards the mouse message.</span></span><br/>                 |
| <dl> <span data-ttu-id="44bd2-126"><dt>**Ma \_ Noativar**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="44bd2-126"><dt>**MA\_NOACTIVATE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="44bd2-127">Não ativa a janela e não descarta a mensagem do mouse.</span><span class="sxs-lookup"><span data-stu-id="44bd2-127">Does not activate the window, and does not discard the mouse message.</span></span><br/> |
| <dl> <span data-ttu-id="44bd2-128"><dt>**Ma \_ NOACTIVATEANDEAT**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="44bd2-128"><dt>**MA\_NOACTIVATEANDEAT**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="44bd2-129">Não ativa a janela, mas descarta a mensagem do mouse.</span><span class="sxs-lookup"><span data-stu-id="44bd2-129">Does not activate the window, but discards the mouse message.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="44bd2-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="44bd2-130">Remarks</span></span>

<span data-ttu-id="44bd2-131">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa a mensagem para a janela pai de uma janela filho antes de qualquer processamento ocorrer.</span><span class="sxs-lookup"><span data-stu-id="44bd2-131">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes the message to a child window's parent window before any processing occurs.</span></span> <span data-ttu-id="44bd2-132">A janela pai determina se a janela filho deve ser ativada.</span><span class="sxs-lookup"><span data-stu-id="44bd2-132">The parent window determines whether to activate the child window.</span></span> <span data-ttu-id="44bd2-133">Se ele ativar a janela filho, a janela pai deverá retornar **ma \_ noactivate** ou **ma \_ NOACTIVATEANDEAT** para impedir que o sistema processe a mensagem ainda mais.</span><span class="sxs-lookup"><span data-stu-id="44bd2-133">If it activates the child window, the parent window should return **MA\_NOACTIVATE** or **MA\_NOACTIVATEANDEAT** to prevent the system from processing the message further.</span></span>

## <a name="requirements"></a><span data-ttu-id="44bd2-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44bd2-134">Requirements</span></span>



| <span data-ttu-id="44bd2-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="44bd2-135">Requirement</span></span> | <span data-ttu-id="44bd2-136">Valor</span><span class="sxs-lookup"><span data-stu-id="44bd2-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44bd2-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44bd2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="44bd2-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44bd2-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="44bd2-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44bd2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="44bd2-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44bd2-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44bd2-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="44bd2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="44bd2-142"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44bd2-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44bd2-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="44bd2-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="44bd2-144">**Referência**</span><span class="sxs-lookup"><span data-stu-id="44bd2-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="44bd2-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="44bd2-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="44bd2-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="44bd2-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="44bd2-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="44bd2-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="44bd2-148">**NCHITTEST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="44bd2-148">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

<span data-ttu-id="44bd2-149">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="44bd2-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="44bd2-150">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="44bd2-150">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

