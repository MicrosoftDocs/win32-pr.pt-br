---
title: Mensagem de EM_GETLINECOUNT (WinUser. h)
description: Obtém o número de linhas em um controle de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Controles de EM_GETLINECOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15ffbeafb13850317faccb4be44571d81b0d7e36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454764"
---
# <a name="em_getlinecount-message-winuserh"></a><span data-ttu-id="f2ea3-105">Mensagem de EM_GETLINECOUNT (WinUser. h)</span><span class="sxs-lookup"><span data-stu-id="f2ea3-105">EM_GETLINECOUNT message (Winuser.h)</span></span>

<span data-ttu-id="f2ea3-106">Obtém o número de linhas em um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="f2ea3-106">Gets the number of lines in a multiline edit control.</span></span> <span data-ttu-id="f2ea3-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="f2ea3-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2ea3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2ea3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2ea3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2ea3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2ea3-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f2ea3-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f2ea3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2ea3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2ea3-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f2ea3-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2ea3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2ea3-113">Return value</span></span>

<span data-ttu-id="f2ea3-114">O valor de retorno é um número inteiro que especifica o número total de linhas de texto no controle de edição de várias linhas ou no controle de edição com formato.</span><span class="sxs-lookup"><span data-stu-id="f2ea3-114">The return value is an integer specifying the total number of text lines in the multiline edit control or rich edit control.</span></span> <span data-ttu-id="f2ea3-115">Se o controle não tiver texto, o valor de retorno será 1.</span><span class="sxs-lookup"><span data-stu-id="f2ea3-115">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="f2ea3-116">O valor de retorno nunca será menor que 1.</span><span class="sxs-lookup"><span data-stu-id="f2ea3-116">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ea3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2ea3-117">Remarks</span></span>

<span data-ttu-id="f2ea3-118">A mensagem em **\_ GETLINECOUNT** recupera o número total de linhas de texto, não apenas o número de linhas que estão visíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="f2ea3-118">The **EM\_GETLINECOUNT** message retrieves the total number of text lines, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="f2ea3-119">Se o recurso WordWrap estiver habilitado, o número de linhas poderá ser alterado quando as dimensões da janela de edição forem alteradas.</span><span class="sxs-lookup"><span data-stu-id="f2ea3-119">If the Wordwrap feature is enabled, the number of lines can change when the dimensions of the editing window change.</span></span>

<span data-ttu-id="f2ea3-120">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="f2ea3-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="f2ea3-121">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f2ea3-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ea3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2ea3-122">Requirements</span></span>



| <span data-ttu-id="f2ea3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2ea3-123">Requirement</span></span> | <span data-ttu-id="f2ea3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f2ea3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ea3-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2ea3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ea3-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2ea3-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f2ea3-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2ea3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ea3-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2ea3-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f2ea3-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2ea3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2ea3-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2ea3-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ea3-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2ea3-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2ea3-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="f2ea3-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f2ea3-133">**em \_ GETline**</span><span class="sxs-lookup"><span data-stu-id="f2ea3-133">**EM\_GETLINE**</span></span>](em-getline.md)
</dt> <dt>

[<span data-ttu-id="f2ea3-134">**em \_ LINELENGTH**</span><span class="sxs-lookup"><span data-stu-id="f2ea3-134">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="f2ea3-135">**Editar \_ GetLineCount**</span><span class="sxs-lookup"><span data-stu-id="f2ea3-135">**Edit\_GetLineCount**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





