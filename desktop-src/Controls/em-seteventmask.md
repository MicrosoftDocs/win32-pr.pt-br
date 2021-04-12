---
title: Mensagem de EM_SETEVENTMASK (RichEdit. h)
description: Define a máscara de evento para um controle de edição rico. A máscara de evento especifica quais códigos de notificação o controle envia para sua janela pai.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- Controles de EM_SETEVENTMASK de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455763"
---
# <a name="em_seteventmask-message"></a><span data-ttu-id="9a359-105">\_Mensagem em SETEVENTMASK</span><span class="sxs-lookup"><span data-stu-id="9a359-105">EM\_SETEVENTMASK message</span></span>

<span data-ttu-id="9a359-106">Define a máscara de evento para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="9a359-106">Sets the event mask for a rich edit control.</span></span> <span data-ttu-id="9a359-107">A máscara de evento especifica quais códigos de notificação o controle envia para sua janela pai.</span><span class="sxs-lookup"><span data-stu-id="9a359-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a359-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a359-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a359-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a359-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a359-110">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9a359-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9a359-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a359-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a359-112">Nova máscara de evento para o controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="9a359-112">New event mask for the rich edit control.</span></span> <span data-ttu-id="9a359-113">Para obter uma lista de máscaras de eventos, consulte [**sinalizadores de máscara de evento de controle de edição avançada**](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9a359-113">For a list of event masks, see [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a359-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a359-114">Return value</span></span>

<span data-ttu-id="9a359-115">Essa mensagem retorna a máscara de evento anterior.</span><span class="sxs-lookup"><span data-stu-id="9a359-115">This message returns the previous event mask.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a359-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a359-116">Remarks</span></span>

<span data-ttu-id="9a359-117">A máscara de evento padrão (antes de qualquer é definida) é ENM \_ None.</span><span class="sxs-lookup"><span data-stu-id="9a359-117">The default event mask (before any is set) is ENM\_NONE.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a359-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a359-118">Requirements</span></span>



| <span data-ttu-id="9a359-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a359-119">Requirement</span></span> | <span data-ttu-id="9a359-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9a359-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a359-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a359-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9a359-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a359-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a359-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a359-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9a359-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a359-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a359-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a359-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a359-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a359-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a359-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a359-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a359-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="9a359-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9a359-129">**em \_ GETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="9a359-129">**EM\_GETEVENTMASK**</span></span>](em-geteventmask.md)
</dt> <dt>

[<span data-ttu-id="9a359-130">**Sinalizadores de máscara de evento de controle de edição avançada**</span><span class="sxs-lookup"><span data-stu-id="9a359-130">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





