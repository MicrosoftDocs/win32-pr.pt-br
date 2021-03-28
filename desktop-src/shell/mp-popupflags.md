---
description: Representam opções disponíveis ao exibir um menu pop-up.
title: Constantes de MP_POPUPFLAGS (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090838"
---
# <a name="mp_popupflags-constants"></a><span data-ttu-id="3b132-103">\_Constantes POPUPFLAGS MP</span><span class="sxs-lookup"><span data-stu-id="3b132-103">MP\_POPUPFLAGS constants</span></span>

<span data-ttu-id="3b132-104">Representam opções disponíveis ao exibir um menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="3b132-104">Represent options available when displaying a pop-up menu.</span></span>



| <span data-ttu-id="3b132-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="3b132-105">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="3b132-106">Description</span><span class="sxs-lookup"><span data-stu-id="3b132-106">Description</span></span>                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <span data-ttu-id="3b132-107"><dt>**MPPF \_ SETFOCUS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="3b132-107"><dt>**MPPF\_SETFOCUS**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="3b132-108">Dê o foco ao menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="3b132-108">Give the pop-up menu the focus.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <span data-ttu-id="3b132-109"><dt>**MPPF \_ INITIALSELECT**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="3b132-109"><dt>**MPPF\_INITIALSELECT**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="3b132-110">Selecione o primeiro item no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="3b132-110">Select the first item in the pop-up menu.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <span data-ttu-id="3b132-111"><dt>**MPPF \_ Noanimate**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="3b132-111"><dt>**MPPF\_NOANIMATE**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="3b132-112">Não use as animações padrão do sistema, por exemplo, fade-in, ao exibir o menu.</span><span class="sxs-lookup"><span data-stu-id="3b132-112">Do not use the default system animations, for example, fade-in, when displaying the menu.</span></span><br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <span data-ttu-id="3b132-113"><dt>**MPPF \_ TECLADO**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="3b132-113"><dt>**MPPF\_KEYBOARD**</dt> <dt>0x00000010</dt></span></span> </dl>                | <span data-ttu-id="3b132-114">Ative o menu por um atalho de teclado.</span><span class="sxs-lookup"><span data-stu-id="3b132-114">Activate the menu by a keyboard shortcut.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <span data-ttu-id="3b132-115"><dt>**MPPF \_ Reposicionar**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="3b132-115"><dt>**MPPF\_REPOSITION**</dt> <dt>0x00000020</dt></span></span> </dl>          | <span data-ttu-id="3b132-116">Exiba a barra em uma posição diferente, com base nas alterações feitas no menu.</span><span class="sxs-lookup"><span data-stu-id="3b132-116">Display the bar in a different position, based on changes to the menu.</span></span><br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <span data-ttu-id="3b132-117"><dt>**MPPF \_ FORCEZORDER**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="3b132-117"><dt>**MPPF\_FORCEZORDER**</dt> <dt>0x00000040</dt></span></span> </dl>       | <span data-ttu-id="3b132-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3b132-118">Reserved.</span></span> <span data-ttu-id="3b132-119">Não use.</span><span class="sxs-lookup"><span data-stu-id="3b132-119">Do not use.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <span data-ttu-id="3b132-120"><dt>**MPPF \_ FINALSELECT**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="3b132-120"><dt>**MPPF\_FINALSELECT**</dt> <dt>0x00000080</dt></span></span> </dl>       | <span data-ttu-id="3b132-121">Selecione o último item no menu.</span><span class="sxs-lookup"><span data-stu-id="3b132-121">Select the last item in the menu.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <span data-ttu-id="3b132-122"><dt>**MPPF \_ ALINHAr 0x02000000 \_ à esquerda**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3b132-122"><dt>**MPPF\_ALIGN\_LEFT**</dt> <dt>0x02000000</dt></span></span> </dl>         | <span data-ttu-id="3b132-123">**Windows Vista ou posterior**: Alinhe o menu pop-up à esquerda da área especificada no parâmetro *prcExclude* de [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="3b132-123">**Windows Vista or later**: Align the pop-up menu to the left of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span> <span data-ttu-id="3b132-124">Esse é o alinhamento padrão.</span><span class="sxs-lookup"><span data-stu-id="3b132-124">This is the default alignment.</span></span><br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <span data-ttu-id="3b132-125"><dt>**MPPF \_ ALINHAr 0x04000000 \_ à direita**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3b132-125"><dt>**MPPF\_ALIGN\_RIGHT**</dt> <dt>0x04000000</dt></span></span> </dl>      | <span data-ttu-id="3b132-126">**Windows Vista ou posterior**: Alinhe o menu pop-up à direita da área especificada no parâmetro *prcExclude* de [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="3b132-126">**Windows Vista or later**: Align the pop-up menu to the right of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <span data-ttu-id="3b132-127"><dt>**MPPF \_**</dt> <dt>0x20000000</dt> superior</span><span class="sxs-lookup"><span data-stu-id="3b132-127"><dt>**MPPF\_TOP**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="3b132-128">Posicione o menu pop-up acima do ponto inicial especificado no parâmetro *ppt* de [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="3b132-128">Position the pop-up menu above the initial point specified in the *ppt* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <span data-ttu-id="3b132-129"><dt>**MPPF \_**</dt> <dt>0x40000000</dt> esquerdo</span><span class="sxs-lookup"><span data-stu-id="3b132-129"><dt>**MPPF\_LEFT**</dt> <dt>0x40000000</dt></span></span> </dl>                            | <span data-ttu-id="3b132-130">Posicione o menu pop-up à esquerda do ponto inicial.</span><span class="sxs-lookup"><span data-stu-id="3b132-130">Position the pop-up menu to the left of the initial point.</span></span><br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <span data-ttu-id="3b132-131"><dt>**MPPF \_ 0x60000000 à direita**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3b132-131"><dt>**MPPF\_RIGHT**</dt> <dt>0x60000000</dt></span></span> </dl>                         | <span data-ttu-id="3b132-132">Posicione o menu pop-up à direita do ponto inicial.</span><span class="sxs-lookup"><span data-stu-id="3b132-132">Position the pop-up menu to the right of the initial point.</span></span><br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <span data-ttu-id="3b132-133"><dt>**MPPF \_ INFERIOR**</dt> <dt>(int) 0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="3b132-133"><dt>**MPPF\_BOTTOM**</dt> <dt>(int)0x80000000</dt></span></span> </dl>                 | <span data-ttu-id="3b132-134">Posicione o menu pop-up abaixo do ponto inicial.</span><span class="sxs-lookup"><span data-stu-id="3b132-134">Position the pop-up menu below the initial point.</span></span><br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <span data-ttu-id="3b132-135"><dt>**MPPF \_ \_Máscara do PDV**</dt> <dt>(int) 0xE0000000</dt></span><span class="sxs-lookup"><span data-stu-id="3b132-135"><dt>**MPPF\_POS\_MASK**</dt> <dt>(int)0xE0000000</dt></span></span> </dl>          | <span data-ttu-id="3b132-136">A máscara de posição do menu.</span><span class="sxs-lookup"><span data-stu-id="3b132-136">The menu position mask.</span></span><br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="3b132-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b132-137">Remarks</span></span>

<span data-ttu-id="3b132-138">Essas constantes são definidas no arquivo ShObjIdl. h a partir do Windows XP Service Pack 1 (SP1) e do Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b132-138">These constants are defined in the Shobjidl.h file beginning in Windows XP Service Pack 1 (SP1) and Windows Server 2003</span></span>

## <a name="requirements"></a><span data-ttu-id="3b132-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b132-139">Requirements</span></span>



| <span data-ttu-id="3b132-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b132-140">Requirement</span></span> | <span data-ttu-id="3b132-141">Valor</span><span class="sxs-lookup"><span data-stu-id="3b132-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b132-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b132-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3b132-143">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="3b132-143">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b132-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b132-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3b132-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3b132-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b132-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b132-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b132-147"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b132-147"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b132-148">INSERI</span><span class="sxs-lookup"><span data-stu-id="3b132-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b132-149"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b132-149"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b132-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b132-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b132-151">**IMenuPopup::P opup**</span><span class="sxs-lookup"><span data-stu-id="3b132-151">**IMenuPopup::Popup**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[<span data-ttu-id="3b132-152">**ITrackShellMenu::P opup**</span><span class="sxs-lookup"><span data-stu-id="3b132-152">**ITrackShellMenu::Popup**</span></span>](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




