---
title: Mensagem de EM_NOSETFOCUS (commctrl. h)
description: Impede que um controle de edição de linha única receba o foco do teclado. Você pode enviar essa mensagem explicitamente ou usando a macro editar \_ nosetfocus.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- Controles de EM_NOSETFOCUS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086030"
---
# <a name="em_nosetfocus-message"></a><span data-ttu-id="d2bf7-105">\_Mensagem em NOsetfocus</span><span class="sxs-lookup"><span data-stu-id="d2bf7-105">EM\_NOSETFOCUS message</span></span>

<span data-ttu-id="d2bf7-106">\[Destinado ao uso interno; Não recomendado para uso em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d2bf7-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="d2bf7-107">Essa mensagem pode não ter suporte em versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d2bf7-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="d2bf7-108">Impede que um controle de edição de linha única receba o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="d2bf7-108">Prevents a single-line edit control from receiving keyboard focus.</span></span> <span data-ttu-id="d2bf7-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**Editar \_ nosetfocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) .</span><span class="sxs-lookup"><span data-stu-id="d2bf7-109">You can send this message explicitly or by using the [**Edit\_NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2bf7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2bf7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2bf7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2bf7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2bf7-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d2bf7-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2bf7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2bf7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2bf7-114">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d2bf7-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2bf7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2bf7-115">Return value</span></span>

<span data-ttu-id="d2bf7-116">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="d2bf7-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="d2bf7-117">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="d2bf7-117">Security Considerations</span></span>

<span data-ttu-id="d2bf7-118">O uso dessa mensagem pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="d2bf7-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2bf7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2bf7-119">Remarks</span></span>

<span data-ttu-id="d2bf7-120">Essa mensagem será ignorada se o controle de edição não for um controle de edição de linha única.</span><span class="sxs-lookup"><span data-stu-id="d2bf7-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="d2bf7-121">Depois que essa mensagem é enviada, o efeito é permanente.</span><span class="sxs-lookup"><span data-stu-id="d2bf7-121">After this message is sent, the effect is permanent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2bf7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2bf7-122">Requirements</span></span>



| <span data-ttu-id="d2bf7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2bf7-123">Requirement</span></span> | <span data-ttu-id="d2bf7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d2bf7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2bf7-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2bf7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d2bf7-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2bf7-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2bf7-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2bf7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d2bf7-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d2bf7-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2bf7-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2bf7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2bf7-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2bf7-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2bf7-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2bf7-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2bf7-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d2bf7-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d2bf7-133">**Editar \_ Nosetfocus**</span><span class="sxs-lookup"><span data-stu-id="d2bf7-133">**Edit\_NoSetFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[<span data-ttu-id="d2bf7-134">**em \_ TAKEFOCUS**</span><span class="sxs-lookup"><span data-stu-id="d2bf7-134">**EM\_TAKEFOCUS**</span></span>](em-takefocus.md)
</dt> </dl>

 

 





