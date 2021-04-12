---
title: Mensagem de EM_TAKEFOCUS (commctrl. h)
description: Força um controle de edição de linha única a receber o foco do teclado. Você pode enviar essa mensagem explicitamente ou usando a macro Edit \_ TakeFocus.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- Controles de EM_TAKEFOCUS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4abdf926cdd337760b5cf151c3f8ee08cb418b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455183"
---
# <a name="em_takefocus-message"></a><span data-ttu-id="68c90-105">\_Mensagem em TAKEFOCUS</span><span class="sxs-lookup"><span data-stu-id="68c90-105">EM\_TAKEFOCUS message</span></span>

<span data-ttu-id="68c90-106">\[Destinado ao uso interno; Não recomendado para uso em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="68c90-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="68c90-107">Essa mensagem pode não ter suporte em versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="68c90-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="68c90-108">Força um controle de edição de linha única a receber o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="68c90-108">Forces a single-line edit control to receive keyboard focus.</span></span> <span data-ttu-id="68c90-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**Edit \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) .</span><span class="sxs-lookup"><span data-stu-id="68c90-109">You can send this message explicitly or by using the [**Edit\_TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="68c90-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68c90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68c90-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68c90-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68c90-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="68c90-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="68c90-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68c90-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68c90-114">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="68c90-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68c90-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68c90-115">Return value</span></span>

<span data-ttu-id="68c90-116">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="68c90-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="68c90-117">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="68c90-117">Security Considerations</span></span>

<span data-ttu-id="68c90-118">O uso dessa mensagem pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="68c90-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="68c90-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="68c90-119">Remarks</span></span>

<span data-ttu-id="68c90-120">Essa mensagem será ignorada se o controle de edição não for um controle de edição de linha única.</span><span class="sxs-lookup"><span data-stu-id="68c90-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="68c90-121">Se o controle de edição tiver recebido anteriormente uma mensagem em [**\_ nosetfocus**](em-nosetfocus.md) , o controle de edição parecerá ter o foco sem realmente tê-lo; caso contrário, o controle de edição receberá o foco.</span><span class="sxs-lookup"><span data-stu-id="68c90-121">If the edit control previously received an [**EM\_NOSETFOCUS**](em-nosetfocus.md) message, the edit control will appear to have the focus without actually having it; otherwise, the edit control will receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="68c90-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68c90-122">Requirements</span></span>



| <span data-ttu-id="68c90-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="68c90-123">Requirement</span></span> | <span data-ttu-id="68c90-124">Valor</span><span class="sxs-lookup"><span data-stu-id="68c90-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68c90-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68c90-125">Minimum supported client</span></span><br/> | <span data-ttu-id="68c90-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68c90-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68c90-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68c90-127">Minimum supported server</span></span><br/> | <span data-ttu-id="68c90-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68c90-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68c90-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68c90-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="68c90-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68c90-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68c90-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="68c90-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="68c90-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="68c90-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="68c90-133">**Editar \_ TakeFocus**</span><span class="sxs-lookup"><span data-stu-id="68c90-133">**Edit\_TakeFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[<span data-ttu-id="68c90-134">**em \_ NOsetfocus**</span><span class="sxs-lookup"><span data-stu-id="68c90-134">**EM\_NOSETFOCUS**</span></span>](em-nosetfocus.md)
</dt> </dl>

 

 





