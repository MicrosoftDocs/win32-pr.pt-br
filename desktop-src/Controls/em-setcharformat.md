---
title: Mensagem de EM_SETCHARFORMAT (RichEdit. h)
description: Define a formatação de caracteres em um controle de edição rico.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- Controles de EM_SETCHARFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086191"
---
# <a name="em_setcharformat-message"></a><span data-ttu-id="c32e9-104">\_Mensagem em SETCHARFORMAT</span><span class="sxs-lookup"><span data-stu-id="c32e9-104">EM\_SETCHARFORMAT message</span></span>

<span data-ttu-id="c32e9-105">Define a formatação de caracteres em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="c32e9-105">Sets character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c32e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c32e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c32e9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c32e9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c32e9-108">Formatação de caractere que se aplica ao controle.</span><span class="sxs-lookup"><span data-stu-id="c32e9-108">Character formatting that applies to the control.</span></span> <span data-ttu-id="c32e9-109">Se esse parâmetro for zero, o formato de caractere padrão será definido.</span><span class="sxs-lookup"><span data-stu-id="c32e9-109">If this parameter is zero, the default character format is set.</span></span> <span data-ttu-id="c32e9-110">Caso contrário, pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c32e9-110">Otherwise, it can be one of the following values.</span></span>



| <span data-ttu-id="c32e9-111">Valor</span><span class="sxs-lookup"><span data-stu-id="c32e9-111">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="c32e9-112">Significado</span><span class="sxs-lookup"><span data-stu-id="c32e9-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <span data-ttu-id="c32e9-113"><dt>**SCF \_ todos**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-113"><dt>**SCF\_ALL**</dt></span></span> </dl>                                     | <span data-ttu-id="c32e9-114">Aplica a formatação a todo o texto no controle.</span><span class="sxs-lookup"><span data-stu-id="c32e9-114">Applies the formatting to all text in the control.</span></span> <span data-ttu-id="c32e9-115">Não é válido **com \_ seleção de SCF** ou **\_ palavra SCF**.</span><span class="sxs-lookup"><span data-stu-id="c32e9-115">Not valid with **SCF\_SELECTION** or **SCF\_WORD**.</span></span><br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <span data-ttu-id="c32e9-116"><dt>**SCF \_ ASSOCIATEFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-116"><dt>**SCF\_ASSOCIATEFONT**</dt></span></span> </dl>       | <span data-ttu-id="c32e9-117">**RichEdit 4,1:** Associa uma fonte a um determinado script, alterando assim a fonte padrão para esse script.</span><span class="sxs-lookup"><span data-stu-id="c32e9-117">**RichEdit 4.1:** Associates a font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="c32e9-118">Para especificar a fonte, use os seguintes membros de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **LCID**.</span><span class="sxs-lookup"><span data-stu-id="c32e9-118">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <span data-ttu-id="c32e9-119"><dt>**SCF \_ ASSOCIATEFONT2**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-119"><dt>**SCF\_ASSOCIATEFONT2**</dt></span></span> </dl>    | <span data-ttu-id="c32e9-120">**RichEdit 4,1:** Associa uma fonte substituta (plano-2) a um determinado script, alterando assim a fonte padrão para esse script.</span><span class="sxs-lookup"><span data-stu-id="c32e9-120">**RichEdit 4.1:** Associates a surrogate (plane-2) font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="c32e9-121">Para especificar a fonte, use os seguintes membros de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **LCID**.</span><span class="sxs-lookup"><span data-stu-id="c32e9-121">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <span data-ttu-id="c32e9-122"><dt>**SCF \_ CHARREPFROMLCID**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-122"><dt>**SCF\_CHARREPFROMLCID**</dt></span></span> </dl> | <span data-ttu-id="c32e9-123">Obtém o caractere repertório do LCID.</span><span class="sxs-lookup"><span data-stu-id="c32e9-123">Gets the character repertoire from the LCID.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="c32e9-124"><dt>**padrão de SCF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-124"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>                         | <span data-ttu-id="c32e9-125">**RichEdit 4,1:** Define a fonte padrão do controle.</span><span class="sxs-lookup"><span data-stu-id="c32e9-125">**RichEdit 4.1:** Sets the default font for the control.</span></span> <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <span data-ttu-id="c32e9-126"><dt>**\_DONTSETDEFAULT SPF**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-126"><dt>**SPF\_DONTSETDEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="c32e9-127">Impede a definição do formato de parágrafo padrão quando o controle rich edit está vazio.</span><span class="sxs-lookup"><span data-stu-id="c32e9-127">Prevents setting the default paragraph format when the rich edit control is empty.</span></span><br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <span data-ttu-id="c32e9-128"><dt>**SCF \_ NOKBUPDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-128"><dt>**SCF\_NOKBUPDATE**</dt></span></span> </dl>                | <span data-ttu-id="c32e9-129">**RichEdit 4,1:** Impede a alternância de teclado para corresponder à fonte.</span><span class="sxs-lookup"><span data-stu-id="c32e9-129">**RichEdit 4.1:** Prevents keyboard switching to match the font.</span></span> <span data-ttu-id="c32e9-130">Por exemplo, se uma fonte em árabe for definida, normalmente o recurso de teclado automático para idiomas bidi altera o teclado para um teclado árabe.</span><span class="sxs-lookup"><span data-stu-id="c32e9-130">For example, if an Arabic font is set, normally the automatic keyboard feature for Bidi languages changes the keyboard to an Arabic keyboard.</span></span><br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="c32e9-131"><dt>**seleção de SCF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-131"><dt>**SCF\_SELECTION**</dt></span></span> </dl>                   | <span data-ttu-id="c32e9-132">Aplica a formatação à seleção atual.</span><span class="sxs-lookup"><span data-stu-id="c32e9-132">Applies the formatting to the current selection.</span></span> <span data-ttu-id="c32e9-133">Se a seleção estiver vazia, a formatação de caractere será aplicada ao ponto de inserção e o novo formato de caractere estará em vigor somente até que o ponto de inserção seja alterado.</span><span class="sxs-lookup"><span data-stu-id="c32e9-133">If the selection is empty, the character formatting is applied to the insertion point, and the new character format is in effect only until the insertion point changes.</span></span><br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <span data-ttu-id="c32e9-134"><dt>**SPF \_ SETpadrão**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-134"><dt>**SPF\_SETDEFAULT**</dt></span></span> </dl>                | <span data-ttu-id="c32e9-135">Define os atributos de formatação de parágrafo padrão.</span><span class="sxs-lookup"><span data-stu-id="c32e9-135">Sets the default paragraph formatting attributes.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <span data-ttu-id="c32e9-136"><dt>**SCF \_ SMARTFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-136"><dt>**SCF\_SMARTFONT**</dt></span></span> </dl>                   | <span data-ttu-id="c32e9-137">Aplique a fonte somente se ela puder manipular o script.</span><span class="sxs-lookup"><span data-stu-id="c32e9-137">Apply the font only if it can handle script.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <span data-ttu-id="c32e9-138"><dt>**SCF \_ USEUIRULES**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-138"><dt>**SCF\_USEUIRULES**</dt></span></span> </dl>                | <span data-ttu-id="c32e9-139">**RichEdit 4,1:** Usado com **a \_ seleção de SCF**.</span><span class="sxs-lookup"><span data-stu-id="c32e9-139">**RichEdit 4.1:** Used with **SCF\_SELECTION**.</span></span> <span data-ttu-id="c32e9-140">Indica que o formato veio de uma barra de ferramentas ou outra ferramenta de interface do usuário, para que as regras de formatação da interface do usuário sejam usadas em vez da formatação literal.</span><span class="sxs-lookup"><span data-stu-id="c32e9-140">Indicates that format came from a toolbar or other UI tool, so UI formatting rules should be used instead of literal formatting.</span></span><br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <span data-ttu-id="c32e9-141"><dt>**palavra do SCF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-141"><dt>**SCF\_WORD**</dt></span></span> </dl>                                  | <span data-ttu-id="c32e9-142">Aplica a formatação à palavra ou às palavras selecionadas.</span><span class="sxs-lookup"><span data-stu-id="c32e9-142">Applies the formatting to the selected word or words.</span></span> <span data-ttu-id="c32e9-143">Se a seleção estiver vazia, mas o ponto de inserção estiver dentro de uma palavra, a formatação será aplicada à palavra.</span><span class="sxs-lookup"><span data-stu-id="c32e9-143">If the selection is empty but the insertion point is inside a word, the formatting is applied to the word.</span></span> <span data-ttu-id="c32e9-144">O valor da **\_ palavra SCF** deve ser usado em conjunto com o valor de **\_ seleção de SCF** .</span><span class="sxs-lookup"><span data-stu-id="c32e9-144">The **SCF\_WORD** value must be used in conjunction with the **SCF\_SELECTION** value.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="c32e9-145">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c32e9-145">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c32e9-146">Ponteiro para uma estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) especificando a formatação de caractere a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c32e9-146">Pointer to a [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure specifying the character formatting to use.</span></span> <span data-ttu-id="c32e9-147">Somente os atributos de formatação especificados pelo membro **dwMask** são alterados.</span><span class="sxs-lookup"><span data-stu-id="c32e9-147">Only the formatting attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="c32e9-148">Microsoft rich edit 2,0 e posterior: esse parâmetro pode ser um ponteiro para uma estrutura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , que é uma extensão da estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="c32e9-148">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="c32e9-149">Antes de enviar a mensagem em **\_ SETCHARFORMAT** , defina o membro **cbSize** da estrutura como `sizeof(CHARFORMAT)` ou `sizeof(CHARFORMAT2)` indique qual versão da estrutura está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="c32e9-149">Before sending the **EM\_SETCHARFORMAT** message, set the structure's **cbSize** member to `sizeof(CHARFORMAT)` or `sizeof(CHARFORMAT2)` indicate which version of the structure is being used.</span></span>

<span data-ttu-id="c32e9-150">Os membros **szFaceName** e **bCharSet** podem ser sobreréguas quando forem inválidos para caracteres, por exemplo: Arial em caracteres kanji.</span><span class="sxs-lookup"><span data-stu-id="c32e9-150">The **szFaceName** and **bCharSet** members may be overruled when invalid for characters, for example: Arial on kanji characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c32e9-151">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c32e9-151">Return value</span></span>

<span data-ttu-id="c32e9-152">Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c32e9-152">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c32e9-153">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="c32e9-153">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c32e9-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="c32e9-154">Remarks</span></span>

<span data-ttu-id="c32e9-155">Se essa mensagem for enviada mais de uma vez com os mesmos parâmetros, o efeito no texto será alternado.</span><span class="sxs-lookup"><span data-stu-id="c32e9-155">If this message is sent more than once with the same parameters, the effect on the text is toggled.</span></span> <span data-ttu-id="c32e9-156">Ou seja, enviar a mensagem uma vez produz o efeito, enviar a mensagem duas vezes cancela o efeito e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c32e9-156">That is, sending the message once produces the effect, sending the message twice cancels the effect, and so forth.</span></span>

## <a name="requirements"></a><span data-ttu-id="c32e9-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c32e9-157">Requirements</span></span>



| <span data-ttu-id="c32e9-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="c32e9-158">Requirement</span></span> | <span data-ttu-id="c32e9-159">Valor</span><span class="sxs-lookup"><span data-stu-id="c32e9-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c32e9-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c32e9-160">Minimum supported client</span></span><br/> | <span data-ttu-id="c32e9-161">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c32e9-161">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c32e9-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c32e9-162">Minimum supported server</span></span><br/> | <span data-ttu-id="c32e9-163">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c32e9-163">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c32e9-164">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c32e9-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="c32e9-165"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c32e9-165"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c32e9-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="c32e9-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="c32e9-167">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c32e9-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c32e9-168">**CHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="c32e9-168">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="c32e9-169">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="c32e9-169">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





