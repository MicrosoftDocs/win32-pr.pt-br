---
title: Mensagem de EM_FINDWORDBREAK (RichEdit. h)
description: Localiza a próxima quebra de palavra antes ou depois da posição do caractere especificado ou recupera informações sobre o caractere nessa posição.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- Controles de EM_FINDWORDBREAK de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455281"
---
# <a name="em_findwordbreak-message"></a><span data-ttu-id="f600d-104">\_Mensagem em FINDWORDBREAK</span><span class="sxs-lookup"><span data-stu-id="f600d-104">EM\_FINDWORDBREAK message</span></span>

<span data-ttu-id="f600d-105">Localiza a próxima quebra de palavra antes ou depois da posição do caractere especificado ou recupera informações sobre o caractere nessa posição.</span><span class="sxs-lookup"><span data-stu-id="f600d-105">Finds the next word break before or after the specified character position or retrieves information about the character at that position.</span></span>

## <a name="parameters"></a><span data-ttu-id="f600d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f600d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f600d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f600d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f600d-108">Especifica a operação Localizar.</span><span class="sxs-lookup"><span data-stu-id="f600d-108">Specifies the find operation.</span></span> <span data-ttu-id="f600d-109">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f600d-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f600d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f600d-110">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="f600d-111">Significado</span><span class="sxs-lookup"><span data-stu-id="f600d-111">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <span data-ttu-id="f600d-112"><dt>**WB \_ classificar**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-112"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>                | <span data-ttu-id="f600d-113">Retorna os sinalizadores de classe de caractere e de quebra de palavra do caractere na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="f600d-113">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <span data-ttu-id="f600d-114"><dt>**\_delimitador WB**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-114"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl>       | <span data-ttu-id="f600d-115">Retornará **true** se o caractere na posição especificada for um delimitador ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f600d-115">Returns **TRUE** if the character at the specified position is a delimiter, or **FALSE** otherwise.</span></span><br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <span data-ttu-id="f600d-116"><dt>**WB \_ à esquerda**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-116"><dt>**WB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="f600d-117">Localiza o caractere mais próximo antes da posição especificada que inicia uma palavra.</span><span class="sxs-lookup"><span data-stu-id="f600d-117">Finds the nearest character before the specified position that begins a word.</span></span><br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <span data-ttu-id="f600d-118"><dt>**WB \_ LEFTBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-118"><dt>**WB\_LEFTBREAK**</dt></span></span> </dl>             | <span data-ttu-id="f600d-119">Localiza a próxima palavra final antes da posição especificada.</span><span class="sxs-lookup"><span data-stu-id="f600d-119">Finds the next word end before the specified position.</span></span> <span data-ttu-id="f600d-120">Esse valor é o mesmo que WB \_ PREVBREAK.</span><span class="sxs-lookup"><span data-stu-id="f600d-120">This value is the same as WB\_PREVBREAK.</span></span><br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <span data-ttu-id="f600d-121"><dt>**WB \_ MOVEWORDLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-121"><dt>**WB\_MOVEWORDLEFT**</dt></span></span> </dl>    | <span data-ttu-id="f600d-122">Localiza o próximo caractere que inicia uma palavra antes da posição especificada.</span><span class="sxs-lookup"><span data-stu-id="f600d-122">Finds the next character that begins a word before the specified position.</span></span> <span data-ttu-id="f600d-123">Esse valor é usado durante o processamento da tecla CTRL + seta para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="f600d-123">This value is used during CTRL+LEFT ARROW key processing.</span></span> <span data-ttu-id="f600d-124">Esse valor é semelhante a WB \_ MOVEWORDPREV.</span><span class="sxs-lookup"><span data-stu-id="f600d-124">This value is the similar to WB\_MOVEWORDPREV.</span></span> <span data-ttu-id="f600d-125">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f600d-125">See Remarks for more information.</span></span><br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <span data-ttu-id="f600d-126"><dt>**WB \_ MOVEWORDRIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-126"><dt>**WB\_MOVEWORDRIGHT**</dt></span></span> </dl> | <span data-ttu-id="f600d-127">Localiza o próximo caractere que inicia uma palavra após a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="f600d-127">Finds the next character that begins a word after the specified position.</span></span> <span data-ttu-id="f600d-128">Esse valor é usado durante o processamento da tecla CTRL + direita.</span><span class="sxs-lookup"><span data-stu-id="f600d-128">This value is used during CTRL+right key processing.</span></span> <span data-ttu-id="f600d-129">Esse valor é semelhante a WB \_ MOVEWORDNEXT.</span><span class="sxs-lookup"><span data-stu-id="f600d-129">This value is similar to WB\_MOVEWORDNEXT.</span></span> <span data-ttu-id="f600d-130">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f600d-130">See Remarks for more information.</span></span><br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <span data-ttu-id="f600d-131"><dt>**WB \_ à direita**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-131"><dt>**WB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="f600d-132">Localiza o próximo caractere que inicia uma palavra após a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="f600d-132">Finds the next character that begins a word after the specified position.</span></span><br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <span data-ttu-id="f600d-133"><dt>**WB \_ RIGHTBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-133"><dt>**WB\_RIGHTBREAK**</dt></span></span> </dl>          | <span data-ttu-id="f600d-134">Localiza o próximo delimitador de fim de palavra após a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="f600d-134">Finds the next end-of-word delimiter after the specified position.</span></span> <span data-ttu-id="f600d-135">Esse valor é o mesmo que WB \_ NEXTBREAK.</span><span class="sxs-lookup"><span data-stu-id="f600d-135">This value is the same as WB\_NEXTBREAK.</span></span><br/>                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="f600d-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f600d-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f600d-137">Posição inicial de caracteres com base em zero.</span><span class="sxs-lookup"><span data-stu-id="f600d-137">Zero-based character starting position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f600d-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f600d-138">Return value</span></span>

