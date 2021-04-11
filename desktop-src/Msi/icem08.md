---
description: O ICEM08 garante que um módulo não exclua outro módulo do qual depende.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9767c6748f5a21d83bddb3b5fe93a0a8d7ea67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170431"
---
# <a name="icem08"></a><span data-ttu-id="337fa-103">ICEM08</span><span class="sxs-lookup"><span data-stu-id="337fa-103">ICEM08</span></span>

<span data-ttu-id="337fa-104">O ICEM08 garante que um módulo não exclua outro módulo do qual depende.</span><span class="sxs-lookup"><span data-stu-id="337fa-104">ICEM08 ensures that a module does not exclude another module that it depends on.</span></span>

## <a name="result"></a><span data-ttu-id="337fa-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="337fa-105">Result</span></span>

<span data-ttu-id="337fa-106">ICEM08 posta um erro quando um módulo exclui outro módulo do qual ele depende.</span><span class="sxs-lookup"><span data-stu-id="337fa-106">ICEM08 posts an error when a module excludes another module that it depends on.</span></span>

## <a name="example"></a><span data-ttu-id="337fa-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="337fa-107">Example</span></span>

<span data-ttu-id="337fa-108">ICEM08 posta a seguinte mensagem de erro para um módulo que contém as entradas de banco de dados mostradas no exemplo.</span><span class="sxs-lookup"><span data-stu-id="337fa-108">ICEM08 posts the following error message for a module containing the database entries shown in the example.</span></span>

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[<span data-ttu-id="337fa-109">Tabela ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="337fa-109">ModuleDependency Table</span></span>](moduledependency-table.md)



| <span data-ttu-id="337fa-110">ModuleID</span><span class="sxs-lookup"><span data-stu-id="337fa-110">ModuleID</span></span>             | <span data-ttu-id="337fa-111">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="337fa-111">ModuleLanguage</span></span> | <span data-ttu-id="337fa-112">Requeridoid</span><span class="sxs-lookup"><span data-stu-id="337fa-112">RequiredID</span></span>           | <span data-ttu-id="337fa-113">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="337fa-113">RequiredLanguage</span></span> | <span data-ttu-id="337fa-114">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="337fa-114">RequiredVersion</span></span> |
|----------------------|----------------|----------------------|------------------|-----------------|
| <span data-ttu-id="337fa-115">Móduloa.<GUID></span><span class="sxs-lookup"><span data-stu-id="337fa-115">ModuleA.<GUID></span></span> | <span data-ttu-id="337fa-116">1046</span><span class="sxs-lookup"><span data-stu-id="337fa-116">1033</span></span>           | <span data-ttu-id="337fa-117">ModuleB.<GUID></span><span class="sxs-lookup"><span data-stu-id="337fa-117">ModuleB.<GUID></span></span> | <span data-ttu-id="337fa-118">1046</span><span class="sxs-lookup"><span data-stu-id="337fa-118">1033</span></span>             | <span data-ttu-id="337fa-119">1.0</span><span class="sxs-lookup"><span data-stu-id="337fa-119">1.0</span></span>             |



 

[<span data-ttu-id="337fa-120">Tabela ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="337fa-120">ModuleExclusion Table</span></span>](moduleexclusion-table.md)



| <span data-ttu-id="337fa-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="337fa-121">ModuleID</span></span>             | <span data-ttu-id="337fa-122">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="337fa-122">ModuleLanguage</span></span> | <span data-ttu-id="337fa-123">Exclusão excluída</span><span class="sxs-lookup"><span data-stu-id="337fa-123">ExcludedID</span></span>           | <span data-ttu-id="337fa-124">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="337fa-124">ExcludedLanguage</span></span> | <span data-ttu-id="337fa-125">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="337fa-125">ExcludedMinVersion</span></span> | <span data-ttu-id="337fa-126">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="337fa-126">ExcludedMaxVersion</span></span> |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| <span data-ttu-id="337fa-127">Móduloa.<GUID></span><span class="sxs-lookup"><span data-stu-id="337fa-127">ModuleA.<GUID></span></span> | <span data-ttu-id="337fa-128">1046</span><span class="sxs-lookup"><span data-stu-id="337fa-128">1033</span></span>           | <span data-ttu-id="337fa-129">ModuleB.<GUID></span><span class="sxs-lookup"><span data-stu-id="337fa-129">ModuleB.<GUID></span></span> | <span data-ttu-id="337fa-130">1046</span><span class="sxs-lookup"><span data-stu-id="337fa-130">1033</span></span>             |                    | <span data-ttu-id="337fa-131">1.0</span><span class="sxs-lookup"><span data-stu-id="337fa-131">1.0</span></span>                |



 

<span data-ttu-id="337fa-132">Para corrigir o erro, remova a dependência ou a exclusão.</span><span class="sxs-lookup"><span data-stu-id="337fa-132">To fix the error, remove either the dependency or the exclusion.</span></span> <span data-ttu-id="337fa-133">Se ModuleB for uma dependência (requeridoid) do Móduloa, você não poderá excluí-la (conforme mostrado na coluna ExludedID da tabela ModuleExclusion).</span><span class="sxs-lookup"><span data-stu-id="337fa-133">If ModuleB is a dependency (RequiredID) of ModuleA, you cannot exclude it (as shown in the ExludedID column of the ModuleExclusion table).</span></span> <span data-ttu-id="337fa-134">Se você precisar excluir ModuleB, deverá remover a dependência do Móduloa nele.</span><span class="sxs-lookup"><span data-stu-id="337fa-134">If you must exclude ModuleB, then you must remove ModuleA's dependency on it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="337fa-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="337fa-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="337fa-136">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="337fa-136">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



