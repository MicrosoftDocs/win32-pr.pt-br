---
title: Mensagem de EM_GETIMEPROPERTY (RichEdit. h)
description: Recupera a propriedade e os recursos do IME (editor de método de entrada) associado à localidade de entrada atual.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- Controles de EM_GETIMEPROPERTY de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c081aa99c99f4cd0995c0f9d2f5256e2958dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086037"
---
# <a name="em_getimeproperty-message"></a><span data-ttu-id="5e660-104">\_Mensagem em GETIMEPROPERTY</span><span class="sxs-lookup"><span data-stu-id="5e660-104">EM\_GETIMEPROPERTY message</span></span>

<span data-ttu-id="5e660-105">Recupera a propriedade e os recursos do IME (editor de método de entrada) associado à localidade de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="5e660-105">Retrieves the property and capabilities of the Input Method Editor (IME) associated with the current input locale.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e660-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e660-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e660-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e660-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e660-108">Especifica o tipo de informações de propriedade a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="5e660-108">Specifies the type of property information to retrieve.</span></span> <span data-ttu-id="5e660-109">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e660-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="5e660-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5e660-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="5e660-111">Significado</span><span class="sxs-lookup"><span data-stu-id="5e660-111">Meaning</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <span data-ttu-id="5e660-112"><dt>**\_Propriedade IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="5e660-112"><dt>**IGP\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="5e660-113">Informações de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5e660-113">Property information.</span></span><br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <span data-ttu-id="5e660-114"><dt>**conversão de IGP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e660-114"><dt>**IGP\_CONVERSION**</dt></span></span> </dl>          | <span data-ttu-id="5e660-115">Recursos de conversão.</span><span class="sxs-lookup"><span data-stu-id="5e660-115">Conversion capabilities.</span></span> <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <span data-ttu-id="5e660-116"><dt>**sentença de IGP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e660-116"><dt>**IGP\_SENTENCE**</dt></span></span> </dl>                | <span data-ttu-id="5e660-117">Recursos do modo de sentença.</span><span class="sxs-lookup"><span data-stu-id="5e660-117">Sentence mode capabilities.</span></span> <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <span data-ttu-id="5e660-118"><dt>**\_interface do usuário do IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="5e660-118"><dt>**IGP\_UI**</dt></span></span> </dl>                                  | <span data-ttu-id="5e660-119">Recursos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5e660-119">User interface capabilities.</span></span> <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <span data-ttu-id="5e660-120"><dt>**SETCOMPSTR de IGP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e660-120"><dt>**IGP\_SETCOMPSTR**</dt></span></span> </dl>          | <span data-ttu-id="5e660-121">Funcionalidades de cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="5e660-121">Composition string capabilities.</span></span> <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <span data-ttu-id="5e660-122"><dt>**seleção de IGP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e660-122"><dt>**IGP\_SELECT**</dt></span></span> </dl>                      | <span data-ttu-id="5e660-123">Funcionalidades de herança de seleção.</span><span class="sxs-lookup"><span data-stu-id="5e660-123">Selection inheritance capabilities.</span></span> <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <span data-ttu-id="5e660-124"><dt>**GETIMEVERSION de IGP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e660-124"><dt>**IGP\_GETIMEVERSION**</dt></span></span> </dl> | <span data-ttu-id="5e660-125">Recupera o número de versão do sistema para o qual o IME especificado foi criado.</span><span class="sxs-lookup"><span data-stu-id="5e660-125">Retrieves the system version number for which the specified IME was created.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="5e660-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e660-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e660-127">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5e660-127">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e660-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e660-128">Return value</span></span>

<span data-ttu-id="5e660-129">Retorna a propriedade ou o valor de funcionalidade, dependendo do valor do parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5e660-129">Returns the property or capability value, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="5e660-130">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="5e660-130">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e660-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e660-131">Remarks</span></span>

<span data-ttu-id="5e660-132">Se *wParam* for \_ a propriedade IGP, ele retornará um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e660-132">If *wParam* is IGP\_PROPERTY, it returns one or more of the following values.</span></span>



