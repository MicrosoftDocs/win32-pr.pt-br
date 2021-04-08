---
title: Mensagem de EM_SETBIDIOPTIONS (RichEdit. h)
description: A \_ mensagem em SETbidioptions define o estado atual das opções bidirecionais no controle de edição rico.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- Controles de EM_SETBIDIOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086193"
---
# <a name="em_setbidioptions-message"></a><span data-ttu-id="4b14a-104">\_Mensagem em SETbidioptions</span><span class="sxs-lookup"><span data-stu-id="4b14a-104">EM\_SETBIDIOPTIONS message</span></span>

<span data-ttu-id="4b14a-105">A mensagem em **\_ setbidioptions** define o estado atual das opções bidirecionais no controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="4b14a-105">The **EM\_SETBIDIOPTIONS** message sets the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b14a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b14a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b14a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b14a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b14a-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4b14a-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4b14a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b14a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b14a-110">Ponteiro para uma estrutura [**bidioptions**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) que indica como definir o estado das opções bidirecionais no controle rich edit.</span><span class="sxs-lookup"><span data-stu-id="4b14a-110">Pointer to a [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that indicates how to set the state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b14a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b14a-111">Return value</span></span>

<span data-ttu-id="4b14a-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4b14a-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b14a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b14a-113">Remarks</span></span>

<span data-ttu-id="4b14a-114">O controle rich edit deve estar no modo de texto sem formatação ou em **\_ setbidioptions** não fará nada.</span><span class="sxs-lookup"><span data-stu-id="4b14a-114">The rich edit control must be in plain text mode or **EM\_SETBIDIOPTIONS** will not do anything.</span></span>

<span data-ttu-id="4b14a-115">Em controles de texto sem formatação, em **\_ setbidioptions** determina automaticamente a direção do parágrafo e/ou o alinhamento com base nas regras de contexto.</span><span class="sxs-lookup"><span data-stu-id="4b14a-115">In plain text controls, **EM\_SETBIDIOPTIONS** automatically determines the paragraph direction and/or alignment based on the context rules.</span></span> <span data-ttu-id="4b14a-116">Essas regras deformam que a direção e/ou o alinhamento são derivados do primeiro caractere forte no controle.</span><span class="sxs-lookup"><span data-stu-id="4b14a-116">These rules state that the direction and/or alignment is derived from the first strong character in the control.</span></span> <span data-ttu-id="4b14a-117">Um caractere forte é aquele do qual a direção do texto pode ser determinada (consulte Unicode Standard versão 2,0).</span><span class="sxs-lookup"><span data-stu-id="4b14a-117">A strong character is one from which text direction can be determined (see Unicode Standard version 2.0).</span></span> <span data-ttu-id="4b14a-118">A direção do parágrafo e/ou o alinhamento é aplicado ao formato padrão.</span><span class="sxs-lookup"><span data-stu-id="4b14a-118">The paragraph direction and/or alignment is applied to the default format.</span></span>

<span data-ttu-id="4b14a-119">**Em \_ Setbidioptions** alterna apenas o formato de parágrafo padrão para RTL (da direita para a esquerda) se encontrar um caractere DPE,</span><span class="sxs-lookup"><span data-stu-id="4b14a-119">**EM\_SETBIDIOPTIONS** only switches the default paragraph format to RTL (right to left) if it finds an RTL character,</span></span>

## <a name="requirements"></a><span data-ttu-id="4b14a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b14a-120">Requirements</span></span>



| <span data-ttu-id="4b14a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b14a-121">Requirement</span></span> | <span data-ttu-id="4b14a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4b14a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b14a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b14a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4b14a-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b14a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b14a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b14a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4b14a-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b14a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b14a-127">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4b14a-127">Redistributable</span></span><br/>          | <span data-ttu-id="4b14a-128">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="4b14a-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="4b14a-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b14a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b14a-130"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b14a-130"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b14a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b14a-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="4b14a-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4b14a-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4b14a-133">**BIDIoptions**</span><span class="sxs-lookup"><span data-stu-id="4b14a-133">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="4b14a-134">**em \_ GETbidioptions**</span><span class="sxs-lookup"><span data-stu-id="4b14a-134">**EM\_GETBIDIOPTIONS**</span></span>](em-getbidioptions.md)
</dt> </dl>

 

 





