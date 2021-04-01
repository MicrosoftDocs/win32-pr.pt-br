---
title: Mensagem de EM_GETEVENTMASK (RichEdit. h)
description: Recupera a máscara de evento para um controle de edição rico. A máscara de evento especifica quais códigos de notificação o controle envia para sua janela pai.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- Controles de EM_GETEVENTMASK de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918810"
---
# <a name="em_geteventmask-message"></a><span data-ttu-id="62e72-105">\_Mensagem em GETEVENTMASK</span><span class="sxs-lookup"><span data-stu-id="62e72-105">EM\_GETEVENTMASK message</span></span>

<span data-ttu-id="62e72-106">Recupera a máscara de evento para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="62e72-106">Retrieves the event mask for a rich edit control.</span></span> <span data-ttu-id="62e72-107">A máscara de evento especifica quais códigos de notificação o controle envia para sua janela pai.</span><span class="sxs-lookup"><span data-stu-id="62e72-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="62e72-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62e72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62e72-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62e72-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62e72-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="62e72-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="62e72-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62e72-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62e72-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="62e72-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62e72-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62e72-113">Return value</span></span>

<span data-ttu-id="62e72-114">Essa mensagem retorna a máscara de evento para o controle rich edit.</span><span class="sxs-lookup"><span data-stu-id="62e72-114">This message returns the event mask for the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="62e72-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62e72-115">Requirements</span></span>



| <span data-ttu-id="62e72-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="62e72-116">Requirement</span></span> | <span data-ttu-id="62e72-117">Valor</span><span class="sxs-lookup"><span data-stu-id="62e72-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62e72-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62e72-118">Minimum supported client</span></span><br/> | <span data-ttu-id="62e72-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62e72-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62e72-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62e72-120">Minimum supported server</span></span><br/> | <span data-ttu-id="62e72-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62e72-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62e72-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62e72-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="62e72-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="62e72-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62e72-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="62e72-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="62e72-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="62e72-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="62e72-126">**em \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="62e72-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="62e72-127">**Sinalizadores de máscara de evento de controle de edição avançada**</span><span class="sxs-lookup"><span data-stu-id="62e72-127">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