| <span data-ttu-id="5e660-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e660-133">Requirement</span></span> | <span data-ttu-id="5e660-134">Valor</span><span class="sxs-lookup"><span data-stu-id="5e660-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e660-135">\_prop IME \_ no \_ cursor</span><span class="sxs-lookup"><span data-stu-id="5e660-135">IME\_PROP\_AT\_CARET</span></span>                | <span data-ttu-id="5e660-136">Se definido, a janela de conversão estará na posição do cursor.</span><span class="sxs-lookup"><span data-stu-id="5e660-136">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="5e660-137">Se estiver claro, a janela estará perto da posição do cursor.</span><span class="sxs-lookup"><span data-stu-id="5e660-137">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="5e660-138">\_ \_ IU especial de prop IME \_</span><span class="sxs-lookup"><span data-stu-id="5e660-138">IME\_PROP\_SPECIAL\_UI</span></span>              | <span data-ttu-id="5e660-139">Se definido, o IME tem uma interface do usuário não padrão.</span><span class="sxs-lookup"><span data-stu-id="5e660-139">If set, IME has a nonstandard user interface.</span></span> <span data-ttu-id="5e660-140">O aplicativo não deve desenhar na janela do IME.</span><span class="sxs-lookup"><span data-stu-id="5e660-140">The application should not draw in the IME window.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="5e660-141">O IME \_ prop \_ CANDLIST \_ começa \_ em \_ 1</span><span class="sxs-lookup"><span data-stu-id="5e660-141">IME\_PROP\_CANDLIST\_START\_FROM\_1</span></span> | <span data-ttu-id="5e660-142">Se definido, as cadeias de caracteres na lista de candidatos serão numeradas a partir de 1.</span><span class="sxs-lookup"><span data-stu-id="5e660-142">If set, strings in the candidate list are numbered starting at 1.</span></span> <span data-ttu-id="5e660-143">Se claro, as cadeias de caracteres começam em zero.</span><span class="sxs-lookup"><span data-stu-id="5e660-143">If clear, strings start at zero.</span></span>                                                                                                                                                                |
| <span data-ttu-id="5e660-144">\_Unicode prop do IME \_</span><span class="sxs-lookup"><span data-stu-id="5e660-144">IME\_PROP\_UNICODE</span></span>                  | <span data-ttu-id="5e660-145">Se definido, o IME será exibido como um UnicodeIME.</span><span class="sxs-lookup"><span data-stu-id="5e660-145">If set, the IME is viewed as a UnicodeIME.</span></span> <span data-ttu-id="5e660-146">O sistema e o IME se comunicarão por meio da interface UnicodeIME.</span><span class="sxs-lookup"><span data-stu-id="5e660-146">The system and the IME will communicate through the UnicodeIME interface.</span></span> <span data-ttu-id="5e660-147">Se claro, o IME usará a interface ANSI para se comunicar com o sistema.</span><span class="sxs-lookup"><span data-stu-id="5e660-147">If clear, IME will use the ANSI interface to communicate with the system.</span></span>                                                                    |
| <span data-ttu-id="5e660-148">\_prop IME \_ concluído \_ ao \_ desmarcar</span><span class="sxs-lookup"><span data-stu-id="5e660-148">IME\_PROP\_COMPLETE\_ON\_UNSELECT</span></span>   | <span data-ttu-id="5e660-149">Se definido, a janela de conversão estará na posição do cursor.</span><span class="sxs-lookup"><span data-stu-id="5e660-149">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="5e660-150">Se estiver claro, a janela estará perto da posição do cursor.</span><span class="sxs-lookup"><span data-stu-id="5e660-150">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="5e660-151">a \_ prop do IME \_ aceita \_ Wide \_ VKEY</span><span class="sxs-lookup"><span data-stu-id="5e660-151">IME\_PROP\_ACCEPT\_WIDE\_VKEY</span></span>       | <span data-ttu-id="5e660-152">Se definido, o IME processará o Unicode injetado que veio da função [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) usando o \_ pacote VK.</span><span class="sxs-lookup"><span data-stu-id="5e660-152">If set, the IME processes the injected Unicode that came from the [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) function by using VK\_PACKET.</span></span> <span data-ttu-id="5e660-153">Se estiver claro, o IME poderá não processar o Unicode injetado, e o Unicode injetado poderá ser enviado diretamente ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e660-153">If clear, the IME might not process the injected Unicode, and the injected Unicode might be sent to the application directly.</span></span> |



 

