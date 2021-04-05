---
title: Mensagem de EM_GETLINE (WinUser. h)
description: Copia uma linha de texto de um controle de edição e a coloca em um buffer especificado. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Controles de EM_GETLINE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918066"
---
# <a name="em_getline-message-winuserh"></a><span data-ttu-id="2c11b-105">Mensagem de EM_GETLINE (WinUser. h)</span><span class="sxs-lookup"><span data-stu-id="2c11b-105">EM_GETLINE message (Winuser.h)</span></span>

<span data-ttu-id="2c11b-106">Copia uma linha de texto de um controle de edição e a coloca em um buffer especificado.</span><span class="sxs-lookup"><span data-stu-id="2c11b-106">Copies a line of text from an edit control and places it in a specified buffer.</span></span> <span data-ttu-id="2c11b-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="2c11b-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c11b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c11b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c11b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c11b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c11b-110">O índice de base zero da linha a ser recuperada de um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="2c11b-110">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="2c11b-111">Um valor de zero Especifica a linha superior.</span><span class="sxs-lookup"><span data-stu-id="2c11b-111">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="2c11b-112">Esse parâmetro é ignorado por um controle de edição de linha única.</span><span class="sxs-lookup"><span data-stu-id="2c11b-112">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="2c11b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c11b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c11b-114">Um ponteiro para o buffer que recebe uma cópia da linha.</span><span class="sxs-lookup"><span data-stu-id="2c11b-114">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="2c11b-115">Antes de enviar a mensagem, defina a primeira palavra desse buffer com o tamanho, em **TCHAR** s, do buffer.</span><span class="sxs-lookup"><span data-stu-id="2c11b-115">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="2c11b-116">Para texto ANSI, este é o número de bytes; para texto Unicode, este é o número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2c11b-116">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="2c11b-117">O tamanho na primeira palavra é substituído pela linha copiada.</span><span class="sxs-lookup"><span data-stu-id="2c11b-117">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c11b-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c11b-118">Return value</span></span>

<span data-ttu-id="2c11b-119">O valor de retorno é o número de **TCHAR** s copiados.</span><span class="sxs-lookup"><span data-stu-id="2c11b-119">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="2c11b-120">O valor de retorno será zero se o número de linha especificado pelo parâmetro *wParam* for maior que o número de linhas no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="2c11b-120">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c11b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c11b-121">Remarks</span></span>

<span data-ttu-id="2c11b-122">**Controles de edição:** A linha copiada não contém um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="2c11b-122">**Edit controls:** The copied line does not contain a terminating null character.</span></span>

<span data-ttu-id="2c11b-123">**Controles de edição avançados:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="2c11b-123">**Rich edit controls:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="2c11b-124">A linha copiada não contém um caractere nulo de terminação, a menos que nenhum texto tenha sido copiado.</span><span class="sxs-lookup"><span data-stu-id="2c11b-124">The copied line does not contain a terminating null character, unless no text was copied.</span></span> <span data-ttu-id="2c11b-125">Se nenhum texto for copiado, a mensagem colocará um caractere nulo no início do buffer.</span><span class="sxs-lookup"><span data-stu-id="2c11b-125">If no text was copied, the message places a null character at the beginning of the buffer.</span></span> <span data-ttu-id="2c11b-126">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="2c11b-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c11b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c11b-127">Requirements</span></span>



| <span data-ttu-id="2c11b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c11b-128">Requirement</span></span> | <span data-ttu-id="2c11b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2c11b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c11b-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c11b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2c11b-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c11b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c11b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c11b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2c11b-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c11b-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c11b-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c11b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c11b-135"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c11b-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c11b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c11b-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c11b-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2c11b-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2c11b-138">**em \_ LINELENGTH**</span><span class="sxs-lookup"><span data-stu-id="2c11b-138">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="2c11b-139">**Editar \_ getline**</span><span class="sxs-lookup"><span data-stu-id="2c11b-139">**Edit\_GetLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

<span data-ttu-id="2c11b-140">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="2c11b-140">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2c11b-141">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="2c11b-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

