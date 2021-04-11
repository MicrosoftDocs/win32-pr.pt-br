---
description: O ICE75 verifica se todo o tipo de ação personalizada 17 (DLL), tipo de ação personalizada 18 (EXE), tipo de ação personalizada 21 (JScript) e ações personalizadas de tipo de ação personalizada 22 (VBScript) são sequenciadas após a ação CostFinalize.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297120"
---
# <a name="ice75"></a><span data-ttu-id="e92e6-103">ICE75</span><span class="sxs-lookup"><span data-stu-id="e92e6-103">ICE75</span></span>

<span data-ttu-id="e92e6-104">O ICE75 verifica se todo o [tipo de ação personalizada 17](custom-action-type-17.md) (DLL), [tipo de ação personalizada 18](custom-action-type-18.md) (exe), [tipo de ação personalizada 21](custom-action-type-21.md) (JScript) e ações personalizadas de [tipo de ação personalizada 22](custom-action-type-22.md) (VBScript) são sequenciadas após a [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e92e6-104">ICE75 verifies that all [Custom Action Type 17](custom-action-type-17.md) (DLL), [Custom Action Type 18](custom-action-type-18.md) (EXE), [Custom Action type 21](custom-action-type-21.md) (JScript), and [Custom Action Type 22](custom-action-type-22.md) (VBScript) custom actions are sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="e92e6-105">Esses tipos de ação personalizada usam um arquivo instalado como sua origem.</span><span class="sxs-lookup"><span data-stu-id="e92e6-105">These types of custom action use an installed file as their source.</span></span> <span data-ttu-id="e92e6-106">ICE75 verifica a tabela [InstallUISequence](installuisequence-table.md), a [tabela InstallExecuteSequence](installexecutesequence-table.md), a tabela [AdminUISequence](adminuisequence-table.md)e a [tabela AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="e92e6-106">ICE75 checks the [InstallUISequence Table](installuisequence-table.md), [InstallExecuteSequence Table](installexecutesequence-table.md), [AdminUISequence Table](adminuisequence-table.md), and [AdminExecuteSequence Table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="e92e6-107">Observe que a ação CostFinalize é necessária nessas tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="e92e6-107">Note that the CostFinalize action is required in these sequence tables.</span></span>

## <a name="result"></a><span data-ttu-id="e92e6-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="e92e6-108">Result</span></span>

<span data-ttu-id="e92e6-109">ICE75 posta um erro se encontrar uma ação personalizada usando um arquivo instalado como um arquivo de origem que não é sequenciado após a ação CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="e92e6-109">ICE75 posts an error if it finds a custom action using an installed file as a source file that is not sequenced after the CostFinalize action.</span></span>

## <a name="example"></a><span data-ttu-id="e92e6-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e92e6-110">Example</span></span>

<span data-ttu-id="e92e6-111">ICE75 relata os seguintes erros para o exemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="e92e6-111">ICE75 reports the following errors for the example shown:</span></span>

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

<span data-ttu-id="e92e6-112">[Tabela CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e92e6-112">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="e92e6-113">Ação</span><span class="sxs-lookup"><span data-stu-id="e92e6-113">Action</span></span>      | <span data-ttu-id="e92e6-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="e92e6-114">Type</span></span> | <span data-ttu-id="e92e6-115">Fonte</span><span class="sxs-lookup"><span data-stu-id="e92e6-115">Source</span></span>  |
|-------------|------|---------|
| <span data-ttu-id="e92e6-116">\_FILEEXE CA</span><span class="sxs-lookup"><span data-stu-id="e92e6-116">CA\_FileExe</span></span> | <span data-ttu-id="e92e6-117">18</span><span class="sxs-lookup"><span data-stu-id="e92e6-117">18</span></span>   | <span data-ttu-id="e92e6-118">FileExe</span><span class="sxs-lookup"><span data-stu-id="e92e6-118">FileExe</span></span> |
| <span data-ttu-id="e92e6-119">\_FILEDLL CA</span><span class="sxs-lookup"><span data-stu-id="e92e6-119">CA\_FileDLL</span></span> | <span data-ttu-id="e92e6-120">17</span><span class="sxs-lookup"><span data-stu-id="e92e6-120">17</span></span>   | <span data-ttu-id="e92e6-121">FileDLL</span><span class="sxs-lookup"><span data-stu-id="e92e6-121">FileDLL</span></span> |



 

<span data-ttu-id="e92e6-122">[Tabela AdminUISequence](adminuisequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e92e6-122">[AdminUISequence Table](adminuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="e92e6-123">Ação</span><span class="sxs-lookup"><span data-stu-id="e92e6-123">Action</span></span>      | <span data-ttu-id="e92e6-124">Sequência</span><span class="sxs-lookup"><span data-stu-id="e92e6-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="e92e6-125">\_FILEEXE CA</span><span class="sxs-lookup"><span data-stu-id="e92e6-125">CA\_FileExe</span></span> | <span data-ttu-id="e92e6-126">1100</span><span class="sxs-lookup"><span data-stu-id="e92e6-126">1100</span></span>     |



 

<span data-ttu-id="e92e6-127">[Tabela AdminExecuteSequence](adminexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e92e6-127">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="e92e6-128">Ação</span><span class="sxs-lookup"><span data-stu-id="e92e6-128">Action</span></span>       | <span data-ttu-id="e92e6-129">Sequência</span><span class="sxs-lookup"><span data-stu-id="e92e6-129">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="e92e6-130">\_FILEDLL CA</span><span class="sxs-lookup"><span data-stu-id="e92e6-130">CA\_FileDLL</span></span>  | <span data-ttu-id="e92e6-131">800</span><span class="sxs-lookup"><span data-stu-id="e92e6-131">800</span></span>      |
| <span data-ttu-id="e92e6-132">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="e92e6-132">CostFinalize</span></span> | <span data-ttu-id="e92e6-133">1000</span><span class="sxs-lookup"><span data-stu-id="e92e6-133">1000</span></span>     |



 

<span data-ttu-id="e92e6-134">Para corrigir os erros, sequenciar as ações personalizadas após a ação CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="e92e6-134">To fix the errors, sequence the custom actions after the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e92e6-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e92e6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e92e6-136">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="e92e6-136">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



