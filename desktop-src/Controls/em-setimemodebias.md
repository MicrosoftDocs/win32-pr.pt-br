---
title: Mensagem de EM_SETIMEMODEBIAS (RichEdit. h)
description: Defina a tendência do modo IME (editor de método de entrada) para um controle de edição rico.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- Controles de EM_SETIMEMODEBIAS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455347"
---
# <a name="em_setimemodebias-message"></a><span data-ttu-id="513f8-104">\_Mensagem em SETIMEMODEBIAS</span><span class="sxs-lookup"><span data-stu-id="513f8-104">EM\_SETIMEMODEBIAS message</span></span>

<span data-ttu-id="513f8-105">Defina a tendência do modo IME (editor de método de entrada) para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="513f8-105">Set the Input Method Editor (IME) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="513f8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="513f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="513f8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="513f8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="513f8-108">Valor de tendência do modo IME.</span><span class="sxs-lookup"><span data-stu-id="513f8-108">IME mode bias value.</span></span> <span data-ttu-id="513f8-109">Pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="513f8-109">It can be one of the following.</span></span>



| <span data-ttu-id="513f8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="513f8-110">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="513f8-111">Significado</span><span class="sxs-lookup"><span data-stu-id="513f8-111">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <span data-ttu-id="513f8-112"><dt>**\_PLAURALCLAUSE SMODE do IMF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="513f8-112"><dt>**IMF\_SMODE\_PLAURALCLAUSE**</dt></span></span> </dl> | <span data-ttu-id="513f8-113">Define o ajuste do modo IME para nome.</span><span class="sxs-lookup"><span data-stu-id="513f8-113">Sets the IME mode bias to Name.</span></span><br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <span data-ttu-id="513f8-114"><dt>**SMODE do IMF \_ \_ nenhum**</dt></span><span class="sxs-lookup"><span data-stu-id="513f8-114"><dt>**IMF\_SMODE\_NONE**</dt></span></span> </dl>                            | <span data-ttu-id="513f8-115">Sem tendência.</span><span class="sxs-lookup"><span data-stu-id="513f8-115">No bias.</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="513f8-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="513f8-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="513f8-117">Deve ser o mesmo valor que *wParam*.</span><span class="sxs-lookup"><span data-stu-id="513f8-117">This must be the same value as *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="513f8-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="513f8-118">Return value</span></span>

<span data-ttu-id="513f8-119">Essa mensagem retorna a nova configuração de ajuste do modo IME.</span><span class="sxs-lookup"><span data-stu-id="513f8-119">This message returns the new IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="513f8-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="513f8-120">Remarks</span></span>

<span data-ttu-id="513f8-121">Quando o IME gera uma lista de opções alternativas para um conjunto de caracteres, essa mensagem define os critérios pelos quais algumas das opções aparecerão na parte superior da lista.</span><span class="sxs-lookup"><span data-stu-id="513f8-121">When the IME generates a list of alternative choices for a set of characters, this message sets the criteria by which some of the choices will appear at the top of the list.</span></span>

<span data-ttu-id="513f8-122">Para definir a tendência do modo TSF (estrutura de serviços de texto), use em [**\_ SETCTFMODEBIAS**](em-setctfmodebias.md).</span><span class="sxs-lookup"><span data-stu-id="513f8-122">To set the Text Services Framework (TSF) mode bias, use [**EM\_SETCTFMODEBIAS**](em-setctfmodebias.md).</span></span>

<span data-ttu-id="513f8-123">O aplicativo deve chamar [**em \_ ISIME**](em-isime.md) antes de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="513f8-123">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="513f8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="513f8-124">Requirements</span></span>



| <span data-ttu-id="513f8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="513f8-125">Requirement</span></span> | <span data-ttu-id="513f8-126">Valor</span><span class="sxs-lookup"><span data-stu-id="513f8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="513f8-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="513f8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="513f8-128">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="513f8-128">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="513f8-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="513f8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="513f8-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="513f8-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="513f8-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="513f8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="513f8-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="513f8-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="513f8-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="513f8-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="513f8-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="513f8-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="513f8-135">**em \_ ISIME**</span><span class="sxs-lookup"><span data-stu-id="513f8-135">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="513f8-136">**em \_ SETCTFMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="513f8-136">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> </dl>

 

 





