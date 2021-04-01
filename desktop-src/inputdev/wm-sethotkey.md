---
title: Mensagem de WM_SETHOTKEY (WinUser. h)
description: Enviado a uma janela para associar uma tecla de acesso à janela. Quando o usuário pressiona a tecla de acesso, o sistema ativa a janela.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- Entrada de mouse e teclado de mensagem WM_SETHOTKEY
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "103663827"
---
# <a name="wm_sethotkey-message"></a><span data-ttu-id="b3f99-105">\_Mensagem de SETtecla do WM</span><span class="sxs-lookup"><span data-stu-id="b3f99-105">WM\_SETHOTKEY message</span></span>

<span data-ttu-id="b3f99-106">Enviado a uma janela para associar uma tecla de acesso à janela.</span><span class="sxs-lookup"><span data-stu-id="b3f99-106">Sent to a window to associate a hot key with the window.</span></span> <span data-ttu-id="b3f99-107">Quando o usuário pressiona a tecla de acesso, o sistema ativa a janela.</span><span class="sxs-lookup"><span data-stu-id="b3f99-107">When the user presses the hot key, the system activates the window.</span></span>


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a><span data-ttu-id="b3f99-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3f99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3f99-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3f99-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3f99-110">A palavra de ordem inferior Especifica o código de chave virtual a ser associado à janela.</span><span class="sxs-lookup"><span data-stu-id="b3f99-110">The low-order word specifies the virtual-key code to associate with the window.</span></span>

<span data-ttu-id="b3f99-111">A palavra de ordem superior pode ser um ou mais dos seguintes valores de CommCtrl. h.</span><span class="sxs-lookup"><span data-stu-id="b3f99-111">The high-order word can be one or more of the following values from CommCtrl.h.</span></span>

<span data-ttu-id="b3f99-112">A definição de *wParam* como **NULL** remove a tecla de acesso associada a uma janela.</span><span class="sxs-lookup"><span data-stu-id="b3f99-112">Setting *wParam* to **NULL** removes the hot key associated with a window.</span></span>



| <span data-ttu-id="b3f99-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b3f99-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="b3f99-114">Significado</span><span class="sxs-lookup"><span data-stu-id="b3f99-114">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <span data-ttu-id="b3f99-115"><dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="b3f99-115"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>             | <span data-ttu-id="b3f99-116">tecla ALT</span><span class="sxs-lookup"><span data-stu-id="b3f99-116">ALT key</span></span><br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <span data-ttu-id="b3f99-117"><dt>**HOTKEYF \_ CONTROLE**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="b3f99-117"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="b3f99-118">Tecla CTRL</span><span class="sxs-lookup"><span data-stu-id="b3f99-118">CTRL key</span></span><br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <span data-ttu-id="b3f99-119"><dt>**HOTKEYF \_**</dt> <dt>0x08</dt> ext.</span><span class="sxs-lookup"><span data-stu-id="b3f99-119"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="b3f99-120">Chave estendida</span><span class="sxs-lookup"><span data-stu-id="b3f99-120">Extended key</span></span><br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <span data-ttu-id="b3f99-121"><dt>**HOTKEYF \_ SHIFT**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="b3f99-121"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>       | <span data-ttu-id="b3f99-122">Tecla SHIFT</span><span class="sxs-lookup"><span data-stu-id="b3f99-122">SHIFT key</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="b3f99-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3f99-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3f99-124">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="b3f99-124">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3f99-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3f99-125">Return value</span></span>

<span data-ttu-id="b3f99-126">O valor de retorno é um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="b3f99-126">The return value is one of the following.</span></span>



