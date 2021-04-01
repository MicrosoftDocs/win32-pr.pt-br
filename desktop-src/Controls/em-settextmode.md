---
title: Mensagem de EM_SETTEXTMODE (RichEdit. h)
description: Define o modo de texto ou o nível de desfazer de um controle de edição rico. A mensagem falhará se o controle contiver qualquer texto.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- Controles de EM_SETTEXTMODE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918616"
---
# <a name="em_settextmode-message"></a><span data-ttu-id="c72ad-105">\_Mensagem em SETtextmode</span><span class="sxs-lookup"><span data-stu-id="c72ad-105">EM\_SETTEXTMODE message</span></span>

<span data-ttu-id="c72ad-106">Define o modo de texto ou o nível de desfazer de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="c72ad-106">Sets the text mode or undo level of a rich edit control.</span></span> <span data-ttu-id="c72ad-107">A mensagem falhará se o controle contiver qualquer texto.</span><span class="sxs-lookup"><span data-stu-id="c72ad-107">The message fails if the control contains any text.</span></span>

## <a name="parameters"></a><span data-ttu-id="c72ad-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c72ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c72ad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c72ad-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c72ad-110">Um ou mais valores do tipo de enumeração [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) .</span><span class="sxs-lookup"><span data-stu-id="c72ad-110">One or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="c72ad-111">Os valores especificam as novas configurações para o modo de texto do controle e os parâmetros de nível de desfazer.</span><span class="sxs-lookup"><span data-stu-id="c72ad-111">The values specify the new settings for the control's text mode and undo level parameters.</span></span>

<span data-ttu-id="c72ad-112">Especifique um dos valores a seguir para definir o parâmetro de modo de texto.</span><span class="sxs-lookup"><span data-stu-id="c72ad-112">Specify one of the following values to set the text mode parameter.</span></span> <span data-ttu-id="c72ad-113">Se você não especificar um valor de modo de texto, o modo de texto permanecerá em sua configuração atual.</span><span class="sxs-lookup"><span data-stu-id="c72ad-113">If you do not specify a text mode value, the text mode remains at its current setting.</span></span> 

