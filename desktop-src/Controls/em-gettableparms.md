---
title: Mensagem de EM_GETTABLEPARMS (RichEdit. h)
description: Recupera os parâmetros de tabela para uma linha de tabela e os parâmetros de célula para o número especificado de células.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- Controles de EM_GETTABLEPARMS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eb244b64258b1cf83559e21affea51b1d0c5d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824363"
---
# <a name="em_gettableparms-message"></a><span data-ttu-id="cfa51-104">\_Mensagem em GETTABLEPARMS</span><span class="sxs-lookup"><span data-stu-id="cfa51-104">EM\_GETTABLEPARMS message</span></span>

<span data-ttu-id="cfa51-105">Recupera os parâmetros de tabela para uma linha de tabela e os parâmetros de célula para o número especificado de células.</span><span class="sxs-lookup"><span data-stu-id="cfa51-105">Retrieves the table parameters for a table row and the cell parameters for the specified number of cells.</span></span>


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
```



## <a name="parameters"></a><span data-ttu-id="cfa51-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfa51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfa51-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfa51-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfa51-108">Um ponteiro para uma estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .</span><span class="sxs-lookup"><span data-stu-id="cfa51-108">A pointer to a [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cfa51-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfa51-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfa51-110">Um ponteiro para uma estrutura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="cfa51-110">A pointer to a [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfa51-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cfa51-111">Return value</span></span>

<span data-ttu-id="cfa51-112">Retorna S \_ OK se for bem-sucedido ou um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="cfa51-112">Returns S\_OK if successful, or one of the following error codes.</span></span>



| <span data-ttu-id="cfa51-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cfa51-113">Return code</span></span>                                                                                    | <span data-ttu-id="cfa51-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cfa51-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cfa51-115"><dt>**E \_ FALHA**</dt></span><span class="sxs-lookup"><span data-stu-id="cfa51-115"><dt>**E\_FAIL** </dt></span></span> </dl>        | <span data-ttu-id="cfa51-116">Não é possível fazer alterações.</span><span class="sxs-lookup"><span data-stu-id="cfa51-116">Changes cannot be made.</span></span> <span data-ttu-id="cfa51-117">Isso pode ocorrer se o controle for um controle de linha simples ou de texto sem formatação ou se o ponto de inserção estiver dentro de um objeto matemático.</span><span class="sxs-lookup"><span data-stu-id="cfa51-117">This can occur if the control is a plain-text or single-line control, or if the insertion point is inside a math object.</span></span> <span data-ttu-id="cfa51-118">Isso também ocorrerá se as tabelas estiverem desabilitadas se a mensagem em [**\_ SETEDITSTYLEEX**](em-seteditstyleex.md) definir o valor de **ses \_ ex \_ notável** .</span><span class="sxs-lookup"><span data-stu-id="cfa51-118">It also occurs if tables are disabled if the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message sets the **SES\_EX\_NOTABLE** value.</span></span> <br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="cfa51-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cfa51-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="cfa51-120">*WParam* ou *lParam* é nulo ou aponta para uma estrutura inválida.</span><span class="sxs-lookup"><span data-stu-id="cfa51-120">The *wParam* or *lParam* is NULL or points to an invalid structure.</span></span> <span data-ttu-id="cfa51-121">O membro **cbRow** da estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve ser igual `sizeof(TABLEROWPARMS)` ou sizeof (TABLEROWPARMS) 2 \* sizeof (Long).</span><span class="sxs-lookup"><span data-stu-id="cfa51-121">The **cbRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure must equal `sizeof(TABLEROWPARMS)` or sizeof(TABLEROWPARMS)   2\*sizeof(long).</span></span> <span data-ttu-id="cfa51-122">O último valor é o tamanho da estrutura RichEdit 4,1 **TABLEROWPARMS** .</span><span class="sxs-lookup"><span data-stu-id="cfa51-122">The latter value is the size of the RichEdit 4.1 **TABLEROWPARMS** structure.</span></span> <span data-ttu-id="cfa51-123">O membro **cbCell** da estrutura **TABLEROWPARMS** deve ser igual `sizeof(TABLECELLPARMS)` .</span><span class="sxs-lookup"><span data-stu-id="cfa51-123">The **cbCell** member of the **TABLEROWPARMS** structure must equal `sizeof(TABLECELLPARMS)`.</span></span> <span data-ttu-id="cfa51-124">A posição do caractere de consulta deve estar em um delimitador de linha de tabela.</span><span class="sxs-lookup"><span data-stu-id="cfa51-124">The query character position must be at a table row delimiter.</span></span> |
| <dl> <span data-ttu-id="cfa51-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cfa51-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl> | <span data-ttu-id="cfa51-126">Memória insuficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="cfa51-126">Insufficient memory is available.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="cfa51-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfa51-127">Remarks</span></span>

<span data-ttu-id="cfa51-128">Essa mensagem obtém os parâmetros de tabela para a linha na posição de caractere especificada pelo membro **cpStartRow** da estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) e o número de células especificado pelo membro **cCells** da estrutura [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .</span><span class="sxs-lookup"><span data-stu-id="cfa51-128">This message gets the table parameters for the row at the character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure, and the number of cells specified by the **cCells** member of the [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) structure.</span></span>

<span data-ttu-id="cfa51-129">A posição do caractere especificada pelo membro **cpStartRow** da estrutura [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) deve estar no início da linha da tabela ou no delimitador final da linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="cfa51-129">The character position specified by the **cpStartRow** member of the [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) structure should be at the start of the table row, or at the end delimiter of the table row.</span></span> <span data-ttu-id="cfa51-130">Se **cpStartRow** for definido como 1, a posição do caractere será fornecida pela seleção atual.</span><span class="sxs-lookup"><span data-stu-id="cfa51-130">If **cpStartRow** is set to  1, the character position is given by the current selection.</span></span> <span data-ttu-id="cfa51-131">Nesse caso, posicione a seleção no final da linha (entre a marca de célula e o delimitador final da linha da tabela) ou selecione a linha.</span><span class="sxs-lookup"><span data-stu-id="cfa51-131">In this case, position the selection at the end of the row (between the cell mark and the end delimiter of the table row), or select the row.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa51-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfa51-132">Requirements</span></span>



| <span data-ttu-id="cfa51-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfa51-133">Requirement</span></span> | <span data-ttu-id="cfa51-134">Valor</span><span class="sxs-lookup"><span data-stu-id="cfa51-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa51-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfa51-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa51-136">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cfa51-136">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cfa51-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfa51-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa51-138">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cfa51-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfa51-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cfa51-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfa51-140"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfa51-140"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfa51-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfa51-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa51-142">**em \_ SETTABLEPARMS**</span><span class="sxs-lookup"><span data-stu-id="cfa51-142">**EM\_SETTABLEPARMS**</span></span>](em-settableparms.md)
</dt> </dl>

 

 





