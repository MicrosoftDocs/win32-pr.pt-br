---
description: As linhas de uma caixa de listagem não são tratadas como controles individuais, mas fazem parte de uma caixa de listagem que funciona como um controle. A tabela ListBox define os valores para todas as caixas de listagem.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: Tabela de ListBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922017"
---
# <a name="listbox-table"></a><span data-ttu-id="150dc-104">Tabela de ListBox</span><span class="sxs-lookup"><span data-stu-id="150dc-104">ListBox Table</span></span>

<span data-ttu-id="150dc-105">As linhas de uma caixa de listagem não são tratadas como controles individuais, mas fazem parte de uma caixa de listagem que funciona como um controle.</span><span class="sxs-lookup"><span data-stu-id="150dc-105">The lines of a list box are not treated as individual controls, but they are part of a list box that functions as a control.</span></span> <span data-ttu-id="150dc-106">A tabela ListBox define os valores para todas as caixas de listagem.</span><span class="sxs-lookup"><span data-stu-id="150dc-106">The ListBox table defines the values for all list boxes.</span></span>

<span data-ttu-id="150dc-107">A tabela ListBox tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="150dc-107">The ListBox table has the following columns.</span></span>



| <span data-ttu-id="150dc-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="150dc-108">Column</span></span>   | <span data-ttu-id="150dc-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="150dc-109">Type</span></span>                         | <span data-ttu-id="150dc-110">Chave</span><span class="sxs-lookup"><span data-stu-id="150dc-110">Key</span></span> | <span data-ttu-id="150dc-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="150dc-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="150dc-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="150dc-112">Property</span></span> | [<span data-ttu-id="150dc-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="150dc-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="150dc-114">S</span><span class="sxs-lookup"><span data-stu-id="150dc-114">Y</span></span>   | <span data-ttu-id="150dc-115">N</span><span class="sxs-lookup"><span data-stu-id="150dc-115">N</span></span>        |
| <span data-ttu-id="150dc-116">Ordem</span><span class="sxs-lookup"><span data-stu-id="150dc-116">Order</span></span>    | [<span data-ttu-id="150dc-117">Inteiro</span><span class="sxs-lookup"><span data-stu-id="150dc-117">Integer</span></span>](integer.md)       | <span data-ttu-id="150dc-118">S</span><span class="sxs-lookup"><span data-stu-id="150dc-118">Y</span></span>   | <span data-ttu-id="150dc-119">N</span><span class="sxs-lookup"><span data-stu-id="150dc-119">N</span></span>        |
| <span data-ttu-id="150dc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="150dc-120">Value</span></span>    | [<span data-ttu-id="150dc-121">Binário</span><span class="sxs-lookup"><span data-stu-id="150dc-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="150dc-122">N</span><span class="sxs-lookup"><span data-stu-id="150dc-122">N</span></span>   | <span data-ttu-id="150dc-123">N</span><span class="sxs-lookup"><span data-stu-id="150dc-123">N</span></span>        |
| <span data-ttu-id="150dc-124">Texto</span><span class="sxs-lookup"><span data-stu-id="150dc-124">Text</span></span>     | [<span data-ttu-id="150dc-125">Binário</span><span class="sxs-lookup"><span data-stu-id="150dc-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="150dc-126">N</span><span class="sxs-lookup"><span data-stu-id="150dc-126">N</span></span>   | <span data-ttu-id="150dc-127">S</span><span class="sxs-lookup"><span data-stu-id="150dc-127">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="150dc-128">Colunas</span><span class="sxs-lookup"><span data-stu-id="150dc-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="150dc-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade</span><span class="sxs-lookup"><span data-stu-id="150dc-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="150dc-130">Uma propriedade nomeada a ser vinculada a este item.</span><span class="sxs-lookup"><span data-stu-id="150dc-130">A named property to be tied to this item.</span></span> <span data-ttu-id="150dc-131">Todos os itens vinculados à mesma propriedade se tornam parte da mesma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="150dc-131">All the items tied to the same property become part of the same list box.</span></span>

</dd> <dt>

<span data-ttu-id="150dc-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordene</span><span class="sxs-lookup"><span data-stu-id="150dc-132"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="150dc-133">Um inteiro positivo usado para determinar a ordem dos itens que aparecem em uma única caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="150dc-133">A positive integer used to determine the ordering of the items that appear in a single list box.</span></span> <span data-ttu-id="150dc-134">Se a caixa de listagem for definida como ordenada, todos os itens deverão ter um valor de pedido.</span><span class="sxs-lookup"><span data-stu-id="150dc-134">If the list box is defined as ordered, then all items should have an Order value.</span></span> <span data-ttu-id="150dc-135">Os inteiros não precisam ser consecutivos.</span><span class="sxs-lookup"><span data-stu-id="150dc-135">The integers do not have to be consecutive.</span></span> <span data-ttu-id="150dc-136">Se a caixa de listagem for definida como não ordenada, essa coluna será ignorada.</span><span class="sxs-lookup"><span data-stu-id="150dc-136">If the list box is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="150dc-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="150dc-137"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="150dc-138">A cadeia de caracteres de valor associada a este item.</span><span class="sxs-lookup"><span data-stu-id="150dc-138">The value string associated with this item.</span></span> <span data-ttu-id="150dc-139">A seleção da linha define a propriedade associada a esse valor.</span><span class="sxs-lookup"><span data-stu-id="150dc-139">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="150dc-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto</span><span class="sxs-lookup"><span data-stu-id="150dc-140"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="150dc-141">O texto localizável visível a ser atribuído ao item.</span><span class="sxs-lookup"><span data-stu-id="150dc-141">The localizable, visible text to be assigned to the item.</span></span> <span data-ttu-id="150dc-142">Se essa entrada ou a coluna inteira estiver ausente, o texto assume como padrão a entrada correspondente no valor.</span><span class="sxs-lookup"><span data-stu-id="150dc-142">If this entry or the entire column is missing, the text defaults to the corresponding entry in Value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="150dc-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="150dc-143">Remarks</span></span>

<span data-ttu-id="150dc-144">O conteúdo dos campos Value e Text são formatados pela função [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando o controle é criado, portanto, eles podem conter qualquer expressão que a função **MsiFormatRecord** possa interpretar.</span><span class="sxs-lookup"><span data-stu-id="150dc-144">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="150dc-145">A formatação ocorre somente quando o controle é criado e não é atualizada se uma propriedade envolvida na expressão é modificada durante a vida útil do controle.</span><span class="sxs-lookup"><span data-stu-id="150dc-145">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="150dc-146">Validação</span><span class="sxs-lookup"><span data-stu-id="150dc-146">Validation</span></span>

<dl>

[<span data-ttu-id="150dc-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="150dc-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="150dc-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="150dc-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="150dc-149">ICE17</span><span class="sxs-lookup"><span data-stu-id="150dc-149">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="150dc-150">ICE20</span><span class="sxs-lookup"><span data-stu-id="150dc-150">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="150dc-151">ICE46</span><span class="sxs-lookup"><span data-stu-id="150dc-151">ICE46</span></span>](ice46.md)  
</dl>

 

 



