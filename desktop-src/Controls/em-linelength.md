---
title: Mensagem de EM_LINELENGTH (WinUser. h)
description: Recupera o comprimento, em caracteres, de uma linha em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Controles de EM_LINELENGTH de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824644"
---
# <a name="em_linelength-message"></a><span data-ttu-id="3da8b-105">\_Mensagem em LINELENGTH</span><span class="sxs-lookup"><span data-stu-id="3da8b-105">EM\_LINELENGTH message</span></span>

<span data-ttu-id="3da8b-106">Recupera o comprimento, em caracteres, de uma linha em um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="3da8b-106">Retrieves the length, in characters, of a line in an edit control.</span></span> <span data-ttu-id="3da8b-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="3da8b-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3da8b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3da8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3da8b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3da8b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3da8b-110">O índice de caracteres de um caractere na linha cujo comprimento deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="3da8b-110">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="3da8b-111">Se esse parâmetro for maior que o número de caracteres no controle, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="3da8b-111">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="3da8b-112">Esse parâmetro pode ser-1.</span><span class="sxs-lookup"><span data-stu-id="3da8b-112">This parameter can be -1.</span></span> <span data-ttu-id="3da8b-113">Nesse caso, a mensagem retorna o número de caracteres não selecionados em linhas que contêm os caracteres selecionados.</span><span class="sxs-lookup"><span data-stu-id="3da8b-113">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="3da8b-114">Por exemplo, se a seleção estendida do quarto caractere de uma linha até o oitavo caractere do final da linha seguinte, o valor de retorno será 10 (três caracteres na primeira linha e sete no próximo).</span><span class="sxs-lookup"><span data-stu-id="3da8b-114">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="3da8b-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3da8b-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3da8b-116">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="3da8b-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3da8b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3da8b-117">Return value</span></span>

<span data-ttu-id="3da8b-118">Para controles de edição de várias linhas, o valor de retorno é o comprimento, em **TCHAR** s, da linha especificada pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="3da8b-118">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter.</span></span> <span data-ttu-id="3da8b-119">Para texto ANSI, este é o número de bytes; para texto Unicode, este é o número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3da8b-119">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="3da8b-120">Ele não inclui o caractere de retorno de carro no final da linha.</span><span class="sxs-lookup"><span data-stu-id="3da8b-120">It does not include the carriage-return character at the end of the line.</span></span>

<span data-ttu-id="3da8b-121">Para controles de edição de linha única, o valor de retorno é o comprimento, em **TCHAR** s, do texto no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="3da8b-121">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="3da8b-122">Se *wParam* for maior que o número de caracteres no controle, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="3da8b-122">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3da8b-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="3da8b-123">Remarks</span></span>

<span data-ttu-id="3da8b-124">Use a mensagem em [**\_ LINEINDEX**](em-lineindex.md) para recuperar um índice de caracteres para um determinado número de linha dentro de um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="3da8b-124">Use the [**EM\_LINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control.</span></span>

<span data-ttu-id="3da8b-125">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3da8b-125">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="3da8b-126">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="3da8b-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3da8b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3da8b-127">Requirements</span></span>



| <span data-ttu-id="3da8b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3da8b-128">Requirement</span></span> | <span data-ttu-id="3da8b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3da8b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3da8b-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3da8b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3da8b-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3da8b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3da8b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3da8b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3da8b-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3da8b-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3da8b-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3da8b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3da8b-135"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3da8b-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3da8b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="3da8b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da8b-137">**em \_ LINEINDEX**</span><span class="sxs-lookup"><span data-stu-id="3da8b-137">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





