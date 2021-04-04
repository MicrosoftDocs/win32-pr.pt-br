---
title: Mensagem de EM_GETMODIFY (WinUser. h)
description: Obtém o estado de um sinalizador de modificação do controle de edição. O sinalizador indica se o conteúdo do controle de edição foi modificado. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- Controles de EM_GETMODIFY de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824224"
---
# <a name="em_getmodify-message"></a><span data-ttu-id="53310-106">Em \_ getmodificar mensagem</span><span class="sxs-lookup"><span data-stu-id="53310-106">EM\_GETMODIFY message</span></span>

<span data-ttu-id="53310-107">Obtém o estado de um sinalizador de modificação do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="53310-107">Gets the state of an edit control's modification flag.</span></span> <span data-ttu-id="53310-108">O sinalizador indica se o conteúdo do controle de edição foi modificado.</span><span class="sxs-lookup"><span data-stu-id="53310-108">The flag indicates whether the contents of the edit control have been modified.</span></span> <span data-ttu-id="53310-109">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="53310-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="53310-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53310-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53310-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53310-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53310-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="53310-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="53310-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53310-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53310-114">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="53310-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53310-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53310-115">Return value</span></span>

<span data-ttu-id="53310-116">Se o conteúdo do controle de edição tiver sido modificado, o valor de retorno será diferente de zero; caso contrário, será zero.</span><span class="sxs-lookup"><span data-stu-id="53310-116">If the contents of edit control have been modified, the return value is nonzero; otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="53310-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="53310-117">Remarks</span></span>

<span data-ttu-id="53310-118">O sistema limpa automaticamente o sinalizador de modificação para zero quando o controle é criado.</span><span class="sxs-lookup"><span data-stu-id="53310-118">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="53310-119">Se o usuário alterar o texto do controle, o sistema definirá o sinalizador como diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="53310-119">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="53310-120">Você pode enviar a [**mensagem \_ eme**](em-setmodify.md) para o controle de edição para definir ou limpar o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="53310-120">You can send the [**EM\_SETMODIFY**](em-setmodify.md) message to the edit control to set or clear the flag.</span></span>

<span data-ttu-id="53310-121">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="53310-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="53310-122">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="53310-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53310-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53310-123">Requirements</span></span>



| <span data-ttu-id="53310-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="53310-124">Requirement</span></span> | <span data-ttu-id="53310-125">Valor</span><span class="sxs-lookup"><span data-stu-id="53310-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53310-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53310-126">Minimum supported client</span></span><br/> | <span data-ttu-id="53310-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53310-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53310-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53310-128">Minimum supported server</span></span><br/> | <span data-ttu-id="53310-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53310-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53310-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53310-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="53310-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53310-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53310-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="53310-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53310-133">**em \_ SETmodify**</span><span class="sxs-lookup"><span data-stu-id="53310-133">**EM\_SETMODIFY**</span></span>](em-setmodify.md)
</dt> </dl>

 

 