<span data-ttu-id="5e660-154">Se *wParam* for \_ a interface do usuário do IGP, ele retornará um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e660-154">If *wParam* is IGP\_UI, it returns one or more of the following values.</span></span>



| <span data-ttu-id="5e660-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e660-155">Requirement</span></span> | <span data-ttu-id="5e660-156">Valor</span><span class="sxs-lookup"><span data-stu-id="5e660-156">Value</span></span> |
|-----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e660-157">Limite de interface do usuário \_ \_ 2700</span><span class="sxs-lookup"><span data-stu-id="5e660-157">UI\_CAP\_2700</span></span>   | <span data-ttu-id="5e660-158">Dá suporte a valores de escape de texto 0 ou 2700.</span><span class="sxs-lookup"><span data-stu-id="5e660-158">Supports text escapement values of 0 or 2700.</span></span> <span data-ttu-id="5e660-159">Para obter mais informações, consulte **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="5e660-159">For more information, see **lfEscapement**.</span></span>             |
| <span data-ttu-id="5e660-160">\_ROT90 Cap da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="5e660-160">UI\_CAP\_ROT90</span></span>  | <span data-ttu-id="5e660-161">Dá suporte a valores de escape de texto de 0, 900, 1800 ou 2700.</span><span class="sxs-lookup"><span data-stu-id="5e660-161">Supports text escapement values of 0, 900, 1800, or 2700.</span></span> <span data-ttu-id="5e660-162">Para obter mais informações, consulte **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="5e660-162">For more information, see **lfEscapement**.</span></span> |
| <span data-ttu-id="5e660-163">\_ROTANY Cap da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="5e660-163">UI\_CAP\_ROTANY</span></span> | <span data-ttu-id="5e660-164">Dá suporte a qualquer valor de escape de texto.</span><span class="sxs-lookup"><span data-stu-id="5e660-164">Supports any text escapement value.</span></span> <span data-ttu-id="5e660-165">Para obter mais informações, consulte **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="5e660-165">For more information, see **lfEscapement**.</span></span>                       |



 

<span data-ttu-id="5e660-166">Se *wParam* for \_ o IGP SETCOMPSTR, ele retornará um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e660-166">If *wParam* is IGP\_SETCOMPSTR, it returns one or more of the following values.</span></span>



| <span data-ttu-id="5e660-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e660-167">Requirement</span></span> | <span data-ttu-id="5e660-168">Valor</span><span class="sxs-lookup"><span data-stu-id="5e660-168">Value</span></span> |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e660-169">\_COMPSTR Cap do SCS \_</span><span class="sxs-lookup"><span data-stu-id="5e660-169">SCS\_CAP\_COMPSTR</span></span>            | <span data-ttu-id="5e660-170">Pode criar a cadeia de caracteres de composição chamando a função [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) com o valor de SETSTR do SCS \_ .</span><span class="sxs-lookup"><span data-stu-id="5e660-170">Can create the composition string by calling the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with the SCS\_SETSTR value.</span></span>                                                      |
| <span data-ttu-id="5e660-171">\_MAKEREAD Cap do SCS \_</span><span class="sxs-lookup"><span data-stu-id="5e660-171">SCS\_CAP\_MAKEREAD</span></span>           | <span data-ttu-id="5e660-172">Pode criar a cadeia de caracteres de leitura da cadeia de caracteres de composição correspondente ao usar a função [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) com o SCS \_ SETSTR e sem definir *lpRead*.</span><span class="sxs-lookup"><span data-stu-id="5e660-172">Can create the reading string from corresponding composition string when using the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with SCS\_SETSTR and without setting *lpRead*.</span></span> |
| <span data-ttu-id="5e660-173">\_SETRECONVERTSTRING Cap do SCS \_</span><span class="sxs-lookup"><span data-stu-id="5e660-173">SCS\_CAP\_SETRECONVERTSTRING</span></span> | <span data-ttu-id="5e660-174">Este IME pode dar suporte à reconversão.</span><span class="sxs-lookup"><span data-stu-id="5e660-174">This IME can support reconversion.</span></span> <span data-ttu-id="5e660-175">Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) para fazer a reconversão.</span><span class="sxs-lookup"><span data-stu-id="5e660-175">Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) to do the reconversion.</span></span>                                                                             |



 