<span data-ttu-id="f600d-139">A mensagem retorna um valor com base no parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f600d-139">The message returns a value based on the *wParam* parameter.</span></span>



| <span data-ttu-id="f600d-140">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f600d-140">Return code</span></span>                                                                                    | <span data-ttu-id="f600d-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="f600d-141">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f600d-142"><dt>**wParam**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-142"><dt>**wParam**</dt></span></span> </dl>          | <span data-ttu-id="f600d-143">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f600d-143">Return Value</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="f600d-144"><dt>**WB \_ classificar**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-144"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>    | <span data-ttu-id="f600d-145">Retorna os sinalizadores de classe de caractere e de quebra de palavra do caractere na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="f600d-145">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                |
| <dl> <span data-ttu-id="f600d-146"><dt>**\_delimitador WB**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-146"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl> | <span data-ttu-id="f600d-147">Retornará **true** se o caractere na posição especificada for um delimitador; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="f600d-147">Returns **TRUE** if the character at the specified position is a delimiter; otherwise it returns **FALSE**.</span></span><br/> |
| <dl> <span data-ttu-id="f600d-148"><dt>**Outros**</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-148"><dt>**Others**</dt></span></span> </dl>          | <span data-ttu-id="f600d-149">Retorna o índice de caracteres da quebra de palavra.</span><span class="sxs-lookup"><span data-stu-id="f600d-149">Returns the character index of the word break.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="f600d-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="f600d-150">Remarks</span></span>

<span data-ttu-id="f600d-151">Se *wParam* for WB \_ Left e WB \_ Right, o procedimento de quebra de palavra localizará quebras de palavras somente após os delimitadores.</span><span class="sxs-lookup"><span data-stu-id="f600d-151">If *wParam* is WB\_LEFT and WB\_RIGHT, the word-break procedure finds word breaks only after delimiters.</span></span> <span data-ttu-id="f600d-152">Isso corresponde à funcionalidade de um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="f600d-152">This matches the functionality of an edit control.</span></span> <span data-ttu-id="f600d-153">Se *wParam* for WB \_ MOVEWORDLEFT ou WB \_ MOVEWORDRIGHT, o procedimento de quebra de palavra também comparará classes de caracteres e sinalizadores de quebra de palavras.</span><span class="sxs-lookup"><span data-stu-id="f600d-153">If *wParam* is WB\_MOVEWORDLEFT or WB\_MOVEWORDRIGHT, the word-break procedure also compares character classes and word-break flags.</span></span>

<span data-ttu-id="f600d-154">Para obter informações sobre classes de caracteres e sinalizadores de quebra de palavras, consulte [quebras de linha e de palavras](using-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f600d-154">For information about character classes and word-break flags, see [Word and Line Breaks](using-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f600d-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f600d-155">Requirements</span></span>



| <span data-ttu-id="f600d-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="f600d-156">Requirement</span></span> | <span data-ttu-id="f600d-157">Valor</span><span class="sxs-lookup"><span data-stu-id="f600d-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f600d-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f600d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f600d-159">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f600d-159">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f600d-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f600d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f600d-161">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f600d-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f600d-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f600d-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="f600d-163"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f600d-163"><dt>Richedit.h</dt></span></span> </dl> |



 

 





