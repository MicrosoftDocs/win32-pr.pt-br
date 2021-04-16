---
description: ICE10 valida que o estado de anúncio de recursos filho corresponde ao do seu recurso pai.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac8f1304f4444a0f087d747328cdea4b3d714ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750804"
---
# <a name="ice10"></a><span data-ttu-id="e8523-103">ICE10</span><span class="sxs-lookup"><span data-stu-id="e8523-103">ICE10</span></span>

<span data-ttu-id="e8523-104">ICE10 valida que o estado de anúncio de recursos filho corresponde ao do seu recurso pai.</span><span class="sxs-lookup"><span data-stu-id="e8523-104">ICE10 validates that the advertise state of child features matches that of its parent feature.</span></span>

<span data-ttu-id="e8523-105">Um recurso filho não pode cancelar o anúncio enquanto seu recurso pai permite anúncio.</span><span class="sxs-lookup"><span data-stu-id="e8523-105">A child feature may not disallow advertisement while its parent feature allows advertisement.</span></span> <span data-ttu-id="e8523-106">A seguinte combinação de atributos pai e filho é, portanto, inválida.</span><span class="sxs-lookup"><span data-stu-id="e8523-106">The following combination of parent and child attributes is therefore invalid.</span></span>

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

<span data-ttu-id="e8523-107">Essa combinação é inválida porque desligaria o pai sempre que o pai deveria ser anunciado.</span><span class="sxs-lookup"><span data-stu-id="e8523-107">This combination is invalid because it would turn off the parent whenever the parent was supposed to be advertised.</span></span> <span data-ttu-id="e8523-108">No entanto, o inverso é permitido.</span><span class="sxs-lookup"><span data-stu-id="e8523-108">However, the reverse is allowed.</span></span> <span data-ttu-id="e8523-109">Um filho pode ser marcado para favorecer o anúncio enquanto o pai está marcado para não permitir anúncio.</span><span class="sxs-lookup"><span data-stu-id="e8523-109">A child can be marked to favor advertisement while the parent is marked to disallow advertisement.</span></span>

<span data-ttu-id="e8523-110">A ação personalizada ICE10 determina o estado dos recursos pai e filho da coluna atributos da tabela de [recursos](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e8523-110">The ICE10 custom action determines the state of parent and child features from the Attributes column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="e8523-111">Observe que é válido definir o estado de um recurso como 0 e ter seu pai ou filho definido como favorecer ou não permitir anúncio.</span><span class="sxs-lookup"><span data-stu-id="e8523-111">Note that it is valid to set the state of a feature to 0 and have its parent or child set to favor or disallow advertisement.</span></span>

## <a name="result"></a><span data-ttu-id="e8523-112">Resultado</span><span class="sxs-lookup"><span data-stu-id="e8523-112">Result</span></span>

<span data-ttu-id="e8523-113">ICE10 posta um erro se a coluna Attributes da tabela [Feature](feature-table.md) contiver uma incompatibilidade no estado Advertise.</span><span class="sxs-lookup"><span data-stu-id="e8523-113">ICE10 posts an error if the Attributes column of the [Feature](feature-table.md) table contains a mismatch in the advertise state.</span></span>

## <a name="example"></a><span data-ttu-id="e8523-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e8523-114">Example</span></span>

<span data-ttu-id="e8523-115">ICE10 posta a seguinte mensagem de erro para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="e8523-115">ICE10 posts the following error message for the example shown.</span></span>

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

<span data-ttu-id="e8523-116">Observe que, para este exemplo, o Microsoft Excel e o Microsoft Word são recursos filho de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="e8523-116">Note for this example that Microsoft Excel and Microsoft Word are child features of Microsoft Office.</span></span>

<span data-ttu-id="e8523-117">Tabela de [recursos](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="e8523-117">[Feature](feature-table.md) table (partial)</span></span>



| <span data-ttu-id="e8523-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="e8523-118">Feature</span></span> | <span data-ttu-id="e8523-119">Pai do recurso \_</span><span class="sxs-lookup"><span data-stu-id="e8523-119">Feature\_Parent</span></span> | <span data-ttu-id="e8523-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="e8523-120">Attributes</span></span> |
|---------|-----------------|------------|
| <span data-ttu-id="e8523-121">Office</span><span class="sxs-lookup"><span data-stu-id="e8523-121">Office</span></span>  | <span data-ttu-id="e8523-122">Nulo</span><span class="sxs-lookup"><span data-stu-id="e8523-122">Null</span></span>            | <span data-ttu-id="e8523-123">4</span><span class="sxs-lookup"><span data-stu-id="e8523-123">4</span></span>          |
| <span data-ttu-id="e8523-124">Excel</span><span class="sxs-lookup"><span data-stu-id="e8523-124">Excel</span></span>   | <span data-ttu-id="e8523-125">Office</span><span class="sxs-lookup"><span data-stu-id="e8523-125">Office</span></span>          | <span data-ttu-id="e8523-126">4</span><span class="sxs-lookup"><span data-stu-id="e8523-126">4</span></span>          |
| <span data-ttu-id="e8523-127">Word</span><span class="sxs-lookup"><span data-stu-id="e8523-127">Word</span></span>    | <span data-ttu-id="e8523-128">Office</span><span class="sxs-lookup"><span data-stu-id="e8523-128">Office</span></span>          | <span data-ttu-id="e8523-129">8</span><span class="sxs-lookup"><span data-stu-id="e8523-129">8</span></span>          |



 

<span data-ttu-id="e8523-130">No exemplo, o Word está definido como não permitir anúncio, que está em conflito com o estado de anúncio de permissão de seu pai, Office.</span><span class="sxs-lookup"><span data-stu-id="e8523-130">In the example, Word is set to disallow advertisement, which conflicts with the allow advertisement state of its parent, Office.</span></span>

<span data-ttu-id="e8523-131">Em alguns casos, o ICE10 envia o seguinte erro:</span><span class="sxs-lookup"><span data-stu-id="e8523-131">In some cases ICE10 posts the following error:</span></span>

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

<span data-ttu-id="e8523-132">Refere-se a uma referência de chave estrangeira inválida.</span><span class="sxs-lookup"><span data-stu-id="e8523-132">This refers to an invalid foreign key reference.</span></span> <span data-ttu-id="e8523-133">A correção é ter o ponto ' filho ' em seu recurso pai correto ou adicionar uma entrada para o recurso pai ' pai ' à tabela de [recursos](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="e8523-133">The fix is to have 'Child' point to its correct parent feature, or add an entry for the parent feature 'Parent' to the [Feature](feature-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8523-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8523-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8523-135">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="e8523-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



