---
title: Mensagem de WM_UPDATEUISTATE (WinUser. h)
description: Um aplicativo envia a mensagem do WM \_ UPDATEUISTATE para alterar o estado da interface do usuário para a janela especificada e todas as suas janelas filhas.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 003d9ca45b357a7d0ebc172000b1e2c01505db8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086480"
---
# <a name="wm_updateuistate-message"></a><span data-ttu-id="e3ed0-104">Mensagem do WM \_ UPDATEUISTATE</span><span class="sxs-lookup"><span data-stu-id="e3ed0-104">WM\_UPDATEUISTATE message</span></span>

<span data-ttu-id="e3ed0-105">Um aplicativo envia a mensagem do **WM \_ UPDATEUISTATE** para alterar o estado da interface do usuário para a janela especificada e todas as suas janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-105">An application sends the **WM\_UPDATEUISTATE** message to change the UI state for the specified window and all its child windows.</span></span>


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a><span data-ttu-id="e3ed0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3ed0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3ed0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3ed0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3ed0-108">A palavra de ordem inferior Especifica a ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-108">The low-order word specifies the action to be performed.</span></span> <span data-ttu-id="e3ed0-109">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e3ed0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e3ed0-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="e3ed0-111">Significado</span><span class="sxs-lookup"><span data-stu-id="e3ed0-111">Meaning</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="e3ed0-112"><dt>**UIs \_ LIMPAR**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e3ed0-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="e3ed0-113">O elemento de estado da interface do usuário especificado pela palavra de ordem superior deve estar oculto.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-113">The UI state element specified by the high-order word should be hidden.</span></span><br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="e3ed0-114"><dt>**UIs \_ INICIALIZAR**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e3ed0-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e3ed0-115">O elemento de estado da interface do usuário especificado pela palavra de ordem superior deve ser alterado com base no último evento de entrada.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-115">The UI state element specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="e3ed0-116">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="e3ed0-117"><dt>**UIs \_ CONJUNTO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e3ed0-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="e3ed0-118">O elemento de estado da interface do usuário especificado pela palavra de ordem superior deve estar visível.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-118">The UI state element specified by the high-order word should be visible.</span></span><br/>                                                                  |



 

<span data-ttu-id="e3ed0-119">A palavra de ordem superior especifica quais elementos de estado da interface do usuário são afetados ou o estilo do controle.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="e3ed0-120">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-120">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="e3ed0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e3ed0-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="e3ed0-122">Significado</span><span class="sxs-lookup"><span data-stu-id="e3ed0-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="e3ed0-123"><dt>**UISF \_ ATIVO**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="e3ed0-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="e3ed0-124">Um controle deve ser desenhado no estilo usado para controles ativos.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="e3ed0-125"><dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL</span><span class="sxs-lookup"><span data-stu-id="e3ed0-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="e3ed0-126">Aceleradores de teclado.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-126">Keyboard accelerators.</span></span><br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="e3ed0-127"><dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="e3ed0-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="e3ed0-128">Indicadores de foco.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-128">Focus indicators.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="e3ed0-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3ed0-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3ed0-130">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3ed0-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3ed0-131">Remarks</span></span>

<span data-ttu-id="e3ed0-132">Uma janela deve enviar essa mensagem para alterar o estado da interface do usuário de todas as janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-132">A window should send this message to change the UI state of all its child windows.</span></span> <span data-ttu-id="e3ed0-133">Ao contrário da mensagem do [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) , que é uma notificação, quando o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processa a mensagem **\_ UPDATEUISTATE do WM** , ele altera o estado da interface do usuário e propaga as alterações para todas as janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-133">In contrast to the [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message, which is a notification, when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processes the **WM\_UPDATEUISTATE** message it changes the UI state and propagates the changes to all child windows.</span></span>

<span data-ttu-id="e3ed0-134">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) atualiza o estado da interface do usuário de acordo com o valor *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e3ed0-134">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function updates the UI state according to the *wParam* value.</span></span> <span data-ttu-id="e3ed0-135">Se o estado da interface do usuário for modificado, a função enviará a mensagem a todas as janelas filho imediatas.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-135">If the UI state is modified, the function sends the message to all the immediate child windows.</span></span> <span data-ttu-id="e3ed0-136">O **DefWindowProc** também envia essa mensagem quando recebe uma mensagem do [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) notificando o sistema de que uma janela filho pretende modificar o estado da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e3ed0-136">**DefWindowProc** also sends this message when it receives a [**WM\_CHANGEUISTATE**](wm-changeuistate.md) message notifying the system that a child window intends to modify the UI state.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ed0-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3ed0-137">Requirements</span></span>



| <span data-ttu-id="e3ed0-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3ed0-138">Requirement</span></span> | <span data-ttu-id="e3ed0-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e3ed0-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ed0-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3ed0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ed0-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e3ed0-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e3ed0-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3ed0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ed0-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e3ed0-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e3ed0-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e3ed0-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3ed0-145"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3ed0-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3ed0-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3ed0-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="e3ed0-147">**Referência**</span><span class="sxs-lookup"><span data-stu-id="e3ed0-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e3ed0-148">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="e3ed0-148">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="e3ed0-149">**CHANGEUISTATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="e3ed0-149">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="e3ed0-150">**QUERYUISTATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="e3ed0-150">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="e3ed0-151">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="e3ed0-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e3ed0-152">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="e3ed0-152">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