| <span data-ttu-id="b3f99-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b3f99-127">Return value</span></span>                                                                  | <span data-ttu-id="b3f99-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3f99-128">Description</span></span>                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3f99-129"><dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="b3f99-129"><dt>-1</dt></span></span> </dl> | <span data-ttu-id="b3f99-130">A função não é bem-sucedida; a tecla de acesso é inválida.</span><span class="sxs-lookup"><span data-stu-id="b3f99-130">The function is unsuccessful; the hot key is invalid.</span></span><br/>                        |
| <dl> <span data-ttu-id="b3f99-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b3f99-131"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="b3f99-132">A função não é bem-sucedida; a janela é inválida.</span><span class="sxs-lookup"><span data-stu-id="b3f99-132">The function is unsuccessful; the window is invalid.</span></span><br/>                         |
| <dl> <span data-ttu-id="b3f99-133"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b3f99-133"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="b3f99-134">A função é bem-sucedida e nenhuma outra janela tem a mesma tecla de atalho.</span><span class="sxs-lookup"><span data-stu-id="b3f99-134">The function is successful, and no other window has the same hot key.</span></span><br/>        |
| <dl> <span data-ttu-id="b3f99-135"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b3f99-135"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="b3f99-136">A função foi bem-sucedida, mas outra janela já tem a mesma tecla de atalho.</span><span class="sxs-lookup"><span data-stu-id="b3f99-136">The function is successful, but another window already has the same hot key.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b3f99-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3f99-137">Remarks</span></span>

<span data-ttu-id="b3f99-138">Uma tecla de acesso não pode ser associada a uma janela filho.</span><span class="sxs-lookup"><span data-stu-id="b3f99-138">A hot key cannot be associated with a child window.</span></span>

<span data-ttu-id="b3f99-139">**VK \_ ESCAPE**, **\_ espaço VK** e **\_ guia VK** são teclas de acesso inválidas.</span><span class="sxs-lookup"><span data-stu-id="b3f99-139">**VK\_ESCAPE**, **VK\_SPACE**, and **VK\_TAB** are invalid hot keys.</span></span>

<span data-ttu-id="b3f99-140">Quando o usuário pressiona a tecla de atalho, o sistema gera uma mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) com *wParam* igual a **sc \_ teclaize** e *lParam* igual ao identificador da janela.</span><span class="sxs-lookup"><span data-stu-id="b3f99-140">When the user presses the hot key, the system generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message with *wParam* equal to **SC\_HOTKEY** and *lParam* equal to the window's handle.</span></span> <span data-ttu-id="b3f99-141">Se essa mensagem for passada para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), o sistema trará o último Popup ativo da janela (se existir) ou a própria janela (se não houver nenhuma janela pop-up) para o primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="b3f99-141">If this message is passed on to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the system will bring the window's last active popup (if it exists) or the window itself (if there is no popup window) to the foreground.</span></span>

<span data-ttu-id="b3f99-142">Uma janela pode ter apenas uma tecla de acesso.</span><span class="sxs-lookup"><span data-stu-id="b3f99-142">A window can only have one hot key.</span></span> <span data-ttu-id="b3f99-143">Se a janela já tiver uma tecla de acesso associada a ela, a nova tecla de acesso substituirá a antiga.</span><span class="sxs-lookup"><span data-stu-id="b3f99-143">If the window already has a hot key associated with it, the new hot key replaces the old one.</span></span> <span data-ttu-id="b3f99-144">Se mais de uma janela tiver a mesma tecla de atalho, a janela ativada pela tecla de acesso será aleatória.</span><span class="sxs-lookup"><span data-stu-id="b3f99-144">If more than one window has the same hot key, the window that is activated by the hot key is random.</span></span>

<span data-ttu-id="b3f99-145">Essas teclas de acesso não estão relacionadas às teclas de acesso definidas por [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span><span class="sxs-lookup"><span data-stu-id="b3f99-145">These hot keys are unrelated to the hot keys set by [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3f99-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3f99-146">Requirements</span></span>



| <span data-ttu-id="b3f99-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3f99-147">Requirement</span></span> | <span data-ttu-id="b3f99-148">Valor</span><span class="sxs-lookup"><span data-stu-id="b3f99-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f99-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3f99-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b3f99-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3f99-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b3f99-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3f99-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b3f99-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3f99-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b3f99-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b3f99-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3f99-154"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3f99-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3f99-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3f99-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="b3f99-156">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b3f99-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b3f99-157">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="b3f99-157">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="b3f99-158">**WM \_**</span><span class="sxs-lookup"><span data-stu-id="b3f99-158">**WM\_GETHOTKEY**</span></span>](wm-gethotkey.md)
</dt> <dt>

[<span data-ttu-id="b3f99-159">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="b3f99-159">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="b3f99-160">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b3f99-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b3f99-161">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="b3f99-161">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

