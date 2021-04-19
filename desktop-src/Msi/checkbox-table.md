---
description: A tabela de caixa de seleção lista os valores para as caixas de seleção.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: Tabela de caixas de seleção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756740"
---
# <a name="checkbox-table"></a><span data-ttu-id="2d622-103">Tabela de caixas de seleção</span><span class="sxs-lookup"><span data-stu-id="2d622-103">CheckBox Table</span></span>

<span data-ttu-id="2d622-104">A tabela de caixa de seleção lista os valores para as caixas de seleção.</span><span class="sxs-lookup"><span data-stu-id="2d622-104">The CheckBox table lists the values for the check boxes.</span></span>

<span data-ttu-id="2d622-105">A tabela de caixas de seleção tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d622-105">The CheckBox table has the following columns.</span></span>



| <span data-ttu-id="2d622-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="2d622-106">Column</span></span>   | <span data-ttu-id="2d622-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d622-107">Type</span></span>                         | <span data-ttu-id="2d622-108">Chave</span><span class="sxs-lookup"><span data-stu-id="2d622-108">Key</span></span> | <span data-ttu-id="2d622-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="2d622-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="2d622-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2d622-110">Property</span></span> | [<span data-ttu-id="2d622-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="2d622-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="2d622-112">S</span><span class="sxs-lookup"><span data-stu-id="2d622-112">Y</span></span>   | <span data-ttu-id="2d622-113">N</span><span class="sxs-lookup"><span data-stu-id="2d622-113">N</span></span>        |
| <span data-ttu-id="2d622-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2d622-114">Value</span></span>    | [<span data-ttu-id="2d622-115">Binário</span><span class="sxs-lookup"><span data-stu-id="2d622-115">Formatted</span></span>](formatted.md)   | <span data-ttu-id="2d622-116">N</span><span class="sxs-lookup"><span data-stu-id="2d622-116">N</span></span>   | <span data-ttu-id="2d622-117">S</span><span class="sxs-lookup"><span data-stu-id="2d622-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2d622-118">Colunas</span><span class="sxs-lookup"><span data-stu-id="2d622-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2d622-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade</span><span class="sxs-lookup"><span data-stu-id="2d622-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="2d622-120">Uma propriedade nomeada a ser vinculada a este item.</span><span class="sxs-lookup"><span data-stu-id="2d622-120">A named property to be tied to this item.</span></span>

</dd> <dt>

<span data-ttu-id="2d622-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="2d622-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="2d622-122">A cadeia de caracteres de valor associada a este item.</span><span class="sxs-lookup"><span data-stu-id="2d622-122">The value string associated with this item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d622-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d622-123">Remarks</span></span>

<span data-ttu-id="2d622-124">Se a caixa de seleção estiver marcada, a propriedade correspondente será definida como o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2d622-124">If the check box is selected, then the corresponding property is set to the specified value.</span></span> <span data-ttu-id="2d622-125">Se não houver nenhum valor especificado ou essa tabela não existir, a propriedade será definida como seu valor original quando a caixa de seleção estiver marcada.</span><span class="sxs-lookup"><span data-stu-id="2d622-125">If there is no value specified or this table does not exist, then the property is set to its original value when the check box is selected.</span></span> <span data-ttu-id="2d622-126">Se o valor original for NULL, a propriedade será definida como "1".</span><span class="sxs-lookup"><span data-stu-id="2d622-126">If the original value is null, the property is set to "1".</span></span>

<span data-ttu-id="2d622-127">O conteúdo da coluna valor é formatado pela função [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando o controle é criado.</span><span class="sxs-lookup"><span data-stu-id="2d622-127">The contents of the Value column are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created.</span></span> <span data-ttu-id="2d622-128">Portanto, ele pode conter qualquer expressão que a função **MsiFormatRecord** possa interpretar.</span><span class="sxs-lookup"><span data-stu-id="2d622-128">Therefore, it can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="2d622-129">A coluna valor é formatada somente quando o controle é criado e não é atualizada se uma propriedade envolvida em uma expressão é modificada durante a vida útil do controle.</span><span class="sxs-lookup"><span data-stu-id="2d622-129">The Value column is formatted only when the control is created, and it is not updated if a property involved in an expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="2d622-130">Validação</span><span class="sxs-lookup"><span data-stu-id="2d622-130">Validation</span></span>

<dl>

[<span data-ttu-id="2d622-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="2d622-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2d622-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="2d622-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2d622-133">ICE46</span><span class="sxs-lookup"><span data-stu-id="2d622-133">ICE46</span></span>](ice46.md)  
</dl>

 

 



