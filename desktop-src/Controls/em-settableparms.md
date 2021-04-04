---
title: Mensagem de EM_SETTABLEPARMS (RichEdit. h)
description: Altera os parâmetros de linhas em uma tabela.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- Controles de EM_SETTABLEPARMS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918280"
---
# <a name="em_settableparms-message"></a><span data-ttu-id="1465d-104">\_Mensagem em SETTABLEPARMS</span><span class="sxs-lookup"><span data-stu-id="1465d-104">EM\_SETTABLEPARMS message</span></span>

<span data-ttu-id="1465d-105">Altera os parâmetros de linhas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="1465d-105">Changes the parameters of rows in a table.</span></span>

## <a name="parameters"></a><span data-ttu-id="1465d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1465d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1465d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1465d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1465d-108">Um ponteiro para uma estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="1465d-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1465d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1465d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1465d-110">Um ponteiro para uma estrutura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="1465d-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1465d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1465d-111">Return value</span></span>

<span data-ttu-id="1465d-112">Retorna S \_ OK se for bem-sucedido ou um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="1465d-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="1465d-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1465d-113">Return code</span></span>                                                                                    | <span data-ttu-id="1465d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1465d-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1465d-115"><dt>**E \_ FALHA**</dt></span><span class="sxs-lookup"><span data-stu-id="1465d-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="1465d-116">Não é possível fazer alterações.</span><span class="sxs-lookup"><span data-stu-id="1465d-116">Changes cannot be made.</span></span> <span data-ttu-id="1465d-117">Isso pode ocorrer se o controle for um controle de linha simples ou de texto sem formatação ou se o ponto de inserção estiver dentro de um objeto matemático.</span><span class="sxs-lookup"><span data-stu-id="1465d-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="1465d-118">Isso também ocorrerá se as tabelas estiverem desabilitadas ou se a mensagem em [**\_ SETEDITSTYLEEX**](em-seteditstyleex.md) definir o valor de **ses \_ ex \_ notável** .</span><span class="sxs-lookup"><span data-stu-id="1465d-118">It also occurs if tables are disabled, or if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="1465d-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1465d-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="1465d-120">*WParam* ou *lParam* é nulo ou aponta para uma estrutura inválida.</span><span class="sxs-lookup"><span data-stu-id="1465d-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="1465d-121">O membro **cCell** da estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve ser pelo menos 1 e não mais que 63.</span><span class="sxs-lookup"><span data-stu-id="1465d-121">The **cCell** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must be at least 1 and not more than 63.</span></span> <span data-ttu-id="1465d-122">O membro **cbRow** deve ser igual `sizeof(TABLEROWPARMS)` ou `sizeof(TABLEROWPARMS)   2*sizeof(long)` .</span><span class="sxs-lookup"><span data-stu-id="1465d-122">The **cbRow** member must equal `sizeof(TABLEROWPARMS)` or `sizeof(TABLEROWPARMS)   2*sizeof(long)`.</span></span> <span data-ttu-id="1465d-123">O último valor é o tamanho da estrutura RichEdit 4,1 **TABLEROWPARMS** .</span><span class="sxs-lookup"><span data-stu-id="1465d-123">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="1465d-124">O membro **cbCell** de **TABLEROWPARMS** deve ser igual `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="1465d-124">The **cbCell** member of **TABLEROWPARMS** must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="1465d-125">O ponto de inserção deve estar no início de uma tabela ou dentro de uma linha de tabela, e o número de células só pode ser alterado por um.</span><span class="sxs-lookup"><span data-stu-id="1465d-125">The insertion point must be at the start of a table or inside a table row, and the number of cells can only change by one.</span></span> |
| <dl> <span data-ttu-id="1465d-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1465d-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="1465d-127">Memória insuficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="1465d-127">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="1465d-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="1465d-128">Remarks</span></span>

<span data-ttu-id="1465d-129">Essa mensagem altera os parâmetros do número de linhas especificado pelo membro de **galinha** da estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) , se a tabela tiver várias linhas consecutivas.</span><span class="sxs-lookup"><span data-stu-id="1465d-129">This message changes the parameters of the number of rows specified by the **cRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, if the table has that many consecutive rows.</span></span> <span data-ttu-id="1465d-130">Se **galinha** for menor que 0, a mensagem será iterada até o final da tabela.</span><span class="sxs-lookup"><span data-stu-id="1465d-130">If **cRow** is less than 0, the message iterates until the end of the table.</span></span> <span data-ttu-id="1465d-131">Se a nova contagem de células for diferente da contagem de células atual por + 1 ou 1, ela inserirá ou excluirá a célula no índice especificado pelo membro **iCell** de **TABLEROWPARMS**.</span><span class="sxs-lookup"><span data-stu-id="1465d-131">If the new cell count differs from the current cell count by +1 or  1, it inserts or deletes the cell at the index specified by the **iCell** member of **TABLEROWPARMS**.</span></span> <span data-ttu-id="1465d-132">A linha de tabela inicial é identificada por uma posição de caractere.</span><span class="sxs-lookup"><span data-stu-id="1465d-132">The starting table row is identified by a character position.</span></span> <span data-ttu-id="1465d-133">Essa posição é especificada por membros **cpStartRow** com valores maiores ou iguais a zero.</span><span class="sxs-lookup"><span data-stu-id="1465d-133">This position is specified by **cpStartRow** members with values that are greater than or equal to zero.</span></span> <span data-ttu-id="1465d-134">A posição deve estar dentro da linha da tabela, mas não dentro de uma tabela aninhada, a menos que você queira alterar os parâmetros da tabela.</span><span class="sxs-lookup"><span data-stu-id="1465d-134">The position should be inside the table row, but not inside a nested table, unless you want to change that table s parameters.</span></span> <span data-ttu-id="1465d-135">Se o membro **cpStartRow** for 1, a posição do caractere será fornecida pela seleção atual.</span><span class="sxs-lookup"><span data-stu-id="1465d-135">If the **cpStartRow** member is  1, the character position is given by the current selection.</span></span> <span data-ttu-id="1465d-136">Para isso, posicione a seleção em qualquer lugar dentro da linha da tabela ou selecione a linha com a extremidade ativa da seleção no final da linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="1465d-136">For this, position the selection anywhere inside the table row, or select the row with the active end of the selection at the end of the table row.</span></span>

## <a name="requirements"></a><span data-ttu-id="1465d-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1465d-137">Requirements</span></span>



| <span data-ttu-id="1465d-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="1465d-138">Requirement</span></span> | <span data-ttu-id="1465d-139">Valor</span><span class="sxs-lookup"><span data-stu-id="1465d-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1465d-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1465d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1465d-141">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1465d-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1465d-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1465d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1465d-143">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1465d-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1465d-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1465d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="1465d-145"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1465d-145"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1465d-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="1465d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1465d-147">**em \_ GETTABLEPARMS**</span><span class="sxs-lookup"><span data-stu-id="1465d-147">**EM\_GETTABLEPARMS**</span></span>](em-gettableparms.md)
</dt> </dl>

 

 





