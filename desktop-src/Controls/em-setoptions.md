---
title: Mensagem de EM_SETOPTIONS (RichEdit. h)
description: Define as opções para um controle de edição rico.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- Controles de EM_SETOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085469"
---
# <a name="em_setoptions-message"></a><span data-ttu-id="313ad-104">\_Mensagem em SEToptionss</span><span class="sxs-lookup"><span data-stu-id="313ad-104">EM\_SETOPTIONS message</span></span>

<span data-ttu-id="313ad-105">Define as opções para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="313ad-105">Sets the options for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="313ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="313ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="313ad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="313ad-108">Especifica a operação, que pode ser um desses valores.</span><span class="sxs-lookup"><span data-stu-id="313ad-108">Specifies the operation, which can be one of these values.</span></span>



| <span data-ttu-id="313ad-109">Valor</span><span class="sxs-lookup"><span data-stu-id="313ad-109">Value</span></span>                                                                                                                                             | <span data-ttu-id="313ad-110">Significado</span><span class="sxs-lookup"><span data-stu-id="313ad-110">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="313ad-111"><dt>**conjunto de ECOOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-111"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="313ad-112">Define as opções para as especificadas por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="313ad-112">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="313ad-113"><dt>**ECOOP \_ ou**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-113"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="313ad-114">Combina as opções especificadas com as opções atuais.</span><span class="sxs-lookup"><span data-stu-id="313ad-114">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="313ad-115"><dt>**ECOOP \_ e**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-115"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="313ad-116">Retém somente as opções atuais que também são especificadas por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="313ad-116">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="313ad-117"><dt>**\_XOR ECOOP**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-117"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="313ad-118">Logicamente exclusivas ou as opções atuais com as especificadas por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="313ad-118">Logically exclusive OR the current options with those specified by *lParam*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="313ad-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="313ad-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="313ad-120">Especifica um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="313ad-120">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="313ad-121">Valor</span><span class="sxs-lookup"><span data-stu-id="313ad-121">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="313ad-122">Significado</span><span class="sxs-lookup"><span data-stu-id="313ad-122">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <span data-ttu-id="313ad-123"><dt>**AUTOWORDSELECTION de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-123"><dt>**ECO\_AUTOWORDSELECTION**</dt></span></span> </dl> | <span data-ttu-id="313ad-124">Seleção automática de palavra ao clicar duas vezes.</span><span class="sxs-lookup"><span data-stu-id="313ad-124">Automatic selection of word on double-click.</span></span><br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <span data-ttu-id="313ad-125"><dt>**AUTOVSCROLL de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-125"><dt>**ECO\_AUTOVSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="313ad-126">O mesmo que [**s \_ AUTOVSCROLL**](rich-edit-control-styles.md) estilo.</span><span class="sxs-lookup"><span data-stu-id="313ad-126">Same as [**ES\_AUTOVSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <span data-ttu-id="313ad-127"><dt>**AUTOHSCROLL de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-127"><dt>**ECO\_AUTOHSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="313ad-128">O mesmo que [**s \_ AUTOHSCROLL**](rich-edit-control-styles.md) estilo.</span><span class="sxs-lookup"><span data-stu-id="313ad-128">Same as [**ES\_AUTOHSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <span data-ttu-id="313ad-129"><dt>**NOHIDESEL de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-129"><dt>**ECO\_NOHIDESEL**</dt></span></span> </dl>                         | <span data-ttu-id="313ad-130">O mesmo que [**s \_ NOHIDESEL**](rich-edit-control-styles.md) estilo.</span><span class="sxs-lookup"><span data-stu-id="313ad-130">Same as [**ES\_NOHIDESEL**](rich-edit-control-styles.md) style.</span></span><br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <span data-ttu-id="313ad-131"><dt>**\_somente leitura do eco**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-131"><dt>**ECO\_READONLY**</dt></span></span> </dl>                            | <span data-ttu-id="313ad-132">O mesmo que o estilo [**\_ ReadOnly**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="313ad-132">Same as [**ES\_READONLY**](rich-edit-control-styles.md) style.</span></span><br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <span data-ttu-id="313ad-133"><dt>**WANTRETURN de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-133"><dt>**ECO\_WANTRETURN**</dt></span></span> </dl>                      | <span data-ttu-id="313ad-134">O mesmo que [**s \_ WANTRETURN**](rich-edit-control-styles.md) estilo.</span><span class="sxs-lookup"><span data-stu-id="313ad-134">Same as [**ES\_WANTRETURN**](rich-edit-control-styles.md) style.</span></span><br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <span data-ttu-id="313ad-135"><dt>**SELECTIONBAR de ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-135"><dt>**ECO\_SELECTIONBAR**</dt></span></span> </dl>                | <span data-ttu-id="313ad-136">O mesmo que [**s \_ SELECTIONBAR**](rich-edit-control-styles.md) estilo.</span><span class="sxs-lookup"><span data-stu-id="313ad-136">Same as [**ES\_SELECTIONBAR**](rich-edit-control-styles.md) style.</span></span><br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <span data-ttu-id="313ad-137"><dt>**VERTICAL do ECO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-137"><dt>**ECO\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="313ad-138">O mesmo que o estilo [**\_ vertical es**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="313ad-138">Same as [**ES\_VERTICAL**](rich-edit-control-styles.md) style.</span></span> <span data-ttu-id="313ad-139">Disponível apenas em versões do idioma asiático.</span><span class="sxs-lookup"><span data-stu-id="313ad-139">Available in Asian-language versions only.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="313ad-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="313ad-140">Return value</span></span>

<span data-ttu-id="313ad-141">Essa mensagem retorna as opções atuais do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="313ad-141">This message returns the current options of the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="313ad-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="313ad-142">Requirements</span></span>



| <span data-ttu-id="313ad-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="313ad-143">Requirement</span></span> | <span data-ttu-id="313ad-144">Valor</span><span class="sxs-lookup"><span data-stu-id="313ad-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="313ad-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="313ad-145">Minimum supported client</span></span><br/> | <span data-ttu-id="313ad-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="313ad-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="313ad-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="313ad-147">Minimum supported server</span></span><br/> | <span data-ttu-id="313ad-148">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="313ad-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="313ad-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="313ad-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="313ad-150"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="313ad-150"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="313ad-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="313ad-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313ad-152">**Estilos de controle de edição avançados**</span><span class="sxs-lookup"><span data-stu-id="313ad-152">**Rich Edit Control Styles**</span></span>](rich-edit-control-styles.md)
</dt> </dl>

 

 





