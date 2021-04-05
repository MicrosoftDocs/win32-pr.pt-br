---
title: Mensagem de EM_GETPUNCTUATION (RichEdit. h)
description: Obtém os caracteres de Pontuação atuais para o controle de edição rico.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- Controles de EM_GETPUNCTUATION de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086095"
---
# <a name="em_getpunctuation-message"></a><span data-ttu-id="4279b-104">\_Mensagem em GETpontuation</span><span class="sxs-lookup"><span data-stu-id="4279b-104">EM\_GETPUNCTUATION message</span></span>

<span data-ttu-id="4279b-105">Obtém os caracteres de Pontuação atuais para o controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="4279b-105">Gets the current punctuation characters for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="4279b-106">Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="4279b-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="4279b-107">Não há suporte para ele em versões posteriores do rich edit.</span><span class="sxs-lookup"><span data-stu-id="4279b-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="4279b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4279b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4279b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4279b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4279b-110">O tipo de Pontuação pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4279b-110">The punctuation type can be one of the following values.</span></span>



| <span data-ttu-id="4279b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4279b-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="4279b-112">Significado</span><span class="sxs-lookup"><span data-stu-id="4279b-112">Meaning</span></span>                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="4279b-113"><dt>**líder do PC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4279b-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="4279b-114">Caracteres de Pontuação à esquerda</span><span class="sxs-lookup"><span data-stu-id="4279b-114">Leading punctuation characters</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="4279b-115"><dt>**PC a \_ seguir**</dt></span><span class="sxs-lookup"><span data-stu-id="4279b-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="4279b-116">Seguintes caracteres de Pontuação</span><span class="sxs-lookup"><span data-stu-id="4279b-116">Following punctuation characters</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="4279b-117"><dt>**delimitador de PC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4279b-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="4279b-118">Delimitador</span><span class="sxs-lookup"><span data-stu-id="4279b-118">Delimiter</span></span><br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <span data-ttu-id="4279b-119"><dt>**estouro de PC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4279b-119"><dt>**PC\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="4279b-120">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4279b-120">Not supported</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="4279b-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4279b-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4279b-122">Ponteiro para uma estrutura de [**Pontuação**](/windows/desktop/api/Richedit/ns-richedit-punctuation) que recebe os caracteres de pontuação.</span><span class="sxs-lookup"><span data-stu-id="4279b-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that receives the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4279b-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4279b-123">Return value</span></span>

<span data-ttu-id="4279b-124">Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="4279b-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4279b-125">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="4279b-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4279b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4279b-126">Requirements</span></span>



| <span data-ttu-id="4279b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4279b-127">Requirement</span></span> | <span data-ttu-id="4279b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4279b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4279b-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4279b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4279b-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4279b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4279b-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4279b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4279b-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4279b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4279b-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4279b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4279b-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4279b-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4279b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="4279b-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="4279b-136">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4279b-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4279b-137">**em \_ SETpontuation**</span><span class="sxs-lookup"><span data-stu-id="4279b-137">**EM\_SETPUNCTUATION**</span></span>](em-setpunctuation.md)
</dt> <dt>

[<span data-ttu-id="4279b-138">**Pontuação**</span><span class="sxs-lookup"><span data-stu-id="4279b-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





