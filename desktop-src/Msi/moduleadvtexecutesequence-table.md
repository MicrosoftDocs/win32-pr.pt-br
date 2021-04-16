---
description: Uma ferramenta de mesclagem avalia a tabela ModuleAdvtExecuteSequence e, em seguida, insere as ações calculadas na tabela AdvtExecuteSequence com um número de sequência correto.
ms.assetid: ed2d1159-da78-4dc5-98a2-2cc876380c43
title: Tabela ModuleAdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699e544df7e0a92b0fee92c753e36a8b9a86ee5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750231"
---
# <a name="moduleadvtexecutesequence-table"></a><span data-ttu-id="b0f45-103">Tabela ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="b0f45-103">ModuleAdvtExecuteSequence Table</span></span>

<span data-ttu-id="b0f45-104">Uma ferramenta de mesclagem avalia a tabela ModuleAdvtExecuteSequence e, em seguida, insere as ações calculadas na [tabela AdvtExecuteSequence](advtexecutesequence-table.md) com um número de sequência correto.</span><span class="sxs-lookup"><span data-stu-id="b0f45-104">A merge tool evaluates the ModuleAdvtExecuteSequence table and then inserts the calculated actions into the [AdvtExecuteSequence table](advtexecutesequence-table.md) with a correct sequence number.</span></span>

