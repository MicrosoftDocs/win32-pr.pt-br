---
title: Mensagem de EM_SETCTFMODEBIAS (RichEdit. h)
description: Define o ajuste do modo TSF (estrutura de serviços de texto) para um controle de edição rico.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- Controles de EM_SETCTFMODEBIAS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499673"
---
# <a name="em_setctfmodebias-message"></a><span data-ttu-id="6d8b0-104">\_Mensagem em SETCTFMODEBIAS</span><span class="sxs-lookup"><span data-stu-id="6d8b0-104">EM\_SETCTFMODEBIAS message</span></span>

<span data-ttu-id="6d8b0-105">Define o ajuste do modo TSF (estrutura de serviços de texto) para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-105">Sets the Text Services Framework (TSF) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d8b0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d8b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d8b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d8b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d8b0-108">Valor de ajuste do modo.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-108">Mode bias value.</span></span> <span data-ttu-id="6d8b0-109">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-109">This can be one of the following values.</span></span>



| <span data-ttu-id="6d8b0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6d8b0-110">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="6d8b0-111">Significado</span><span class="sxs-lookup"><span data-stu-id="6d8b0-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <span data-ttu-id="6d8b0-112"><dt>**CTFMODEBIAS \_ padrão**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-112"><dt>**CTFMODEBIAS\_DEFAULT**</dt></span></span> </dl>                                           | <span data-ttu-id="6d8b0-113">Não há nenhuma diferença de modo.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-113">There is no mode bias.</span></span><br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <span data-ttu-id="6d8b0-114"><dt>**\_nome de arquivo CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-114"><dt>**CTFMODEBIAS\_FILENAME**</dt></span></span> </dl>                                        | <span data-ttu-id="6d8b0-115">A tendência é de um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-115">The bias is to a filename.</span></span><br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <span data-ttu-id="6d8b0-116"><dt>**nome do CTFMODEBIAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-116"><dt>**CTFMODEBIAS\_NAME**</dt></span></span> </dl>                                                    | <span data-ttu-id="6d8b0-117">A tendência é de um nome.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-117">The bias is to a name.</span></span><br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <span data-ttu-id="6d8b0-118"><dt>**CTFMODEBIAS \_ leitura**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-118"><dt>**CTFMODEBIAS\_READING**</dt></span></span> </dl>                                           | <span data-ttu-id="6d8b0-119">A tendência é a leitura.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-119">The bias is to the reading.</span></span><br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <span data-ttu-id="6d8b0-120"><dt>**CTFMODEBIAS \_ DateTime**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-120"><dt>**CTFMODEBIAS\_DATETIME**</dt></span></span> </dl>                                        | <span data-ttu-id="6d8b0-121">A tendência é de uma data ou hora.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-121">The bias is to a date or time.</span></span><br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <span data-ttu-id="6d8b0-122"><dt>**conversa do CTFMODEBIAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-122"><dt>**CTFMODEBIAS\_CONVERSATION**</dt></span></span> </dl>                            | <span data-ttu-id="6d8b0-123">A tendência é de uma conversa.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-123">The bias is to a conversation.</span></span><br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <span data-ttu-id="6d8b0-124"><dt>**CTFMODEBIAS \_ numeric**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-124"><dt>**CTFMODEBIAS\_NUMERIC**</dt></span></span> </dl>                                           | <span data-ttu-id="6d8b0-125">A tendência é de um número.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-125">The bias is to a number.</span></span><br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <span data-ttu-id="6d8b0-126"><dt>**CTFMODEBIAS \_ Hiragana**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-126"><dt>**CTFMODEBIAS\_HIRAGANA**</dt></span></span> </dl>                                        | <span data-ttu-id="6d8b0-127">A tendência é a cadeias de caracteres hiragana.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-127">The bias is to hiragana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <span data-ttu-id="6d8b0-128"><dt>**CTFMODEBIAS \_ katakana**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-128"><dt>**CTFMODEBIAS\_KATAKANA**</dt></span></span> </dl>                                        | <span data-ttu-id="6d8b0-129">A tendência é a cadeias de caracteres de katakana.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-129">The bias is to katakana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <span data-ttu-id="6d8b0-130"><dt>**CTFMODEBIAS \_ Hangul**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-130"><dt>**CTFMODEBIAS\_HANGUL**</dt></span></span> </dl>                                              | <span data-ttu-id="6d8b0-131">A tendência é de caracteres Hangul.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-131">The bias is to Hangul characters.</span></span><br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <span data-ttu-id="6d8b0-132"><dt>**CTFMODEBIAS \_ HALFWIDTHKATAKANA**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-132"><dt>**CTFMODEBIAS\_HALFWIDTHKATAKANA**</dt></span></span> </dl>             | <span data-ttu-id="6d8b0-133">A tendência é a cadeias de caracteres Katakana de meia largura.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-133">The bias is to half-width katakana strings.</span></span><br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <span data-ttu-id="6d8b0-134"><dt>**CTFMODEBIAS \_ FULLWIDTHALPHANUMERIC**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-134"><dt>**CTFMODEBIAS\_FULLWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="6d8b0-135">A tendência é de caracteres alfanuméricos de largura total.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-135">The bias is to full-width alphanumeric characters.</span></span><br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <span data-ttu-id="6d8b0-136"><dt>**CTFMODEBIAS \_ HALFWIDTHALPHANUMERIC**</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-136"><dt>**CTFMODEBIAS\_HALFWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="6d8b0-137">A tendência é a caracteres alfanuméricos de meia largura.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-137">The bias is to half-width alphanumeric characters.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6d8b0-138">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d8b0-138">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d8b0-139">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-139">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d8b0-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d8b0-140">Return value</span></span>

