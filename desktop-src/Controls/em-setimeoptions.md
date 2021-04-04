---
title: Mensagem de EM_SETIMEOPTIONS (RichEdit. h)
description: Define as opções do IME (editor de método de entrada).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- Controles de EM_SETIMEOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824527"
---
# <a name="em_setimeoptions-message"></a><span data-ttu-id="fd9a7-104">\_Mensagem em SETIMEOPTIONS</span><span class="sxs-lookup"><span data-stu-id="fd9a7-104">EM\_SETIMEOPTIONS message</span></span>

<span data-ttu-id="fd9a7-105">Define as opções do IME (editor de método de entrada).</span><span class="sxs-lookup"><span data-stu-id="fd9a7-105">Sets the Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="fd9a7-106">Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="fd9a7-107">Não há suporte para ele em nenhuma versão posterior.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="fd9a7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd9a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd9a7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd9a7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd9a7-110">Especifica um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-110">Specifies one of the following values.</span></span>



| <span data-ttu-id="fd9a7-111">Valor</span><span class="sxs-lookup"><span data-stu-id="fd9a7-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="fd9a7-112">Significado</span><span class="sxs-lookup"><span data-stu-id="fd9a7-112">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="fd9a7-113"><dt>**conjunto de ECOOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-113"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="fd9a7-114">Define as opções para as especificadas por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-114">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="fd9a7-115"><dt>**ECOOP \_ ou**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-115"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="fd9a7-116">Combina as opções especificadas com as opções atuais.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-116">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="fd9a7-117"><dt>**ECOOP \_ e**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-117"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="fd9a7-118">Retém somente as opções atuais que também são especificadas por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-118">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="fd9a7-119"><dt>**\_XOR ECOOP**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-119"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="fd9a7-120">Logicamente exclusivas ou as opções atuais com as especificadas por *lParam.*</span><span class="sxs-lookup"><span data-stu-id="fd9a7-120">Logically exclusive OR the current options with those specified by *lParam.*</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fd9a7-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd9a7-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd9a7-122">Especifica um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-122">Specifies one of more of the following values.</span></span>



| <span data-ttu-id="fd9a7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fd9a7-123">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="fd9a7-124">Significado</span><span class="sxs-lookup"><span data-stu-id="fd9a7-124">Meaning</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <span data-ttu-id="fd9a7-125"><dt>**CLOSESTATUSWINDOW do IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-125"><dt>**IMF\_CLOSESTATUSWINDOW**</dt></span></span> </dl> | <span data-ttu-id="fd9a7-126">Fecha a janela de status do IME quando o controle recebe o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-126">Closes the IME status window when the control receives the input focus.</span></span><br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <span data-ttu-id="fd9a7-127"><dt>**FORCEACTIVE do IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-127"><dt>**IMF\_FORCEACTIVE**</dt></span></span> </dl>                   | <span data-ttu-id="fd9a7-128">Ativa o IME quando o controle recebe o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-128">Activates the IME when the control receives the input focus.</span></span><br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <span data-ttu-id="fd9a7-129"><dt>**FORCEDISABLE do IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-129"><dt>**IMF\_FORCEDISABLE**</dt></span></span> </dl>                | <span data-ttu-id="fd9a7-130">Desabilita o IME quando o controle recebe o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-130">Disables the IME when the control receives the input focus.</span></span><br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <span data-ttu-id="fd9a7-131"><dt>**FORCEENABLE do IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-131"><dt>**IMF\_FORCEENABLE**</dt></span></span> </dl>                   | <span data-ttu-id="fd9a7-132">Habilita o IME quando o controle recebe o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-132">Enables the IME when the control receives the input focus.</span></span><br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <span data-ttu-id="fd9a7-133"><dt>**FORCEINACTIVE do IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-133"><dt>**IMF\_FORCEINACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="fd9a7-134">Desativa o IME quando o controle recebe o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-134">Inactivates the IME when the control receives the input focus.</span></span><br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <span data-ttu-id="fd9a7-135"><dt>**FORCENONE do IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-135"><dt>**IMF\_FORCENONE**</dt></span></span> </dl>                         | <span data-ttu-id="fd9a7-136">Desabilita a manipulação do IME.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-136">Disables IME handling.</span></span><br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <span data-ttu-id="fd9a7-137"><dt>**FORCEREMEMBER do IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-137"><dt>**IMF\_FORCEREMEMBER**</dt></span></span> </dl>             | <span data-ttu-id="fd9a7-138">Restaura o status anterior do IME quando o controle recebe o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-138">Restores the previous IME status when the control receives the input focus.</span></span><br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <span data-ttu-id="fd9a7-139"><dt>**MULTIPLEEDIT do IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-139"><dt>**IMF\_MULTIPLEEDIT**</dt></span></span> </dl>                | <span data-ttu-id="fd9a7-140">Especifica que a cadeia de caracteres de composição não será cancelada ou determinada pelas alterações de foco.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-140">Specifies that the composition string will not be canceled or determined by focus changes.</span></span> <span data-ttu-id="fd9a7-141">Isso permite que um aplicativo tenha cadeias de caracteres de composição separadas em cada controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-141">This allows an application to have separate composition strings on each rich edit control.</span></span><br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <span data-ttu-id="fd9a7-142"><dt>**VERTICAL do IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-142"><dt>**IMF\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="fd9a7-143">Observação usada no rich edit 2,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-143">Note used in Rich Edit 2.0 and later.</span></span> <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd9a7-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd9a7-144">Return value</span></span>

<span data-ttu-id="fd9a7-145">Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-145">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="fd9a7-146">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="fd9a7-146">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd9a7-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd9a7-147">Requirements</span></span>



| <span data-ttu-id="fd9a7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd9a7-148">Requirement</span></span> | <span data-ttu-id="fd9a7-149">Valor</span><span class="sxs-lookup"><span data-stu-id="fd9a7-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9a7-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd9a7-150">Minimum supported client</span></span><br/> | <span data-ttu-id="fd9a7-151">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd9a7-151">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd9a7-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd9a7-152">Minimum supported server</span></span><br/> | <span data-ttu-id="fd9a7-153">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd9a7-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd9a7-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd9a7-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd9a7-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd9a7-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd9a7-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd9a7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd9a7-157">**em \_ GETIMEOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="fd9a7-157">**EM\_GETIMEOPTIONS**</span></span>](em-getimeoptions.md)
</dt> </dl>

 

 





