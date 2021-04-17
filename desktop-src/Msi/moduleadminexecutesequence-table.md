---
description: Uma ferramenta de mesclagem avalia a tabela ModuleAdminExecuteSequence e, em seguida, insere as ações calculadas na tabela AdminExecuteSequence com um número de sequência correto.
ms.assetid: 26cc5e15-8dfd-4bf5-8830-225164302278
title: Tabela ModuleAdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0f062f552f92ec667a2889d2bf26a98900e152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766391"
---
# <a name="moduleadminexecutesequence-table"></a><span data-ttu-id="4c5d5-103">Tabela ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="4c5d5-103">ModuleAdminExecuteSequence Table</span></span>

<span data-ttu-id="4c5d5-104">Uma ferramenta de mesclagem avalia a tabela ModuleAdminExecuteSequence e, em seguida, insere as ações calculadas na [tabela AdminExecuteSequence](adminexecutesequence-table.md) com um número de sequência correto.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-104">A merge tool evaluates the ModuleAdminExecuteSequence table and then inserts the calculated actions into the [AdminExecuteSequence table](adminexecutesequence-table.md) with a correct sequence number.</span></span>

<span data-ttu-id="4c5d5-105">A tabela ModuleAdminExecuteSequence tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-105">The ModuleAdminExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="4c5d5-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="4c5d5-106">Column</span></span>     | <span data-ttu-id="4c5d5-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c5d5-107">Type</span></span>                         | <span data-ttu-id="4c5d5-108">Chave</span><span class="sxs-lookup"><span data-stu-id="4c5d5-108">Key</span></span> | <span data-ttu-id="4c5d5-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="4c5d5-109">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="4c5d5-110">Ação</span><span class="sxs-lookup"><span data-stu-id="4c5d5-110">Action</span></span>     | [<span data-ttu-id="4c5d5-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="4c5d5-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="4c5d5-112">S</span><span class="sxs-lookup"><span data-stu-id="4c5d5-112">Y</span></span>   | <span data-ttu-id="4c5d5-113">N</span><span class="sxs-lookup"><span data-stu-id="4c5d5-113">N</span></span>        |
| <span data-ttu-id="4c5d5-114">Sequência</span><span class="sxs-lookup"><span data-stu-id="4c5d5-114">Sequence</span></span>   | [<span data-ttu-id="4c5d5-115">Inteiro</span><span class="sxs-lookup"><span data-stu-id="4c5d5-115">Integer</span></span>](integer.md)       |     | <span data-ttu-id="4c5d5-116">S</span><span class="sxs-lookup"><span data-stu-id="4c5d5-116">Y</span></span>        |
| <span data-ttu-id="4c5d5-117">Baseaction</span><span class="sxs-lookup"><span data-stu-id="4c5d5-117">BaseAction</span></span> | [<span data-ttu-id="4c5d5-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="4c5d5-118">Identifier</span></span>](identifier.md) |     | <span data-ttu-id="4c5d5-119">S</span><span class="sxs-lookup"><span data-stu-id="4c5d5-119">Y</span></span>        |
| <span data-ttu-id="4c5d5-120">After (após)</span><span class="sxs-lookup"><span data-stu-id="4c5d5-120">After</span></span>      | [<span data-ttu-id="4c5d5-121">Inteiro</span><span class="sxs-lookup"><span data-stu-id="4c5d5-121">Integer</span></span>](integer.md)       |     | <span data-ttu-id="4c5d5-122">S</span><span class="sxs-lookup"><span data-stu-id="4c5d5-122">Y</span></span>        |
| <span data-ttu-id="4c5d5-123">Condição</span><span class="sxs-lookup"><span data-stu-id="4c5d5-123">Condition</span></span>  | [<span data-ttu-id="4c5d5-124">Condição</span><span class="sxs-lookup"><span data-stu-id="4c5d5-124">Condition</span></span>](condition.md)   |     | <span data-ttu-id="4c5d5-125">S</span><span class="sxs-lookup"><span data-stu-id="4c5d5-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="4c5d5-126">Colunas</span><span class="sxs-lookup"><span data-stu-id="4c5d5-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="4c5d5-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="4c5d5-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="4c5d5-128">Ação a ser inserida em sequência.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-128">Action to insert into sequence.</span></span> <span data-ttu-id="4c5d5-129">Refere-se a uma das [ações padrão](standard-actions.md)do instalador ou a uma entrada na tabela [CustomAction](customaction-table.md) ou na [tabela de diálogo](dialog-table.md)do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-129">Refers to one of the installer [standard actions](standard-actions.md), or an entry in the merge module's [CustomAction table](customaction-table.md) or [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="4c5d5-130">Se uma [ação padrão](standard-actions.md) for usada na coluna ação de uma tabela de sequência de módulo de mesclagem, as colunas baseaction e After desse registro deverão ser nulas.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-130">If a [standard action](standard-actions.md) is used in the Action column of a merge module sequence table, the BaseAction and After columns of that record must be Null.</span></span>

</dd> <dt>

<span data-ttu-id="4c5d5-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem</span><span class="sxs-lookup"><span data-stu-id="4c5d5-131"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="4c5d5-132">O número de sequência de uma ação padrão.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-132">The sequence number of a standard action.</span></span> <span data-ttu-id="4c5d5-133">Se uma ação ou caixa de diálogo personalizada for inserida na coluna ação dessa linha, esse campo deverá ser definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-133">If a custom action or dialog is entered into the Action column of this row, this field must be set to Null.</span></span>

<span data-ttu-id="4c5d5-134">Ao usar [ações padrão](standard-actions.md) em tabelas de sequências do módulo de mesclagem, o valor na coluna sequência deve ser o número de sequência de ação recomendado.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-134">When using [standard actions](standard-actions.md) in merge module sequence tables, the value in the Sequence column should be the recommended action sequence number.</span></span> <span data-ttu-id="4c5d5-135">Se o número de sequência no módulo de mesclagem for diferente daquele para a mesma ação na tabela de sequência de arquivos. msi, a ferramenta de mesclagem usará o número de sequência do arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-135">If the sequence number in the merge module differs from that for the same action in the .msi file sequence table, the merge tool uses the sequence number from the .msi file.</span></span> <span data-ttu-id="4c5d5-136">Consulte as sequências sugeridas em [usando uma tabela de sequência](using-a-sequence-table.md) para os números de sequência recomendados de ações padrão.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-136">See the suggested sequences in [Using a Sequence Table](using-a-sequence-table.md) for the recommended sequence numbers of standard actions.</span></span>

</dd> <dt>

<span data-ttu-id="4c5d5-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>Baseaction</span><span class="sxs-lookup"><span data-stu-id="4c5d5-137"><span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction</span></span>
</dt> <dd>

<span data-ttu-id="4c5d5-138">A coluna Baseaction pode conter uma ação padrão, uma ação personalizada especificada na tabela de ação personalizada do módulo de mesclagem ou uma caixa de diálogo especificada na tabela de diálogo do módulo.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-138">The BaseAction column can contain a standard action, a custom action specified in the merge module's custom action table, or a dialog specified in the module's dialog table.</span></span> <span data-ttu-id="4c5d5-139">A coluna Baseaction é uma chave na coluna ação desta tabela.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-139">The BaseAction column is a key into the Action column of this table.</span></span> <span data-ttu-id="4c5d5-140">Ele não pode ser uma chave estrangeira em outra tabela ou tabela de mesclagem no arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-140">It cannot be a foreign key into another merge table or table in the .msi file.</span></span> <span data-ttu-id="4c5d5-141">Isso significa que cada ação padrão, ação personalizada ou caixa de diálogo listada na coluna Baseaction também deve ser listada na coluna ação de outro registro nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-141">This means that every standard action, custom action, or dialog listed in the BaseAction column must also be listed in the Action column of another record in this table.</span></span>

</dd> <dt>

<span data-ttu-id="4c5d5-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>Após</span><span class="sxs-lookup"><span data-stu-id="4c5d5-142"><span id="After"></span><span id="after"></span><span id="AFTER"></span>After</span></span>
</dt> <dd>

<span data-ttu-id="4c5d5-143">Booliano para se a ação vier antes ou depois de Baseaction.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-143">Boolean for whether Action comes before or after BaseAction.</span></span>



| <span data-ttu-id="4c5d5-144">Valor</span><span class="sxs-lookup"><span data-stu-id="4c5d5-144">Value</span></span> | <span data-ttu-id="4c5d5-145">Significado</span><span class="sxs-lookup"><span data-stu-id="4c5d5-145">Meaning</span></span>                          |
|-------|----------------------------------|
| <span data-ttu-id="4c5d5-146">0</span><span class="sxs-lookup"><span data-stu-id="4c5d5-146">0</span></span>     | <span data-ttu-id="4c5d5-147">Ação a ser executada antes de Baseaction</span><span class="sxs-lookup"><span data-stu-id="4c5d5-147">Action to come before BaseAction</span></span> |
| <span data-ttu-id="4c5d5-148">1</span><span class="sxs-lookup"><span data-stu-id="4c5d5-148">1</span></span>     | <span data-ttu-id="4c5d5-149">Ação a ser executada após Baseaction</span><span class="sxs-lookup"><span data-stu-id="4c5d5-149">Action to come after BaseAction</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4c5d5-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="4c5d5-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="4c5d5-151">Uma instrução condicional que indica se a ação é executada.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-151">A conditional statement that indicates if the action is be executed.</span></span> <span data-ttu-id="4c5d5-152">NULL é avaliado como true.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-152">Null evaluates to true.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c5d5-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c5d5-153">Remarks</span></span>

<span data-ttu-id="4c5d5-154">Se essa tabela estiver presente, a [tabela AdminExecuteSequence](adminexecutesequence-table.md) também deverá estar presente no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="4c5d5-154">If this table is present the [AdminExecuteSequence table](adminexecutesequence-table.md) must also be present in the merge module.</span></span>

 

 