<span data-ttu-id="6d8b0-141">Se for bem-sucedido, o valor de retorno será o novo valor de tendência do modo TSF.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-141">If successful, the return value is the new TSF mode bias value.</span></span> <span data-ttu-id="6d8b0-142">Se não for bem-sucedida, o valor de retorno será o antigo valor de tendência do modo TSF.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-142">If unsuccessful, the return value is the old TSF mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d8b0-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d8b0-143">Remarks</span></span>

<span data-ttu-id="6d8b0-144">Quando um aplicativo de edição rica da Microsoft usa o TSF, ele pode selecionar a tendência do modo TSF.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-144">When a Microsoft Rich Edit application uses TSF, it can select the TSF mode bias.</span></span> <span data-ttu-id="6d8b0-145">Essa mensagem define os critérios pelos quais uma opção alternativa aparece na parte superior da lista para seleção.</span><span class="sxs-lookup"><span data-stu-id="6d8b0-145">This message sets the criteria by which an alternative choice appears at the top of the list for selection.</span></span>

<span data-ttu-id="6d8b0-146">Para definir a tendência de modo para o IME (editor de método de entrada), use em [**\_ SETIMEMODEBIAS**](em-setimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="6d8b0-146">To set the mode bias for the Input Method Editor (IME), use [**EM\_SETIMEMODEBIAS**](em-setimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d8b0-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d8b0-147">Requirements</span></span>



| <span data-ttu-id="6d8b0-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d8b0-148">Requirement</span></span> | <span data-ttu-id="6d8b0-149">Valor</span><span class="sxs-lookup"><span data-stu-id="6d8b0-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d8b0-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d8b0-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6d8b0-151">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="6d8b0-151">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d8b0-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d8b0-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6d8b0-153">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d8b0-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d8b0-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d8b0-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d8b0-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d8b0-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d8b0-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d8b0-156">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d8b0-157">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6d8b0-157">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6d8b0-158">**em \_ GETCTFMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="6d8b0-158">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="6d8b0-159">**em \_ SETIMEMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="6d8b0-159">**EM\_SETIMEMODEBIAS**</span></span>](em-setimemodebias.md)
</dt> </dl>

 

 





