---
description: ICE12 valida as tabelas CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence e InstallUISequence do banco de dados Windows Installer.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769319"
---
# <a name="ice12"></a><span data-ttu-id="519e1-103">ICE12</span><span class="sxs-lookup"><span data-stu-id="519e1-103">ICE12</span></span>

<span data-ttu-id="519e1-104">ICE12 consulta as tabelas [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e [InstallUISequence](installuisequence-table.md) para validar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="519e1-104">ICE12 queries the [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [InstallUISequence](installuisequence-table.md) tables to validate the following:</span></span>

-   <span data-ttu-id="519e1-105">A [ação CostFinalize](costfinalize-action.md) ocorre em qualquer tabela de sequência que contenha ações do tipo tipo de [ação personalizada 35](custom-action-type-35.md) ou [tipo de ação personalizada 51](custom-action-type-51.md).</span><span class="sxs-lookup"><span data-stu-id="519e1-105">That the [CostFinalize action](costfinalize-action.md) occurs in any sequence table containing actions of the type [Custom Action Type 35](custom-action-type-35.md) or [Custom Action Type 51](custom-action-type-51.md).</span></span>
-   <span data-ttu-id="519e1-106">Cada [tipo de ação personalizada 35](custom-action-type-35.md) vem após a [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="519e1-106">That every [Custom Action Type 35](custom-action-type-35.md) comes after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="519e1-107">nas tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="519e1-107">in the sequence tables.</span></span>
-   <span data-ttu-id="519e1-108">Cada [ação personalizada tipo 51](custom-action-type-51.md) que tem uma chave estrangeira para a tabela de diretório na coluna de origem da tabela CustomAction vem antes da [ação CostFinalize](costfinalize-action.md) nas tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="519e1-108">That every [Custom Action Type 51](custom-action-type-51.md) that has a foreign key to the Directory table in the Source column of the CustomAction table comes before the [CostFinalize action](costfinalize-action.md) in the sequence tables.</span></span>

<span data-ttu-id="519e1-109">Observe que o ICE12 não valida o texto formatado na coluna de destino da tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="519e1-109">Note that ICE12 does not validate the formatted text in the Target column of the CustomAction table.</span></span>

## <a name="result"></a><span data-ttu-id="519e1-110">Resultado</span><span class="sxs-lookup"><span data-stu-id="519e1-110">Result</span></span>

<span data-ttu-id="519e1-111">ICE12 posta uma mensagem de erro se a validação das ações personalizadas que definem uma propriedade de diretório falhar.</span><span class="sxs-lookup"><span data-stu-id="519e1-111">ICE12 posts an error message if validation of the custom actions that set a directory property fails.</span></span>

## <a name="example"></a><span data-ttu-id="519e1-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="519e1-112">Example</span></span>

<span data-ttu-id="519e1-113">ICE12 iria postar três erros para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="519e1-113">ICE12 would post three errors for the example shown.</span></span>

-   <span data-ttu-id="519e1-114">Para CA1, pasta ' MyFolder ' não encontrada na tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="519e1-114">For CA1, Folder 'MyFolder' not found in Directory table</span></span>
-   <span data-ttu-id="519e1-115">Para CA2, a sequência ' 80 ' vem antes de CostFinalize na tabela InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="519e1-115">For CA2, Sequence '80' comes before CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="519e1-116">Ele deve vir após ( CF@100 )</span><span class="sxs-lookup"><span data-stu-id="519e1-116">It must come after (CF@100)</span></span>
-   <span data-ttu-id="519e1-117">Para CA3, a sequência ' 125 ' vem após CostFinalize na tabela InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="519e1-117">For CA3, Sequence '125' comes after CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="519e1-118">Ele deve vir antes de ( CF@100 )</span><span class="sxs-lookup"><span data-stu-id="519e1-118">It must come before (CF@100)</span></span>

<span data-ttu-id="519e1-119">[Tabela CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="519e1-119">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="519e1-120">Ação</span><span class="sxs-lookup"><span data-stu-id="519e1-120">Action</span></span> | <span data-ttu-id="519e1-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="519e1-121">Type</span></span> | <span data-ttu-id="519e1-122">Fonte</span><span class="sxs-lookup"><span data-stu-id="519e1-122">Source</span></span>        |
|--------|------|---------------|
| <span data-ttu-id="519e1-123">CA1</span><span class="sxs-lookup"><span data-stu-id="519e1-123">CA1</span></span>    | <span data-ttu-id="519e1-124">35</span><span class="sxs-lookup"><span data-stu-id="519e1-124">35</span></span>   | <span data-ttu-id="519e1-125">MyFolder</span><span class="sxs-lookup"><span data-stu-id="519e1-125">MyFolder</span></span>      |
| <span data-ttu-id="519e1-126">CA2</span><span class="sxs-lookup"><span data-stu-id="519e1-126">CA2</span></span>    | <span data-ttu-id="519e1-127">35</span><span class="sxs-lookup"><span data-stu-id="519e1-127">35</span></span>   | <span data-ttu-id="519e1-128">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="519e1-128">WindowsFolder</span></span> |
| <span data-ttu-id="519e1-129">CA3</span><span class="sxs-lookup"><span data-stu-id="519e1-129">CA3</span></span>    | <span data-ttu-id="519e1-130">51</span><span class="sxs-lookup"><span data-stu-id="519e1-130">51</span></span>   | <span data-ttu-id="519e1-131">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="519e1-131">WindowsFolder</span></span> |



 

[<span data-ttu-id="519e1-132">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="519e1-132">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="519e1-133">Diretório</span><span class="sxs-lookup"><span data-stu-id="519e1-133">Directory</span></span>     | <span data-ttu-id="519e1-134">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="519e1-134">Directory\_Parent</span></span> | <span data-ttu-id="519e1-135">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="519e1-135">DefaultDir</span></span>    |
|---------------|-------------------|---------------|
| <span data-ttu-id="519e1-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="519e1-136">TARGETDIR</span></span>     |                   | <span data-ttu-id="519e1-137">SourceDir</span><span class="sxs-lookup"><span data-stu-id="519e1-137">SourceDir</span></span>     |
| <span data-ttu-id="519e1-138">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="519e1-138">WindowsFolder</span></span> | <span data-ttu-id="519e1-139">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="519e1-139">TARGETDIR</span></span>         | <span data-ttu-id="519e1-140">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="519e1-140">WindowsFolder</span></span> |



 

<span data-ttu-id="519e1-141">[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="519e1-141">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="519e1-142">Ação</span><span class="sxs-lookup"><span data-stu-id="519e1-142">Action</span></span>       | <span data-ttu-id="519e1-143">Sequência</span><span class="sxs-lookup"><span data-stu-id="519e1-143">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="519e1-144">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="519e1-144">CostFinalize</span></span> | <span data-ttu-id="519e1-145">100</span><span class="sxs-lookup"><span data-stu-id="519e1-145">100</span></span>      |
| <span data-ttu-id="519e1-146">CA2</span><span class="sxs-lookup"><span data-stu-id="519e1-146">CA2</span></span>          | <span data-ttu-id="519e1-147">80</span><span class="sxs-lookup"><span data-stu-id="519e1-147">80</span></span>       |
| <span data-ttu-id="519e1-148">CA3</span><span class="sxs-lookup"><span data-stu-id="519e1-148">CA3</span></span>          | <span data-ttu-id="519e1-149">125</span><span class="sxs-lookup"><span data-stu-id="519e1-149">125</span></span>      |



 

<span data-ttu-id="519e1-150">Para corrigir o erro de CA1, altere sua entrada em sua coluna de origem na tabela CustomAction para uma entrada existente na tabela de diretório ou adicione MyFolder à tabela de diretórios.</span><span class="sxs-lookup"><span data-stu-id="519e1-150">To fix the error for CA1 change its entry in its Source column in the CustomAction table to an existing entry in the Directory table or add MyFolder to the Directory table.</span></span>

<span data-ttu-id="519e1-151">Para corrigir o erro para CA2, altere sua sequência na tabela InstallExecuteSequence de modo que ela venha após a ação CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="519e1-151">To fix the error for CA2, change its sequence in the InstallExecuteSequence table such that it comes after the CostFinalize action.</span></span>

<span data-ttu-id="519e1-152">Para corrigir o erro para CA3, altere sua sequência na tabela InstallExecuteSequence de tal forma que ela venha antes da ação CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="519e1-152">To fix the error for CA3, change its sequence in the InstallExecuteSequence table such that it comes before the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="519e1-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="519e1-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="519e1-154">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="519e1-154">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



