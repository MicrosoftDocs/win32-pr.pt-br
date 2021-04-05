---
title: Mensagem de WM_MENUCHAR (WinUser. h)
description: Enviado quando um menu está ativo e o usuário pressiona uma tecla que não corresponde a nenhum mnemônico ou tecla de aceleração. Essa mensagem é enviada para a janela que possui o menu.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645232"
---
# <a name="wm_menuchar-message"></a><span data-ttu-id="89d20-105">Mensagem do WM \_ MENUCHAR</span><span class="sxs-lookup"><span data-stu-id="89d20-105">WM\_MENUCHAR message</span></span>

<span data-ttu-id="89d20-106">Enviado quando um menu está ativo e o usuário pressiona uma tecla que não corresponde a nenhum mnemônico ou tecla de aceleração.</span><span class="sxs-lookup"><span data-stu-id="89d20-106">Sent when a menu is active and the user presses a key that does not correspond to any mnemonic or accelerator key.</span></span> <span data-ttu-id="89d20-107">Essa mensagem é enviada para a janela que possui o menu.</span><span class="sxs-lookup"><span data-stu-id="89d20-107">This message is sent to the window that owns the menu.</span></span>


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a><span data-ttu-id="89d20-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89d20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89d20-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89d20-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89d20-110">A palavra de ordem inferior Especifica o código de caractere que corresponde à chave que o usuário pressionou.</span><span class="sxs-lookup"><span data-stu-id="89d20-110">The low-order word specifies the character code that corresponds to the key the user pressed.</span></span>

<span data-ttu-id="89d20-111">A palavra de ordem superior especifica o tipo de menu ativo.</span><span class="sxs-lookup"><span data-stu-id="89d20-111">The high-order word specifies the active menu type.</span></span> <span data-ttu-id="89d20-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="89d20-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="89d20-113">Valor</span><span class="sxs-lookup"><span data-stu-id="89d20-113">Value</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="89d20-114">Significado</span><span class="sxs-lookup"><span data-stu-id="89d20-114">Meaning</span></span>                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="89d20-115"><dt>**MF \_ 0x00000010L pop-up**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="89d20-115"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>       | <span data-ttu-id="89d20-116">Um menu suspenso, submenu ou menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="89d20-116">A drop-down menu, submenu, or shortcut menu.</span></span><br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="89d20-117"><dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt></span><span class="sxs-lookup"><span data-stu-id="89d20-117"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl> | <span data-ttu-id="89d20-118">O menu janela.</span><span class="sxs-lookup"><span data-stu-id="89d20-118">The window menu.</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="89d20-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89d20-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89d20-120">Um identificador para o menu ativo.</span><span class="sxs-lookup"><span data-stu-id="89d20-120">A handle to the active menu.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89d20-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89d20-121">Return value</span></span>

<span data-ttu-id="89d20-122">Um aplicativo que processa essa mensagem deve retornar um dos valores a seguir na palavra de ordem superior do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="89d20-122">An application that processes this message should return one of the following values in the high-order word of the return value.</span></span>



| <span data-ttu-id="89d20-123">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="89d20-123">Return code/value</span></span>                                                                                                                                  | <span data-ttu-id="89d20-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="89d20-124">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89d20-125"><dt>**MNC \_ PERTO**</dt> de <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="89d20-125"><dt>**MNC\_CLOSE**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="89d20-126">Informa ao sistema que ele deve fechar o menu ativo.</span><span class="sxs-lookup"><span data-stu-id="89d20-126">Informs the system that it should close the active menu.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="89d20-127"><dt>**MNC \_ EXECUTAR**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="89d20-127"><dt>**MNC\_EXECUTE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="89d20-128">Informa ao sistema que ele deve escolher o item especificado na palavra de ordem inferior do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="89d20-128">Informs the system that it should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="89d20-129">A janela do proprietário recebe uma mensagem de [**\_ comando do WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="89d20-129">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span><br/> |
| <dl> <span data-ttu-id="89d20-130"><dt>**MNC \_ IGNORAR**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="89d20-130"><dt>**MNC\_IGNORE**</dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="89d20-131">Informa ao sistema que ele deve descartar o caractere que o usuário pressionou e criar um bipe curto no alto-falante do sistema.</span><span class="sxs-lookup"><span data-stu-id="89d20-131">Informs the system that it should discard the character the user pressed and create a short beep on the system speaker.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="89d20-132"><dt>**MNC \_ Selecione**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="89d20-132"><dt>**MNC\_SELECT**</dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="89d20-133">Informa ao sistema que ele deve selecionar o item especificado na palavra de ordem inferior do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="89d20-133">Informs the system that it should select the item specified in the low-order word of the return value.</span></span> <br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="89d20-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="89d20-134">Remarks</span></span>

<span data-ttu-id="89d20-135">A palavra de ordem inferior será ignorada se a palavra de ordem superior contiver 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="89d20-135">The low-order word is ignored if the high-order word contains 0 or 1.</span></span>

<span data-ttu-id="89d20-136">Um aplicativo deve processar essa mensagem quando um acelerador é usado para selecionar um item de menu que exibe um bitmap.</span><span class="sxs-lookup"><span data-stu-id="89d20-136">An application should process this message when an accelerator is used to select a menu item that displays a bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="89d20-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89d20-137">Requirements</span></span>



| <span data-ttu-id="89d20-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="89d20-138">Requirement</span></span> | <span data-ttu-id="89d20-139">Valor</span><span class="sxs-lookup"><span data-stu-id="89d20-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89d20-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89d20-140">Minimum supported client</span></span><br/> | <span data-ttu-id="89d20-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89d20-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="89d20-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89d20-142">Minimum supported server</span></span><br/> | <span data-ttu-id="89d20-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89d20-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="89d20-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="89d20-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="89d20-145"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89d20-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89d20-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="89d20-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="89d20-147">**Referência**</span><span class="sxs-lookup"><span data-stu-id="89d20-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="89d20-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="89d20-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="89d20-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="89d20-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="89d20-150">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="89d20-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="89d20-151">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="89d20-151">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