<span data-ttu-id="5e660-176">Se *wParam* for \_ o IGP Select, ele retornará um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e660-176">If *wParam* is IGP\_SELECT, it returns one or more of the following values.</span></span>



| <span data-ttu-id="5e660-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e660-177">Requirement</span></span> | <span data-ttu-id="5e660-178">Valor</span><span class="sxs-lookup"><span data-stu-id="5e660-178">Value</span></span> |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="5e660-179">Selecione \_ \_ arconvmode de Cap</span><span class="sxs-lookup"><span data-stu-id="5e660-179">SELECT\_CAP\_CONVMODE</span></span> | <span data-ttu-id="5e660-180">Herda o modo de conversão quando um novo IME é selecionado.</span><span class="sxs-lookup"><span data-stu-id="5e660-180">Inherits conversion mode when a new IME is selected.</span></span> |
| <span data-ttu-id="5e660-181">SELECIONAR \_ frase de extremidade \_</span><span class="sxs-lookup"><span data-stu-id="5e660-181">SELECT\_CAP\_SENTENCE</span></span> | <span data-ttu-id="5e660-182">Herda o modo de frase quando um novo IME é selecionado.</span><span class="sxs-lookup"><span data-stu-id="5e660-182">Inherits sentence mode when a new IME is selected.</span></span>   |



 

<span data-ttu-id="5e660-183">Se *wParam* for \_ o IGP GETIMEVERSION, ele retornará um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e660-183">If *wParam* is IGP\_GETIMEVERSION, it returns one or more of the following values.</span></span>



| <span data-ttu-id="5e660-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e660-184">Requirement</span></span> | <span data-ttu-id="5e660-185">Valor</span><span class="sxs-lookup"><span data-stu-id="5e660-185">Value</span></span> |
|--------------|---------------------------------------------|
| <span data-ttu-id="5e660-186">Nunca \_ 0310</span><span class="sxs-lookup"><span data-stu-id="5e660-186">IMEVER\_0310</span></span> | <span data-ttu-id="5e660-187">O IME foi criado para o Windows 3,1.</span><span class="sxs-lookup"><span data-stu-id="5e660-187">The IME was created for Windows 3.1.</span></span>        |
| <span data-ttu-id="5e660-188">Nunca \_ 0400</span><span class="sxs-lookup"><span data-stu-id="5e660-188">IMEVER\_0400</span></span> | <span data-ttu-id="5e660-189">O IME foi criado para o Windows 95 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5e660-189">The IME was created for Windows 95 or later</span></span> |



 

<span data-ttu-id="5e660-190">Essa mensagem é semelhante a [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), exceto pelo fato de que ela usa a localidade de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="5e660-190">This message is similar to [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), except that it uses the current input locale.</span></span> <span data-ttu-id="5e660-191">O aplicativo deve chamar [**em \_ ISIME**](em-isime.md) antes de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="5e660-191">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e660-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e660-192">Requirements</span></span>



| <span data-ttu-id="5e660-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e660-193">Requirement</span></span> | <span data-ttu-id="5e660-194">Valor</span><span class="sxs-lookup"><span data-stu-id="5e660-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e660-195">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e660-195">Minimum supported client</span></span><br/> | <span data-ttu-id="5e660-196">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e660-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e660-197">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e660-197">Minimum supported server</span></span><br/> | <span data-ttu-id="5e660-198">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5e660-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e660-199">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e660-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e660-200"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e660-200"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e660-201">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e660-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e660-202">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5e660-202">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5e660-203">**em \_ ISIME**</span><span class="sxs-lookup"><span data-stu-id="5e660-203">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

<span data-ttu-id="5e660-204">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="5e660-204">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5e660-205">**ImmGetProperty**</span><span class="sxs-lookup"><span data-stu-id="5e660-205">**ImmGetProperty**</span></span>](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

