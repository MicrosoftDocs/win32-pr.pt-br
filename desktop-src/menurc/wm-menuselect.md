---
title: Mensagem de WM_MENUSELECT (WinUser. h)
description: Enviado para a janela do proprietário de um menu quando o usuário seleciona um item de menu.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811964"
---
# <a name="wm_menuselect-message"></a><span data-ttu-id="2c642-104">Mensagem do WM \_ MENUSELECT</span><span class="sxs-lookup"><span data-stu-id="2c642-104">WM\_MENUSELECT message</span></span>

<span data-ttu-id="2c642-105">Enviado para a janela do proprietário de um menu quando o usuário seleciona um item de menu.</span><span class="sxs-lookup"><span data-stu-id="2c642-105">Sent to a menu's owner window when the user selects a menu item.</span></span>


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a><span data-ttu-id="2c642-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c642-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c642-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c642-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c642-108">A palavra de ordem inferior Especifica o item de menu ou o índice de submenu.</span><span class="sxs-lookup"><span data-stu-id="2c642-108">The low-order word specifies the menu item or submenu index.</span></span> <span data-ttu-id="2c642-109">Se o item selecionado for um item de comando, esse parâmetro conterá o identificador do item de menu.</span><span class="sxs-lookup"><span data-stu-id="2c642-109">If the selected item is a command item, this parameter contains the identifier of the menu item.</span></span> <span data-ttu-id="2c642-110">Se o item selecionado abrir um menu suspenso ou submenu, esse parâmetro conterá o índice do menu suspenso ou submenu no menu principal, e o parâmetro *lParam* conterá o identificador para o menu principal (clicado); Use a função [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) para obter o identificador de menu para o menu suspenso ou o submenu.</span><span class="sxs-lookup"><span data-stu-id="2c642-110">If the selected item opens a drop-down menu or submenu, this parameter contains the index of the drop-down menu or submenu in the main menu, and the *lParam* parameter contains the handle to the main (clicked) menu; use the [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) function to get the menu handle to the drop-down menu or submenu.</span></span>

