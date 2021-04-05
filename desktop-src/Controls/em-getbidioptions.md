---
title: Mensagem de EM_GETBIDIOPTIONS (RichEdit. h)
description: Indica o estado atual das opções bidirecionais no controle de edição rico.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- Controles de EM_GETBIDIOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085678"
---
# <a name="em_getbidioptions-message"></a><span data-ttu-id="06e1c-104">\_Mensagem em GETbidioptions</span><span class="sxs-lookup"><span data-stu-id="06e1c-104">EM\_GETBIDIOPTIONS message</span></span>

<span data-ttu-id="06e1c-105">Indica o estado atual das opções bidirecionais no controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="06e1c-105">Indicates the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="06e1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06e1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e1c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06e1c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06e1c-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="06e1c-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="06e1c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06e1c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06e1c-110">Uma estrutura [**bidioptions**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) que recebe o estado atual das opções bidirecionais no controle rich edit.</span><span class="sxs-lookup"><span data-stu-id="06e1c-110">A [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that receives the current state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e1c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06e1c-111">Return value</span></span>

<span data-ttu-id="06e1c-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="06e1c-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06e1c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="06e1c-113">Remarks</span></span>

<span data-ttu-id="06e1c-114">Essa mensagem define os valores dos membros **wMask** e **wEffects** como o valor do estado atual das opções bidirecionais no controle rich edit.</span><span class="sxs-lookup"><span data-stu-id="06e1c-114">This message sets the values of the **wMask** and **wEffects** members to the value of the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="06e1c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06e1c-115">Requirements</span></span>



| <span data-ttu-id="06e1c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="06e1c-116">Requirement</span></span> | <span data-ttu-id="06e1c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="06e1c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06e1c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06e1c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06e1c-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06e1c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06e1c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06e1c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06e1c-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06e1c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06e1c-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="06e1c-122">Redistributable</span></span><br/>          | <span data-ttu-id="06e1c-123">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="06e1c-123">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="06e1c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06e1c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="06e1c-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="06e1c-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06e1c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="06e1c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="06e1c-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="06e1c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="06e1c-128">**BIDIoptions**</span><span class="sxs-lookup"><span data-stu-id="06e1c-128">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="06e1c-129">**em \_ SETbidioptions**</span><span class="sxs-lookup"><span data-stu-id="06e1c-129">**EM\_SETBIDIOPTIONS**</span></span>](em-setbidioptions.md)
</dt> </dl>

 

 





