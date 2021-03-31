---
title: Mensagem de WM_CHANGEUISTATE (WinUser. h)
description: Um aplicativo envia a mensagem do WM \_ CHANGEUISTATE para indicar que o estado da interface do usuário deve ser alterado.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645170"
---
# <a name="wm_changeuistate-message"></a><span data-ttu-id="a1d8b-104">Mensagem do WM \_ CHANGEUISTATE</span><span class="sxs-lookup"><span data-stu-id="a1d8b-104">WM\_CHANGEUISTATE message</span></span>

<span data-ttu-id="a1d8b-105">Um aplicativo envia a mensagem do **WM \_ CHANGEUISTATE** para indicar que o estado da interface do usuário deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-105">An application sends the **WM\_CHANGEUISTATE** message to indicate that the UI state should be changed.</span></span>


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a><span data-ttu-id="a1d8b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1d8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1d8b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1d8b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1d8b-108">A palavra de ordem inferior Especifica a ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-108">The low-order word specifies the action to be taken.</span></span> <span data-ttu-id="a1d8b-109">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-109">This member can be one of the following values.</span></span>



| <span data-ttu-id="a1d8b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a1d8b-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="a1d8b-111">Significado</span><span class="sxs-lookup"><span data-stu-id="a1d8b-111">Meaning</span></span>                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <span data-ttu-id="a1d8b-112"><dt>**UIs \_ LIMPAR**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a1d8b-112"><dt>**UIS\_CLEAR**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="a1d8b-113">Os sinalizadores de estado da interface do usuário especificados pela palavra de ordem superior devem ser apagados.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-113">The UI state flags specified by the high-order word should be cleared.</span></span><br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <span data-ttu-id="a1d8b-114"><dt>**UIs \_ INICIALIZAR**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a1d8b-114"><dt>**UIS\_INITIALIZE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="a1d8b-115">Os sinalizadores de estado da interface do usuário especificados pela palavra de ordem superior devem ser alterados com base no último evento de entrada.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-115">The UI state flags specified by the high-order word should be changed based on the last input event.</span></span> <span data-ttu-id="a1d8b-116">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-116">For more information, see Remarks.</span></span><br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <span data-ttu-id="a1d8b-117"><dt>**UIs \_ CONJUNTO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a1d8b-117"><dt>**UIS\_SET**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="a1d8b-118">Os sinalizadores de estado da interface do usuário especificados pela palavra de ordem superior devem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-118">The UI state flags specified by the high-order word should be set.</span></span><br/>                                                                      |



 

<span data-ttu-id="a1d8b-119">A palavra de ordem superior especifica quais elementos de estado da interface do usuário são afetados ou o estilo do controle.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-119">The high-order word specifies which UI state elements are affected or the style of the control.</span></span> <span data-ttu-id="a1d8b-120">Esse membro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-120">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="a1d8b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a1d8b-121">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="a1d8b-122">Significado</span><span class="sxs-lookup"><span data-stu-id="a1d8b-122">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <span data-ttu-id="a1d8b-123"><dt>**UISF \_ ATIVO**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="a1d8b-123"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>          | <span data-ttu-id="a1d8b-124">Um controle deve ser desenhado no estilo usado para controles ativos.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-124">A control should be drawn in the style used for active controls.</span></span><br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <span data-ttu-id="a1d8b-125"><dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL</span><span class="sxs-lookup"><span data-stu-id="a1d8b-125"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="a1d8b-126">Os aceleradores de teclado estão ocultos.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-126">Keyboard accelerators are hidden.</span></span><br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <span data-ttu-id="a1d8b-127"><dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="a1d8b-127"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="a1d8b-128">Os indicadores de foco estão ocultos.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-128">Focus indicators are hidden.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="a1d8b-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1d8b-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1d8b-130">Esse parâmetro não é usado e deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-130">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1d8b-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1d8b-131">Remarks</span></span>

<span data-ttu-id="a1d8b-132">Uma janela deve enviar essa mensagem para ela mesma ou para seu pai quando ela deve alterar os elementos de estado da interface do usuário de todas as janelas na mesma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-132">A window should send this message to itself or its parent when it must change the UI state elements of all windows in the same hierarchy.</span></span> <span data-ttu-id="a1d8b-133">O procedimento de janela deve permitir que [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processe essa mensagem para que toda a árvore de janela tenha um estado de interface de usuário consistente.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-133">The window procedure must let [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) process this message so that the entire window tree has a consistent UI state.</span></span> <span data-ttu-id="a1d8b-134">Quando a janela de nível superior recebe a mensagem do **WM \_ CHANGEUISTATE** , ela envia uma mensagem do [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) com os mesmos parâmetros para todas as janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-134">When the top-level window receives the **WM\_CHANGEUISTATE** message, it sends a [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with the same parameters to all child windows.</span></span> <span data-ttu-id="a1d8b-135">Quando o sistema processa a mensagem do **WM \_ UPDATEUISTATE** , ele faz a alteração no estado da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-135">When the system processes the **WM\_UPDATEUISTATE** message, it makes the change in the UI state.</span></span>

<span data-ttu-id="a1d8b-136">Se a palavra de ordem inferior de *wParam* for \_ inicializada por UIS, o sistema enviará a mensagem do [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) com um estado de interface do usuário com base no último evento de entrada.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-136">If the low-order word of *wParam* is UIS\_INITIALIZE, the system will send the [**WM\_UPDATEUISTATE**](wm-updateuistate.md) message with a UI state based on the last input event.</span></span> <span data-ttu-id="a1d8b-137">Por exemplo, se a última entrada for proveniente do mouse, o sistema ocultará as indicações de teclado. E, se a última entrada for proveniente do teclado, o sistema mostrará as indicações de teclado. Se o estado que resulta do processamento do **WM \_ CHANGEUISTATE** for igual ao estado antigo, o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) não enviará essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="a1d8b-137">For example, if the last input came from the mouse, the system will hide the keyboard cues. And, if the last input came from the keyboard, the system will show the keyboard cues. If the state that results from processing **WM\_CHANGEUISTATE** is the same as the old state, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) does not send this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d8b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1d8b-138">Requirements</span></span>



| <span data-ttu-id="a1d8b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1d8b-139">Requirement</span></span> | <span data-ttu-id="a1d8b-140">Valor</span><span class="sxs-lookup"><span data-stu-id="a1d8b-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d8b-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1d8b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d8b-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a1d8b-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a1d8b-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1d8b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d8b-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a1d8b-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a1d8b-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a1d8b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1d8b-146"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1d8b-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1d8b-147">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a1d8b-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1d8b-148">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a1d8b-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="a1d8b-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a1d8b-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a1d8b-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a1d8b-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a1d8b-151">**QUERYUISTATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a1d8b-151">**WM\_QUERYUISTATE**</span></span>](wm-queryuistate.md)
</dt> <dt>

<span data-ttu-id="a1d8b-152">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="a1d8b-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a1d8b-153">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="a1d8b-153">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

