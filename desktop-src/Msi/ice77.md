---
description: ICE77 verifica se as ações personalizadas com o conjunto de bits msidbCustomActionTypeInScript são sequenciadas após a ação InstallInitialize e antes da ação InstallFinalize.
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090782"
---
# <a name="ice77"></a><span data-ttu-id="0d37a-103">ICE77</span><span class="sxs-lookup"><span data-stu-id="0d37a-103">ICE77</span></span>

<span data-ttu-id="0d37a-104">ICE77 verifica se as ações personalizadas com o conjunto de bits **msidbCustomActionTypeInScript** são sequenciadas após a [ação InstallInitialize](installinitialize-action.md) e antes da [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="0d37a-104">ICE77 verifies that custom actions with the **msidbCustomActionTypeInScript** bit set are sequenced after the [InstallInitialize action](installinitialize-action.md) and before the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="0d37a-105">ICE77 verifica a sequência na [tabela InstallExecuteSequence](installexecutesequence-table.md) e na [tabela AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="0d37a-105">ICE77 checks the sequence in the [InstallExecuteSequence table](installexecutesequence-table.md) and [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="0d37a-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="0d37a-106">Result</span></span>

<span data-ttu-id="0d37a-107">ICE77 posta um erro se uma ação personalizada em script for sequenciada antes da ação InstallInitialize ou após a ação InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="0d37a-107">ICE77 posts an error if an in-script custom action is sequenced before the InstallInitialize action or after the InstallFinalize action.</span></span>

<span data-ttu-id="0d37a-108">ICE77 lançará um erro se a ação InstallInitialize ou a ação InstallFinalize estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="0d37a-108">ICE77 posts an error if the InstallInitialize action or the InstallFinalize action is missing.</span></span>

## <a name="example"></a><span data-ttu-id="0d37a-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0d37a-109">Example</span></span>

<span data-ttu-id="0d37a-110">ICE77 relata os seguintes erros para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="0d37a-110">ICE77 reports the following errors for the example:</span></span>

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

<span data-ttu-id="0d37a-111">[Tabela CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="0d37a-111">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="0d37a-112">Ação</span><span class="sxs-lookup"><span data-stu-id="0d37a-112">Action</span></span>              | <span data-ttu-id="0d37a-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d37a-113">Type</span></span> |
|---------------------|------|
| <span data-ttu-id="0d37a-114">\_INSCRIPTINSTALL CA</span><span class="sxs-lookup"><span data-stu-id="0d37a-114">CA\_InScriptInstall</span></span> | <span data-ttu-id="0d37a-115">1025</span><span class="sxs-lookup"><span data-stu-id="0d37a-115">1025</span></span> |
| <span data-ttu-id="0d37a-116">\_INSCRIPTADMIN CA</span><span class="sxs-lookup"><span data-stu-id="0d37a-116">CA\_InScriptAdmin</span></span>   | <span data-ttu-id="0d37a-117">1026</span><span class="sxs-lookup"><span data-stu-id="0d37a-117">1026</span></span> |



 

<span data-ttu-id="0d37a-118">[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="0d37a-118">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="0d37a-119">Ação</span><span class="sxs-lookup"><span data-stu-id="0d37a-119">Action</span></span>              | <span data-ttu-id="0d37a-120">Sequência</span><span class="sxs-lookup"><span data-stu-id="0d37a-120">Sequence</span></span> |
|---------------------|----------|
| <span data-ttu-id="0d37a-121">\_INSCRIPTINSTALL CA</span><span class="sxs-lookup"><span data-stu-id="0d37a-121">CA\_InScriptInstall</span></span> | <span data-ttu-id="0d37a-122">2000</span><span class="sxs-lookup"><span data-stu-id="0d37a-122">2000</span></span>     |
| <span data-ttu-id="0d37a-123">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="0d37a-123">InstallInitialize</span></span>   | <span data-ttu-id="0d37a-124">1500</span><span class="sxs-lookup"><span data-stu-id="0d37a-124">1500</span></span>     |



 

<span data-ttu-id="0d37a-125">[Tabela AdminExecuteSequence](adminexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="0d37a-125">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="0d37a-126">Ação</span><span class="sxs-lookup"><span data-stu-id="0d37a-126">Action</span></span>            | <span data-ttu-id="0d37a-127">Sequência</span><span class="sxs-lookup"><span data-stu-id="0d37a-127">Sequence</span></span> |
|-------------------|----------|
| <span data-ttu-id="0d37a-128">\_INSCRIPTADMIN CA</span><span class="sxs-lookup"><span data-stu-id="0d37a-128">CA\_InScriptAdmin</span></span> | <span data-ttu-id="0d37a-129">1.400</span><span class="sxs-lookup"><span data-stu-id="0d37a-129">1400</span></span>     |
| <span data-ttu-id="0d37a-130">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="0d37a-130">InstallInitialize</span></span> | <span data-ttu-id="0d37a-131">1500</span><span class="sxs-lookup"><span data-stu-id="0d37a-131">1500</span></span>     |
| <span data-ttu-id="0d37a-132">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="0d37a-132">InstallFinalize</span></span>   | <span data-ttu-id="0d37a-133">6600</span><span class="sxs-lookup"><span data-stu-id="0d37a-133">6600</span></span>     |



 

<span data-ttu-id="0d37a-134">Para corrigir os erros, sequenciar as ações personalizadas em script após a ação InstallInitialize e antes da ação InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="0d37a-134">To fix the errors, sequence the in-script custom actions after the InstallInitialize action and before the InstallFinalize action.</span></span> <span data-ttu-id="0d37a-135">As ações InstallInitialize e InstallFinalize devem estar presentes na tabela InstallExecuteSequence e na tabela AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="0d37a-135">The InstallInitialize and InstallFinalize actions must be present in the InstallExecuteSequence table and the AdminExecuteSequence table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d37a-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d37a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d37a-137">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="0d37a-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