<span data-ttu-id="2c642-111">A palavra de ordem superior especifica um ou mais sinalizadores de menu.</span><span class="sxs-lookup"><span data-stu-id="2c642-111">The high-order word specifies one or more menu flags.</span></span> <span data-ttu-id="2c642-112">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c642-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="2c642-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2c642-113">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="2c642-114">Significado</span><span class="sxs-lookup"><span data-stu-id="2c642-114">Meaning</span></span>                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <span data-ttu-id="2c642-115"><dt>**MF \_**</dt> <dt>0X00000004L</dt> de bitmap</span><span class="sxs-lookup"><span data-stu-id="2c642-115"><dt>**MF\_BITMAP**</dt> <dt>0x00000004L</dt></span></span> </dl>                | <span data-ttu-id="2c642-116">Item exibe um bitmap.</span><span class="sxs-lookup"><span data-stu-id="2c642-116">Item displays a bitmap.</span></span><br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <span data-ttu-id="2c642-117"><dt>**MF \_ 0x00000008L VERIFICAda**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2c642-117"><dt>**MF\_CHECKED**</dt> <dt>0x00000008L</dt></span></span> </dl>             | <span data-ttu-id="2c642-118">O item está marcado.</span><span class="sxs-lookup"><span data-stu-id="2c642-118">Item is checked.</span></span><br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <span data-ttu-id="2c642-119"><dt>**MF \_ 0x00000002L DESABILITAdo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2c642-119"><dt>**MF\_DISABLED**</dt> <dt>0x00000002L</dt></span></span> </dl>          | <span data-ttu-id="2c642-120">O item está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2c642-120">Item is disabled.</span></span><br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <span data-ttu-id="2c642-121"><dt>**MF \_ Em cinza**</dt> - <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2c642-121"><dt>**MF\_GRAYED**</dt> <dt>0x00000001L</dt></span></span> </dl>                | <span data-ttu-id="2c642-122">O item está acinzentado.</span><span class="sxs-lookup"><span data-stu-id="2c642-122">Item is grayed.</span></span><br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <span data-ttu-id="2c642-123"><dt>**MF \_ HILITE**</dt> <dt>0x00000080L</dt></span><span class="sxs-lookup"><span data-stu-id="2c642-123"><dt>**MF\_HILITE**</dt> <dt>0x00000080L</dt></span></span> </dl>                | <span data-ttu-id="2c642-124">O item está realçado.</span><span class="sxs-lookup"><span data-stu-id="2c642-124">Item is highlighted.</span></span><br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <span data-ttu-id="2c642-125"><dt>**MF \_ MOUSESELECT**</dt> <dt>0x00008000L</dt></span><span class="sxs-lookup"><span data-stu-id="2c642-125"><dt>**MF\_MOUSESELECT**</dt> <dt>0x00008000L</dt></span></span> </dl> | <span data-ttu-id="2c642-126">Item selecionado com o mouse.</span><span class="sxs-lookup"><span data-stu-id="2c642-126">Item is selected with the mouse.</span></span><br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <span data-ttu-id="2c642-127"><dt>**MF \_ OWNERDRAW**</dt> <dt>0x00000100L</dt></span><span class="sxs-lookup"><span data-stu-id="2c642-127"><dt>**MF\_OWNERDRAW**</dt> <dt>0x00000100L</dt></span></span> </dl>       | <span data-ttu-id="2c642-128">Item é um item desenhado pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="2c642-128">Item is an owner-drawn item.</span></span><br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="2c642-129"><dt>**MF \_ 0x00000010L pop-up**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2c642-129"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>                   | <span data-ttu-id="2c642-130">Item abre um menu suspenso ou submenu.</span><span class="sxs-lookup"><span data-stu-id="2c642-130">Item opens a drop-down menu or submenu.</span></span><br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="2c642-131"><dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt></span><span class="sxs-lookup"><span data-stu-id="2c642-131"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl>             | <span data-ttu-id="2c642-132">O item está contido no menu janela.</span><span class="sxs-lookup"><span data-stu-id="2c642-132">Item is contained in the window menu.</span></span> <span data-ttu-id="2c642-133">O parâmetro *lParam* contém um identificador para o menu associado à mensagem.</span><span class="sxs-lookup"><span data-stu-id="2c642-133">The *lParam* parameter contains a handle to the menu associated with the message.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2c642-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c642-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c642-135">Um identificador para o menu que foi clicado.</span><span class="sxs-lookup"><span data-stu-id="2c642-135">A handle to the menu that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c642-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c642-136">Return value</span></span>

<span data-ttu-id="2c642-137">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="2c642-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c642-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c642-138">Remarks</span></span>

<span data-ttu-id="2c642-139">Se a palavra de ordem superior de *wParam* contiver 0xFFFF e o parâmetro *lParam* contiver **NULL**, o sistema fechará o menu.</span><span class="sxs-lookup"><span data-stu-id="2c642-139">If the high-order word of *wParam* contains 0xFFFF and the *lParam* parameter contains **NULL**, the system has closed the menu.</span></span>

<span data-ttu-id="2c642-140">Não use o valor 1 para a palavra de ordem superior de *wParam*, pois esse valor é especificado como (**uint**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span><span class="sxs-lookup"><span data-stu-id="2c642-140">Do not use the value  1 for the high-order word of *wParam*, because this value is specified as (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span></span> <span data-ttu-id="2c642-141">Se o valor for 0xFFFF, ele será interpretado como 0x0000FFFF, e não 1, devido à conversão para um **uint**.</span><span class="sxs-lookup"><span data-stu-id="2c642-141">If the value is 0xFFFF, it would be interpreted as 0x0000FFFF, not  1, because of the cast to a **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c642-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c642-142">Requirements</span></span>



| <span data-ttu-id="2c642-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c642-143">Requirement</span></span> | <span data-ttu-id="2c642-144">Valor</span><span class="sxs-lookup"><span data-stu-id="2c642-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c642-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c642-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2c642-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2c642-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2c642-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c642-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2c642-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2c642-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c642-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2c642-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c642-150"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c642-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c642-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c642-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c642-152">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2c642-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2c642-153">**GetSubMenu**</span><span class="sxs-lookup"><span data-stu-id="2c642-153">**GetSubMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

<span data-ttu-id="2c642-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2c642-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2c642-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2c642-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2c642-156">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="2c642-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2c642-157">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="2c642-157">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

