---
description: ICE72 verifica se as ações personalizadas não internas não são usadas na tabela AdvtExecuteSequence.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753445"
---
# <a name="ice72"></a><span data-ttu-id="635ba-103">ICE72</span><span class="sxs-lookup"><span data-stu-id="635ba-103">ICE72</span></span>

<span data-ttu-id="635ba-104">ICE72 verifica se as ações personalizadas não internas não são usadas na [tabela AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="635ba-104">ICE72 verifies that non-built-in custom actions are not used in the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span> <span data-ttu-id="635ba-105">Especificamente, apenas o tipo 19, o tipo 35, e as ações personalizadas de tipo 51 são permitidas na tabela AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="635ba-105">Specifically, only type 19, type 35, and type 51 custom actions are allowed in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="635ba-106">Se outras ações personalizadas forem usadas, o anúncio poderá não se comportar conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="635ba-106">If other custom actions are used, advertisement may not behave as expected.</span></span>

## <a name="result"></a><span data-ttu-id="635ba-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="635ba-107">Result</span></span>

<span data-ttu-id="635ba-108">ICE72 retornará um erro se a tabela AdvExecuteSequence usar ações personalizadas que não sejam do tipo 35, digite 51 e digite 19.</span><span class="sxs-lookup"><span data-stu-id="635ba-108">ICE72 returns an error if the AdvExecuteSequence table uses custom actions other than type 35, type 51, and type 19.</span></span>

## <a name="example"></a><span data-ttu-id="635ba-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="635ba-109">Example</span></span>

<span data-ttu-id="635ba-110">ICE72 relata o seguinte erro para o exemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="635ba-110">ICE72 reports the following error for the example shown:</span></span>

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

<span data-ttu-id="635ba-111">Para corrigir o erro, remova ' CA1 ' da tabela AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="635ba-111">To fix the error, remove 'CA1' from the AdvtExecuteSequence table.</span></span>

<span data-ttu-id="635ba-112">[Tabela AdvtExecuteSequence](advtexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="635ba-112">[AdvtExecuteSequence Table](advtexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="635ba-113">Ação</span><span class="sxs-lookup"><span data-stu-id="635ba-113">Action</span></span> |
|--------|
| <span data-ttu-id="635ba-114">CA1</span><span class="sxs-lookup"><span data-stu-id="635ba-114">CA1</span></span>    |
| <span data-ttu-id="635ba-115">CA35</span><span class="sxs-lookup"><span data-stu-id="635ba-115">CA35</span></span>   |



 

<span data-ttu-id="635ba-116">[Tabela CustomAction](customaction-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="635ba-116">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="635ba-117">Ação</span><span class="sxs-lookup"><span data-stu-id="635ba-117">Action</span></span> | <span data-ttu-id="635ba-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="635ba-118">Type</span></span> |
|--------|------|
| <span data-ttu-id="635ba-119">CA1</span><span class="sxs-lookup"><span data-stu-id="635ba-119">CA1</span></span>    | <span data-ttu-id="635ba-120">1</span><span class="sxs-lookup"><span data-stu-id="635ba-120">1</span></span>    |
| <span data-ttu-id="635ba-121">CA35</span><span class="sxs-lookup"><span data-stu-id="635ba-121">CA35</span></span>   | <span data-ttu-id="635ba-122">35</span><span class="sxs-lookup"><span data-stu-id="635ba-122">35</span></span>   |



 

## <a name="tables-used-during-execution"></a><span data-ttu-id="635ba-123">Tabelas usadas durante a execução</span><span class="sxs-lookup"><span data-stu-id="635ba-123">Tables used during execution</span></span>

[<span data-ttu-id="635ba-124">Tabela AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="635ba-124">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)

[<span data-ttu-id="635ba-125">Tabela CustomAction</span><span class="sxs-lookup"><span data-stu-id="635ba-125">CustomAction Table</span></span>](customaction-table.md)

## <a name="related-topics"></a><span data-ttu-id="635ba-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="635ba-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="635ba-127">Tipo de ação personalizada 19</span><span class="sxs-lookup"><span data-stu-id="635ba-127">Custom Action Type 19</span></span>](custom-action-type-19.md)
</dt> <dt>

[<span data-ttu-id="635ba-128">Tipo de ação personalizada 35</span><span class="sxs-lookup"><span data-stu-id="635ba-128">Custom Action Type 35</span></span>](custom-action-type-35.md)
</dt> <dt>

[<span data-ttu-id="635ba-129">Tipo de ação personalizada 51</span><span class="sxs-lookup"><span data-stu-id="635ba-129">Custom Action Type 51</span></span>](custom-action-type-51.md)
</dt> <dt>

[<span data-ttu-id="635ba-130">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="635ba-130">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



