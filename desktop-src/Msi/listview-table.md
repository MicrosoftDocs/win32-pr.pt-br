---
description: As linhas de ListView não são tratadas como controles individuais, mas fazem parte de um ListView que funciona como um controle. A tabela ListView define os valores para todos os ListViews.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: Tabela ListView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770192"
---
# <a name="listview-table"></a><span data-ttu-id="25103-104">Tabela ListView</span><span class="sxs-lookup"><span data-stu-id="25103-104">ListView Table</span></span>

<span data-ttu-id="25103-105">As linhas de ListView não são tratadas como controles individuais, mas fazem parte de um ListView que funciona como um controle.</span><span class="sxs-lookup"><span data-stu-id="25103-105">The lines of a listview are not treated as individual controls, but they are part of a listview that functions as a control.</span></span> <span data-ttu-id="25103-106">A tabela ListView define os valores para todos os ListViews.</span><span class="sxs-lookup"><span data-stu-id="25103-106">The ListView table defines the values for all listviews.</span></span>

<span data-ttu-id="25103-107">A tabela ListView tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="25103-107">The ListView table has the following columns.</span></span>



| <span data-ttu-id="25103-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="25103-108">Column</span></span>   | <span data-ttu-id="25103-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="25103-109">Type</span></span>                         | <span data-ttu-id="25103-110">Chave</span><span class="sxs-lookup"><span data-stu-id="25103-110">Key</span></span> | <span data-ttu-id="25103-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="25103-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="25103-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="25103-112">Property</span></span> | [<span data-ttu-id="25103-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="25103-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="25103-114">S</span><span class="sxs-lookup"><span data-stu-id="25103-114">Y</span></span>   | <span data-ttu-id="25103-115">N</span><span class="sxs-lookup"><span data-stu-id="25103-115">N</span></span>        |
| <span data-ttu-id="25103-116">Ordem</span><span class="sxs-lookup"><span data-stu-id="25103-116">Order</span></span>    | [<span data-ttu-id="25103-117">Inteiro</span><span class="sxs-lookup"><span data-stu-id="25103-117">Integer</span></span>](integer.md)       | <span data-ttu-id="25103-118">S</span><span class="sxs-lookup"><span data-stu-id="25103-118">Y</span></span>   | <span data-ttu-id="25103-119">N</span><span class="sxs-lookup"><span data-stu-id="25103-119">N</span></span>        |
| <span data-ttu-id="25103-120">Valor</span><span class="sxs-lookup"><span data-stu-id="25103-120">Value</span></span>    | [<span data-ttu-id="25103-121">Binário</span><span class="sxs-lookup"><span data-stu-id="25103-121">Formatted</span></span>](formatted.md)   | <span data-ttu-id="25103-122">N</span><span class="sxs-lookup"><span data-stu-id="25103-122">N</span></span>   | <span data-ttu-id="25103-123">N</span><span class="sxs-lookup"><span data-stu-id="25103-123">N</span></span>        |
| <span data-ttu-id="25103-124">Texto</span><span class="sxs-lookup"><span data-stu-id="25103-124">Text</span></span>     | [<span data-ttu-id="25103-125">Binário</span><span class="sxs-lookup"><span data-stu-id="25103-125">Formatted</span></span>](formatted.md)   | <span data-ttu-id="25103-126">N</span><span class="sxs-lookup"><span data-stu-id="25103-126">N</span></span>   | <span data-ttu-id="25103-127">S</span><span class="sxs-lookup"><span data-stu-id="25103-127">Y</span></span>        |
| <span data-ttu-id="25103-128">Binário\_</span><span class="sxs-lookup"><span data-stu-id="25103-128">Binary\_</span></span> | [<span data-ttu-id="25103-129">Identificador</span><span class="sxs-lookup"><span data-stu-id="25103-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="25103-130">N</span><span class="sxs-lookup"><span data-stu-id="25103-130">N</span></span>   | <span data-ttu-id="25103-131">S</span><span class="sxs-lookup"><span data-stu-id="25103-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="25103-132">Colunas</span><span class="sxs-lookup"><span data-stu-id="25103-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="25103-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade</span><span class="sxs-lookup"><span data-stu-id="25103-133"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="25103-134">Uma propriedade nomeada a ser vinculada a este item.</span><span class="sxs-lookup"><span data-stu-id="25103-134">A named property to be tied to this item.</span></span> <span data-ttu-id="25103-135">Todos os itens vinculados à mesma propriedade se tornam parte do mesmo ListView.</span><span class="sxs-lookup"><span data-stu-id="25103-135">All the items tied to the same property become part of the same listview.</span></span>

</dd> <dt>

<span data-ttu-id="25103-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordene</span><span class="sxs-lookup"><span data-stu-id="25103-136"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="25103-137">Um inteiro positivo usado para determinar a ordem dos itens que aparecem em uma única lista de ListView.</span><span class="sxs-lookup"><span data-stu-id="25103-137">A positive integer used to determine the ordering of the items that appear in a single listview list.</span></span> <span data-ttu-id="25103-138">Os inteiros não precisam ser consecutivos.</span><span class="sxs-lookup"><span data-stu-id="25103-138">The integers do not have to be consecutive.</span></span> <span data-ttu-id="25103-139">Se um ListView for definido como ordenado, todos os itens deverão ter um valor de ordenação.</span><span class="sxs-lookup"><span data-stu-id="25103-139">If a listview is defined as ordered, then all the items should have an Ordering value.</span></span> <span data-ttu-id="25103-140">Se ListView for definido como não ordenado, essa coluna será ignorada.</span><span class="sxs-lookup"><span data-stu-id="25103-140">If the listview is defined as unordered, then this column is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="25103-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="25103-141"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="25103-142">A cadeia de caracteres de valor associada a este item.</span><span class="sxs-lookup"><span data-stu-id="25103-142">The value string associated with this item.</span></span> <span data-ttu-id="25103-143">A seleção da linha define a propriedade associada a esse valor.</span><span class="sxs-lookup"><span data-stu-id="25103-143">Selecting the line sets the associated property to this value.</span></span>

</dd> <dt>

<span data-ttu-id="25103-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto</span><span class="sxs-lookup"><span data-stu-id="25103-144"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="25103-145">O texto que está visível e localizável a ser atribuído ao item.</span><span class="sxs-lookup"><span data-stu-id="25103-145">The visible, localizable text to be assigned to the item.</span></span> <span data-ttu-id="25103-146">Se essa entrada ou a coluna inteira estiver ausente, o texto usa como padrão a entrada correspondente no valor.</span><span class="sxs-lookup"><span data-stu-id="25103-146">If this entry or the entire column is missing, then the text defaults to the corresponding entry in Value.</span></span>

</dd> <dt>

<span data-ttu-id="25103-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binário\_</span><span class="sxs-lookup"><span data-stu-id="25103-147"><span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binary\_</span></span>
</dt> <dd>

<span data-ttu-id="25103-148">Os dados da imagem para o ícone.</span><span class="sxs-lookup"><span data-stu-id="25103-148">The image data for the icon.</span></span> <span data-ttu-id="25103-149">Esta é uma chave estrangeira para a [tabela binária](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="25103-149">This is a foreign key to the [Binary table](binary-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25103-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="25103-150">Remarks</span></span>

<span data-ttu-id="25103-151">O conteúdo dos campos Value e Text são formatados pela função [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando o controle é criado, portanto, eles podem conter qualquer expressão que a função MsiFormatRecord possa interpretar.</span><span class="sxs-lookup"><span data-stu-id="25103-151">The contents of the Value and Text fields are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created, therefore they can contain any expression that the MsiFormatRecord function can interpret.</span></span> <span data-ttu-id="25103-152">A formatação ocorre somente quando o controle é criado e não é atualizada se uma propriedade envolvida na expressão é modificada durante a vida útil do controle.</span><span class="sxs-lookup"><span data-stu-id="25103-152">The formatting occurs only when the control is created, and it is not updated if a property involved in the expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="25103-153">Validação</span><span class="sxs-lookup"><span data-stu-id="25103-153">Validation</span></span>

<dl>

[<span data-ttu-id="25103-154">ICE03</span><span class="sxs-lookup"><span data-stu-id="25103-154">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="25103-155">ICE06</span><span class="sxs-lookup"><span data-stu-id="25103-155">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="25103-156">ICE17</span><span class="sxs-lookup"><span data-stu-id="25103-156">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="25103-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="25103-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



