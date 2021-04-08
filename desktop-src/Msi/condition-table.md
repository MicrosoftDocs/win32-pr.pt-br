---
description: A tabela de condição pode ser usada para modificar o estado de seleção de qualquer entrada na tabela de recursos com base em uma expressão condicional.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Tabela de condição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d9a3c27d43b7d71bc8e5b0593771bc86a3ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920720"
---
# <a name="condition-table"></a><span data-ttu-id="461f1-103">Tabela de condição</span><span class="sxs-lookup"><span data-stu-id="461f1-103">Condition Table</span></span>

<span data-ttu-id="461f1-104">A tabela de condição pode ser usada para modificar o estado de seleção de qualquer entrada na [tabela de recursos](feature-table.md) com base em uma expressão condicional.</span><span class="sxs-lookup"><span data-stu-id="461f1-104">The Condition table can be used to modify the selection state of any entry in the [Feature table](feature-table.md) based on a conditional expression.</span></span>

<span data-ttu-id="461f1-105">A tabela de condições tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="461f1-105">The Condition table has the following columns.</span></span>



| <span data-ttu-id="461f1-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="461f1-106">Column</span></span>    | <span data-ttu-id="461f1-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="461f1-107">Type</span></span>                         | <span data-ttu-id="461f1-108">Chave</span><span class="sxs-lookup"><span data-stu-id="461f1-108">Key</span></span> | <span data-ttu-id="461f1-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="461f1-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="461f1-110">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="461f1-110">Feature\_</span></span> | [<span data-ttu-id="461f1-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="461f1-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="461f1-112">S</span><span class="sxs-lookup"><span data-stu-id="461f1-112">Y</span></span>   | <span data-ttu-id="461f1-113">N</span><span class="sxs-lookup"><span data-stu-id="461f1-113">N</span></span>        |
| <span data-ttu-id="461f1-114">Nível</span><span class="sxs-lookup"><span data-stu-id="461f1-114">Level</span></span>     | [<span data-ttu-id="461f1-115">Inteiro</span><span class="sxs-lookup"><span data-stu-id="461f1-115">Integer</span></span>](integer.md)       | <span data-ttu-id="461f1-116">S</span><span class="sxs-lookup"><span data-stu-id="461f1-116">Y</span></span>   | <span data-ttu-id="461f1-117">N</span><span class="sxs-lookup"><span data-stu-id="461f1-117">N</span></span>        |
| <span data-ttu-id="461f1-118">Condição</span><span class="sxs-lookup"><span data-stu-id="461f1-118">Condition</span></span> | [<span data-ttu-id="461f1-119">Condição</span><span class="sxs-lookup"><span data-stu-id="461f1-119">Condition</span></span>](condition.md)   | <span data-ttu-id="461f1-120">N</span><span class="sxs-lookup"><span data-stu-id="461f1-120">N</span></span>   | <span data-ttu-id="461f1-121">S</span><span class="sxs-lookup"><span data-stu-id="461f1-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="461f1-122">Colunas</span><span class="sxs-lookup"><span data-stu-id="461f1-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="461f1-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_</span><span class="sxs-lookup"><span data-stu-id="461f1-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="461f1-124">Chave externa na coluna um da tabela de recursos.</span><span class="sxs-lookup"><span data-stu-id="461f1-124">External key into column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Geral</span><span class="sxs-lookup"><span data-stu-id="461f1-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Level</span></span>
</dt> <dd>

<span data-ttu-id="461f1-126">Um nível de instalação condicional para o recurso na \_ coluna recurso desta tabela.</span><span class="sxs-lookup"><span data-stu-id="461f1-126">A conditional install level for the feature in the Feature\_ column of this table.</span></span> <span data-ttu-id="461f1-127">O instalador definirá o nível de instalação desse recurso para o nível especificado nesta coluna se a expressão na coluna condição for avaliada como TRUE.</span><span class="sxs-lookup"><span data-stu-id="461f1-127">The installer sets the install level of this feature to the level specified in this column if the expression in the Condition column evaluates to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="461f1-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="461f1-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="461f1-129">Se essa expressão condicional for avaliada como TRUE, a coluna nível na tabela de recursos será definida como o nível de instalação condicional.</span><span class="sxs-lookup"><span data-stu-id="461f1-129">If this conditional expression evaluates to TRUE, then the Level column in the Feature table is set to the conditional install level.</span></span>

<span data-ttu-id="461f1-130">A expressão na coluna condição não deve conter referência ao estado instalado de qualquer recurso ou componente.</span><span class="sxs-lookup"><span data-stu-id="461f1-130">The expression in the Condition column should not contain reference to the installed state of any feature or component.</span></span> <span data-ttu-id="461f1-131">Isso ocorre porque as expressões na coluna condição são avaliadas antes que o instalador avalie os Estados instalados de recursos e componentes.</span><span class="sxs-lookup"><span data-stu-id="461f1-131">This is because the expressions in the Condition column are evaluated before the installer evaluates the installed states of features and components.</span></span> <span data-ttu-id="461f1-132">Qualquer expressão na tabela de condição que tenta verificar o estado instalado de um recurso ou componente sempre é avaliada como false.</span><span class="sxs-lookup"><span data-stu-id="461f1-132">Any expression in the Condition table that attempts to check the installed state of a feature or component always evaluates to false.</span></span>

<span data-ttu-id="461f1-133">Para obter informações sobre a sintaxe de instruções condicionais, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="461f1-133">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="461f1-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="461f1-134">Remarks</span></span>

<span data-ttu-id="461f1-135">Um recurso pode ser desabilitado permanentemente definindo a coluna nível como 0.</span><span class="sxs-lookup"><span data-stu-id="461f1-135">A feature can be permanently disabled by setting the Level column to 0.</span></span>

<span data-ttu-id="461f1-136">O nível pode ser definido com base em qualquer instrução condicional, como um teste para plataforma, sistema operacional ou uma configuração de propriedade específica.</span><span class="sxs-lookup"><span data-stu-id="461f1-136">The Level may be set based on any conditional statement, such as a test for platform, operating system, or a particular property setting.</span></span>

<span data-ttu-id="461f1-137">As condições devem ser cuidadosamente escolhidas para que um recurso não seja habilitado na instalação e, em seguida, desabilitado na desinstalação.</span><span class="sxs-lookup"><span data-stu-id="461f1-137">Conditions should be carefully chosen so that a feature is not enabled on install and then disabled on uninstall.</span></span> <span data-ttu-id="461f1-138">Isso deixará o recurso órfão e o produto não será capaz de ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="461f1-138">This will orphan the feature and the product will not be able to be uninstalled.</span></span>

<span data-ttu-id="461f1-139">Essa tabela é referida quando a [ação CostFinalize](costfinalize-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="461f1-139">This table is referred to when the [CostFinalize action](costfinalize-action.md) is executed.</span></span>

<span data-ttu-id="461f1-140">Se a propriedade [**preselecionada**](preselected.md) tiver sido definida como 1, o instalador não avaliará a tabela de condições.</span><span class="sxs-lookup"><span data-stu-id="461f1-140">If the [**Preselected**](preselected.md) property has been set to 1, the installer does not evaluate the Condition table.</span></span> <span data-ttu-id="461f1-141">A tabela de condição afeta apenas a instalação de recursos quando nenhuma das propriedades a seguir foi definida:</span><span class="sxs-lookup"><span data-stu-id="461f1-141">The Condition table affects only the installation of features when none of the following properties have been set:</span></span>

<dl>

[<span data-ttu-id="461f1-142">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="461f1-142">**ADDLOCAL**</span></span>](addlocal.md)  
[<span data-ttu-id="461f1-143">**EXCLU**</span><span class="sxs-lookup"><span data-stu-id="461f1-143">**REMOVE**</span></span>](remove.md)  
[<span data-ttu-id="461f1-144">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="461f1-144">**ADDSOURCE**</span></span>](addsource.md)  
[<span data-ttu-id="461f1-145">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="461f1-145">**ADDDEFAULT**</span></span>](adddefault.md)  
[<span data-ttu-id="461f1-146">**Install**</span><span class="sxs-lookup"><span data-stu-id="461f1-146">**REINSTALL**</span></span>](reinstall.md)  
[<span data-ttu-id="461f1-147">**ANUNCI**</span><span class="sxs-lookup"><span data-stu-id="461f1-147">**ADVERTISE**</span></span>](advertise.md)  
[<span data-ttu-id="461f1-148">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="461f1-148">**COMPADDLOCAL**</span></span>](compaddlocal.md)  
[<span data-ttu-id="461f1-149">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="461f1-149">**COMPADDSOURCE**</span></span>](compaddsource.md)  
[<span data-ttu-id="461f1-150">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="461f1-150">**COMPADDDEFAULT**</span></span>](compadddefault.md)  
[<span data-ttu-id="461f1-151">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="461f1-151">**FILEADDLOCAL**</span></span>](fileaddlocal.md)  
[<span data-ttu-id="461f1-152">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="461f1-152">**FILEADDSOURCE**</span></span>](fileaddsource.md)  
[<span data-ttu-id="461f1-153">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="461f1-153">**FILEADDDEFAULT**</span></span>](fileadddefault.md)  
</dl>

## <a name="validation"></a><span data-ttu-id="461f1-154">Validação</span><span class="sxs-lookup"><span data-stu-id="461f1-154">Validation</span></span>

<dl>

[<span data-ttu-id="461f1-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="461f1-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="461f1-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="461f1-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="461f1-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="461f1-157">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="461f1-158">ICE46</span><span class="sxs-lookup"><span data-stu-id="461f1-158">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="461f1-159">ICE79</span><span class="sxs-lookup"><span data-stu-id="461f1-159">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="461f1-160">ICE86</span><span class="sxs-lookup"><span data-stu-id="461f1-160">ICE86</span></span>](ice86.md)  
</dl>

 

 