<span data-ttu-id="b0f45-105">A tabela ModuleAdvtExecuteSequence tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="b0f45-105">The ModuleAdvtExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="b0f45-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="b0f45-106">Column</span></span>     | <span data-ttu-id="b0f45-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0f45-107">Type</span></span>                         | <span data-ttu-id="b0f45-108">Chave</span><span class="sxs-lookup"><span data-stu-id="b0f45-108">Key</span></span> | <span data-ttu-id="b0f45-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="b0f45-109">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="b0f45-110">Ação</span><span class="sxs-lookup"><span data-stu-id="b0f45-110">Action</span></span>     | [<span data-ttu-id="b0f45-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="b0f45-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="b0f45-112">S</span><span class="sxs-lookup"><span data-stu-id="b0f45-112">Y</span></span>   | <span data-ttu-id="b0f45-113">N</span><span class="sxs-lookup"><span data-stu-id="b0f45-113">N</span></span>        |
| <span data-ttu-id="b0f45-114">Sequência</span><span class="sxs-lookup"><span data-stu-id="b0f45-114">Sequence</span></span>   | [<span data-ttu-id="b0f45-115">Inteiro</span><span class="sxs-lookup"><span data-stu-id="b0f45-115">Integer</span></span>](integer.md)       |     | <span data-ttu-id="b0f45-116">S</span><span class="sxs-lookup"><span data-stu-id="b0f45-116">Y</span></span>        |
| <span data-ttu-id="b0f45-117">Baseaction</span><span class="sxs-lookup"><span data-stu-id="b0f45-117">BaseAction</span></span> | [<span data-ttu-id="b0f45-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="b0f45-118">Identifier</span></span>](identifier.md) |     | <span data-ttu-id="b0f45-119">S</span><span class="sxs-lookup"><span data-stu-id="b0f45-119">Y</span></span>        |
| <span data-ttu-id="b0f45-120">After (após)</span><span class="sxs-lookup"><span data-stu-id="b0f45-120">After</span></span>      | [<span data-ttu-id="b0f45-121">Inteiro</span><span class="sxs-lookup"><span data-stu-id="b0f45-121">Integer</span></span>](integer.md)       |     | <span data-ttu-id="b0f45-122">S</span><span class="sxs-lookup"><span data-stu-id="b0f45-122">Y</span></span>        |
| <span data-ttu-id="b0f45-123">Condição</span><span class="sxs-lookup"><span data-stu-id="b0f45-123">Condition</span></span>  | [<span data-ttu-id="b0f45-124">Condição</span><span class="sxs-lookup"><span data-stu-id="b0f45-124">Condition</span></span>](condition.md)   |     | <span data-ttu-id="b0f45-125">S</span><span class="sxs-lookup"><span data-stu-id="b0f45-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b0f45-126">Colunas</span><span class="sxs-lookup"><span data-stu-id="b0f45-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b0f45-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="b0f45-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="b0f45-128">Ação a ser inserida em sequência.</span><span class="sxs-lookup"><span data-stu-id="b0f45-128">Action to insert into sequence.</span></span> <span data-ttu-id="b0f45-129">Refere-se a uma das [ações padrão](standard-actions.md)do instalador ou a uma entrada na tabela [CustomAction](customaction-table.md) ou na [tabela de diálogo](dialog-table.md)do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="b0f45-129">Refers to one of the installer [standard actions](standard-actions.md), or an entry in the merge module's [CustomAction table](customaction-table.md) or [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="b0f45-130">Se uma [ação padrão](standard-actions.md) for usada na coluna ação de uma tabela de sequência de módulo de mesclagem, as colunas baseaction e After desse registro deverão ser nulas.</span><span class="sxs-lookup"><span data-stu-id="b0f45-130">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be Null.</span></span>

</dd> <dt>

<span data-ttu-id="b0f45-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem</span><span class="sxs-lookup"><span data-stu-id="b0f45-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="b0f45-132">O número de sequência de uma ação padrão.</span><span class="sxs-lookup"><span data-stu-id="b0f45-132">The sequence number of a standard action.</span></span> <span data-ttu-id="b0f45-133">Se uma ação ou caixa de diálogo personalizada for inserida na coluna ação dessa linha, esse campo deverá ser definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="b0f45-133">If a custom action or dialog is entered into the Action column of this row, this field must be set to Null.</span></span>

<span data-ttu-id="b0f45-134">Ao usar [ações padrão](standard-actions.md) em tabelas de sequências do módulo de mesclagem, o valor na coluna sequência deve ser o número de sequência de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="b0f45-134">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number.</span></span> <span data-ttu-id="b0f45-135">Se o número de sequência no módulo de mesclagem for diferente daquele para a mesma ação na tabela de sequência de arquivos. msi, a ferramenta de mesclagem usará o número de sequência do arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="b0f45-135">If the sequence number in the merge module differs from that for the same action in the .msi file sequence table, the merge tool uses the sequence number from the .msi file.</span></span> <span data-ttu-id="b0f45-136">Consulte as sequências sugeridas em [usando uma tabela de sequência](using-a-sequence-table.md) para os números de sequência recomendados de ações padrão.</span><span class="sxs-lookup"><span data-stu-id="b0f45-136">See the suggested sequences in [Using a Sequence Table](using-a-sequence-table.md) for the recommended sequence numbers of standard actions.</span></span>

</dd> <dt>

<span data-ttu-id="b0f45-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>Baseaction</span><span class="sxs-lookup"><span data-stu-id="b0f45-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span></span>
</dt> <dd>

<span data-ttu-id="b0f45-138">A coluna Baseaction pode conter uma ação padrão, uma ação personalizada especificada na tabela de ação personalizada do módulo de mesclagem ou uma caixa de diálogo especificada na tabela de diálogo do módulo.</span><span class="sxs-lookup"><span data-stu-id="b0f45-138">The BaseAction column can contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="b0f45-139">A coluna Baseaction é uma chave na coluna ação desta tabela.</span><span class="sxs-lookup"><span data-stu-id="b0f45-139">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="b0f45-140">Ele não pode ser uma chave estrangeira em outra tabela ou tabela de mesclagem no arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="b0f45-140">It cannot be a foreign key into another merge table or table in the .msi file.</span></span> <span data-ttu-id="b0f45-141">Isso significa que cada ação padrão, ação personalizada ou caixa de diálogo listada na coluna Baseaction também deve ser listada na coluna ação de outro registro nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="b0f45-141">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

</dd> <dt>

<span data-ttu-id="b0f45-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>Após</span><span class="sxs-lookup"><span data-stu-id="b0f45-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>After</span></span>
</dt> <dd>

<span data-ttu-id="b0f45-143">Booliano para se a ação vier antes ou depois de Baseaction.</span><span class="sxs-lookup"><span data-stu-id="b0f45-143">Boolean for whether Action comes before or after BaseAction.</span></span>



| <span data-ttu-id="b0f45-144">Valor</span><span class="sxs-lookup"><span data-stu-id="b0f45-144">Value</span></span> | <span data-ttu-id="b0f45-145">Significado</span><span class="sxs-lookup"><span data-stu-id="b0f45-145">Meaning</span></span>                          |
|-------|----------------------------------|
| <span data-ttu-id="b0f45-146">0</span><span class="sxs-lookup"><span data-stu-id="b0f45-146">0</span></span>     | <span data-ttu-id="b0f45-147">Ação a ser executada antes de Baseaction</span><span class="sxs-lookup"><span data-stu-id="b0f45-147">Action to come before BaseAction</span></span> |
| <span data-ttu-id="b0f45-148">1</span><span class="sxs-lookup"><span data-stu-id="b0f45-148">1</span></span>     | <span data-ttu-id="b0f45-149">Ação a ser executada após Baseaction</span><span class="sxs-lookup"><span data-stu-id="b0f45-149">Action to come after BaseAction</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b0f45-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="b0f45-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="b0f45-151">Uma instrução condicional que indica se a ação é executada.</span><span class="sxs-lookup"><span data-stu-id="b0f45-151">A conditional statement that indicates if the action is be executed.</span></span> <span data-ttu-id="b0f45-152">NULL é avaliado como true.</span><span class="sxs-lookup"><span data-stu-id="b0f45-152">Null evaluates to true.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0f45-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0f45-153">Remarks</span></span>

<span data-ttu-id="b0f45-154">Se essa tabela estiver presente, a [tabela AdvtExecuteSequence](advtexecutesequence-table.md) também deverá estar presente no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="b0f45-154">If this table is present the [AdvtExecuteSequence table](advtexecutesequence-table.md) must also be present in the merge module.</span></span>

 

 