| <span data-ttu-id="c72ad-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c72ad-114">Value</span></span>                                          | <span data-ttu-id="c72ad-115">Significado</span><span class="sxs-lookup"><span data-stu-id="c72ad-115">Meaning</span></span>                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c72ad-116">**TM \_ sem formatação**</span><span class="sxs-lookup"><span data-stu-id="c72ad-116">**TM\_PLAINTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="c72ad-117">Indica o modo de texto sem formatação, no qual o controle é semelhante a um controle de edição padrão.</span><span class="sxs-lookup"><span data-stu-id="c72ad-117">Indicates plain text mode, in which the control is similar to a standard edit control.</span></span> <span data-ttu-id="c72ad-118">Para obter mais informações sobre o modo de texto sem formatação, consulte a seção de comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="c72ad-118">For more information about plain text mode, see the following Remarks section.</span></span> |
| [<span data-ttu-id="c72ad-119">**RICHTEXT de TM \_**</span><span class="sxs-lookup"><span data-stu-id="c72ad-119">**TM\_RICHTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="c72ad-120">Indica o modo de Rich Text, no qual o controle tem a funcionalidade de edição avançada padrão.</span><span class="sxs-lookup"><span data-stu-id="c72ad-120">Indicates rich text mode, in which the control has standard rich edit functionality.</span></span> <span data-ttu-id="c72ad-121">O modo de Rich Text é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="c72ad-121">Rich text mode is the default setting.</span></span>                                           |



 

<span data-ttu-id="c72ad-122">Especifique um dos valores a seguir para definir o parâmetro de nível de desfazer.</span><span class="sxs-lookup"><span data-stu-id="c72ad-122">Specify one of the following values to set the undo level parameter.</span></span> <span data-ttu-id="c72ad-123">Se você não especificar um valor de nível de desfazer, o nível de desfazer permanecerá em sua configuração atual.</span><span class="sxs-lookup"><span data-stu-id="c72ad-123">If you do not specify an undo level value, the undo level remains at its current setting.</span></span> 

| <span data-ttu-id="c72ad-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c72ad-124">Value</span></span>                                                      | <span data-ttu-id="c72ad-125">Significado</span><span class="sxs-lookup"><span data-stu-id="c72ad-125">Meaning</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c72ad-126">**TM \_ SINGLELEVELUNDO**</span><span class="sxs-lookup"><span data-stu-id="c72ad-126">**TM\_SINGLELEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="c72ad-127">O controle permite que o usuário desfaça apenas a última ação que pode ser desfeita.</span><span class="sxs-lookup"><span data-stu-id="c72ad-127">The control allows the user to undo only the last action that can be undone.</span></span>                                                                                                       |
| [<span data-ttu-id="c72ad-128">**TM \_ MULTILEVELUNDO**</span><span class="sxs-lookup"><span data-stu-id="c72ad-128">**TM\_MULTILEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="c72ad-129">O controle dá suporte a várias operações de desfazer.</span><span class="sxs-lookup"><span data-stu-id="c72ad-129">The control supports multiple undo operations.</span></span> <span data-ttu-id="c72ad-130">Essa é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="c72ad-130">This is the default setting.</span></span> <span data-ttu-id="c72ad-131">Use a mensagem em [**\_ SETUNDOLIMIT**](em-setundolimit.md) para definir o número máximo de ações de desfazer.</span><span class="sxs-lookup"><span data-stu-id="c72ad-131">Use the [**EM\_SETUNDOLIMIT**](em-setundolimit.md) message to set the maximum number of undo actions.</span></span> |



 

<span data-ttu-id="c72ad-132">Especifique um dos valores a seguir para definir o parâmetro de página de código.</span><span class="sxs-lookup"><span data-stu-id="c72ad-132">Specify one of the following values to set the code page parameter.</span></span> <span data-ttu-id="c72ad-133">Se você não especificar um valor de página de código, a página de código permanecerá em sua configuração atual.</span><span class="sxs-lookup"><span data-stu-id="c72ad-133">If you do not specify an code page value, the code page remains at its current setting.</span></span> 

| <span data-ttu-id="c72ad-134">Valor</span><span class="sxs-lookup"><span data-stu-id="c72ad-134">Value</span></span>                                                    | <span data-ttu-id="c72ad-135">Significado</span><span class="sxs-lookup"><span data-stu-id="c72ad-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c72ad-136">**TM \_ SINGLECODEPAGE**</span><span class="sxs-lookup"><span data-stu-id="c72ad-136">**TM\_SINGLECODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="c72ad-137">O controle só permite o teclado em inglês e um teclado correspondente ao conjunto de caracteres padrão.</span><span class="sxs-lookup"><span data-stu-id="c72ad-137">The control only allows the English keyboard and a keyboard corresponding to the default character set.</span></span> <span data-ttu-id="c72ad-138">Por exemplo, você pode ter grego e inglês.</span><span class="sxs-lookup"><span data-stu-id="c72ad-138">For example, you could have Greek and English.</span></span> <span data-ttu-id="c72ad-139">Observe que isso impede que o texto Unicode entre no controle.</span><span class="sxs-lookup"><span data-stu-id="c72ad-139">Note that this prevents Unicode text from entering the control.</span></span> <span data-ttu-id="c72ad-140">Por exemplo, use esse valor se um controle de edição rico precisar ser restrito ao texto ANSI.</span><span class="sxs-lookup"><span data-stu-id="c72ad-140">For example, use this value if a Rich Edit control must be restricted to ANSI text.</span></span> |
| [<span data-ttu-id="c72ad-141">**TM \_ MULTIcodepage**</span><span class="sxs-lookup"><span data-stu-id="c72ad-141">**TM\_MULTICODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="c72ad-142">O controle permite várias páginas de código e texto Unicode no controle.</span><span class="sxs-lookup"><span data-stu-id="c72ad-142">The control allows multiple code pages and Unicode text into the control.</span></span> <span data-ttu-id="c72ad-143">Essa é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="c72ad-143">This is the default setting.</span></span>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="c72ad-144">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c72ad-144">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c72ad-145">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c72ad-145">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c72ad-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c72ad-146">Return value</span></span>

<span data-ttu-id="c72ad-147">Se a mensagem tiver sucesso, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="c72ad-147">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="c72ad-148">Se a mensagem falhar, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c72ad-148">If the message fails, the return value is a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c72ad-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="c72ad-149">Remarks</span></span>

<span data-ttu-id="c72ad-150">No modo Rich Text, um controle rich edit tem funcionalidade de edição avançada padrão.</span><span class="sxs-lookup"><span data-stu-id="c72ad-150">In rich text mode, a rich edit control has standard rich edit functionality.</span></span> <span data-ttu-id="c72ad-151">No entanto, no modo de texto sem formatação, o controle é semelhante a um controle de edição padrão:</span><span class="sxs-lookup"><span data-stu-id="c72ad-151">However, in plain text mode, the control is similar to a standard edit control:</span></span>

-   <span data-ttu-id="c72ad-152">O texto em um controle de texto sem formatação pode ter apenas um formato (como negrito, 10pt Arial).</span><span class="sxs-lookup"><span data-stu-id="c72ad-152">The text in a plain text control can have only one format (such as Bold, 10pt Arial).</span></span>
-   <span data-ttu-id="c72ad-153">O usuário não pode colar formatos de Rich Text, como Rich Text Format (RTF) ou objetos incorporados em um controle de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="c72ad-153">The user cannot paste rich text formats, such as Rich Text Format (RTF) or embedded objects into a plain text control.</span></span>
-   <span data-ttu-id="c72ad-154">Controles de modo de Rich Text sempre têm um marcador de fim de documento padrão ou retorno de carro, para formatar parágrafos.</span><span class="sxs-lookup"><span data-stu-id="c72ad-154">Rich text mode controls always have a default end-of-document marker or carriage return, to format paragraphs.</span></span> <span data-ttu-id="c72ad-155">Os controles de texto sem formatação, por outro lado, não precisam do marcador padrão de fim de documento, portanto, ele é omitido.</span><span class="sxs-lookup"><span data-stu-id="c72ad-155">Plain text controls, on the other hand, do not need the default, end-of-document marker, so it is omitted.</span></span>

<span data-ttu-id="c72ad-156">O controle não deve conter nenhum texto quando receber a mensagem em **\_ settextmode** .</span><span class="sxs-lookup"><span data-stu-id="c72ad-156">The control must contain no text when it receives the **EM\_SETTEXTMODE** message.</span></span> <span data-ttu-id="c72ad-157">Para garantir que não haja texto, envie uma mensagem de [**\_ SetText do WM**](/windows/desktop/winmsg/wm-settext) com uma cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="c72ad-157">To ensure there is no text, send a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message with an empty string ("").</span></span>

## <a name="requirements"></a><span data-ttu-id="c72ad-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c72ad-158">Requirements</span></span>



| <span data-ttu-id="c72ad-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="c72ad-159">Requirement</span></span> | <span data-ttu-id="c72ad-160">Valor</span><span class="sxs-lookup"><span data-stu-id="c72ad-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c72ad-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c72ad-161">Minimum supported client</span></span><br/> | <span data-ttu-id="c72ad-162">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c72ad-162">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c72ad-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c72ad-163">Minimum supported server</span></span><br/> | <span data-ttu-id="c72ad-164">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c72ad-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c72ad-165">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c72ad-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="c72ad-166"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c72ad-166"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c72ad-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="c72ad-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c72ad-168">**em \_ GETtextmode**</span><span class="sxs-lookup"><span data-stu-id="c72ad-168">**EM\_GETTEXTMODE**</span></span>](em-gettextmode.md)
</dt> <dt>

[<span data-ttu-id="c72ad-169">**em \_ SETUNDOLIMIT**</span><span class="sxs-lookup"><span data-stu-id="c72ad-169">**EM\_SETUNDOLIMIT**</span></span>](em-setundolimit.md)
</dt> <dt>

[<span data-ttu-id="c72ad-170">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="c72ad-170">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[<span data-ttu-id="c72ad-171">**SetText do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c72ad-171">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

