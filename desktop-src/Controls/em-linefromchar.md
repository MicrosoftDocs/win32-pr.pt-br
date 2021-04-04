---
title: Mensagem de EM_LINEFROMCHAR (WinUser. h)
description: Obtém o índice da linha que contém o índice de caracteres especificado em um controle de edição de várias linhas.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Controles de EM_LINEFROMCHAR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085410"
---
# <a name="em_linefromchar-message"></a><span data-ttu-id="6694e-104">\_Mensagem em LINEFROMCHAR</span><span class="sxs-lookup"><span data-stu-id="6694e-104">EM\_LINEFROMCHAR message</span></span>

<span data-ttu-id="6694e-105">Obtém o índice da linha que contém o índice de caracteres especificado em um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="6694e-105">Gets the index of the line that contains the specified character index in a multiline edit control.</span></span> <span data-ttu-id="6694e-106">Um índice de caracteres é o índice de base zero do caractere do início do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="6694e-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="6694e-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="6694e-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6694e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6694e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6694e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6694e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6694e-110">O índice de caracteres do caractere contido na linha cujo número deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="6694e-110">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="6694e-111">Se esse parâmetro for-1, **em \_ LINEFROMCHAR** recuperará o número de linha da linha atual (a linha que contém o cursor) ou, se houver uma seleção, o número de linha da linha que contém o início da seleção.</span><span class="sxs-lookup"><span data-stu-id="6694e-111">If this parameter is -1, **EM\_LINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="6694e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6694e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6694e-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6694e-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6694e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6694e-114">Return value</span></span>

<span data-ttu-id="6694e-115">O valor de retorno é o número de linha com base em zero da linha que contém o índice de caracteres especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="6694e-115">The return value is the zero-based line number of the line containing the character index specified by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="6694e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6694e-116">Remarks</span></span>

<span data-ttu-id="6694e-117">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="6694e-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="6694e-118">Se o índice de caracteres for maior que 64.000, use a mensagem em [**\_ EXLINEFROMCHAR**](em-exlinefromchar.md) .</span><span class="sxs-lookup"><span data-stu-id="6694e-118">If the character index is greater than 64,000, use the [**EM\_EXLINEFROMCHAR**](em-exlinefromchar.md) message.</span></span> <span data-ttu-id="6694e-119">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="6694e-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6694e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6694e-120">Requirements</span></span>



| <span data-ttu-id="6694e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6694e-121">Requirement</span></span> | <span data-ttu-id="6694e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6694e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6694e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6694e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6694e-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6694e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6694e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6694e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6694e-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6694e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6694e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6694e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6694e-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6694e-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6694e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6694e-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="6694e-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6694e-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6694e-131">**em \_ EXLINEFROMCHAR**</span><span class="sxs-lookup"><span data-stu-id="6694e-131">**EM\_EXLINEFROMCHAR**</span></span>](em-exlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="6694e-132">**em \_ LINEINDEX**</span><span class="sxs-lookup"><span data-stu-id="6694e-132">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





