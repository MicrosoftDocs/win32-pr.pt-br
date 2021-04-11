---
description: ICE47 verifica o recurso e as tabelas FeatureComponents para obter recursos com 1600 ou mais componentes.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169400"
---
# <a name="ice47"></a><span data-ttu-id="2e9f1-103">ICE47</span><span class="sxs-lookup"><span data-stu-id="2e9f1-103">ICE47</span></span>

<span data-ttu-id="2e9f1-104">ICE47 verifica o [recurso](feature-table.md) e as tabelas [FeatureComponents](featurecomponents-table.md) para obter recursos com 1600 ou mais componentes.</span><span class="sxs-lookup"><span data-stu-id="2e9f1-104">ICE47 checks the [Feature](feature-table.md) and [FeatureComponents](featurecomponents-table.md) tables for features with 1600 or more components.</span></span>

## <a name="result"></a><span data-ttu-id="2e9f1-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="2e9f1-105">Result</span></span>

<span data-ttu-id="2e9f1-106">ICE47 posta uma mensagem de erro se um recurso exceder o limite máximo de 1600 componentes por recurso.</span><span class="sxs-lookup"><span data-stu-id="2e9f1-106">ICE47 posts an error message if a feature exceeds the maximum limit of 1600 components per feature.</span></span>

## <a name="example"></a><span data-ttu-id="2e9f1-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2e9f1-107">Example</span></span>

<span data-ttu-id="2e9f1-108">ICE47 relataria o seguinte aviso:</span><span class="sxs-lookup"><span data-stu-id="2e9f1-108">ICE47 would report the following warning:</span></span>

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

<span data-ttu-id="2e9f1-109">[Tabela de recursos](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="2e9f1-109">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="2e9f1-110">Recurso</span><span class="sxs-lookup"><span data-stu-id="2e9f1-110">Feature</span></span>  |
|----------|
| <span data-ttu-id="2e9f1-111">Feature1</span><span class="sxs-lookup"><span data-stu-id="2e9f1-111">Feature1</span></span> |



 

<span data-ttu-id="2e9f1-112">[Tabela FeatureComponents](featurecomponents-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="2e9f1-112">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="2e9f1-113">Ação</span><span class="sxs-lookup"><span data-stu-id="2e9f1-113">Action</span></span>   | <span data-ttu-id="2e9f1-114">Condição</span><span class="sxs-lookup"><span data-stu-id="2e9f1-114">Condition</span></span>     |
|----------|---------------|
| <span data-ttu-id="2e9f1-115">Feature1</span><span class="sxs-lookup"><span data-stu-id="2e9f1-115">Feature1</span></span> | <span data-ttu-id="2e9f1-116">Component1</span><span class="sxs-lookup"><span data-stu-id="2e9f1-116">Component1</span></span>    |
| <span data-ttu-id="2e9f1-117">Feature1</span><span class="sxs-lookup"><span data-stu-id="2e9f1-117">Feature1</span></span> | <span data-ttu-id="2e9f1-118">Component1600</span><span class="sxs-lookup"><span data-stu-id="2e9f1-118">Component1600</span></span> |



 

<span data-ttu-id="2e9f1-119">Para corrigir esse aviso, tente dividir o recurso em vários recursos</span><span class="sxs-lookup"><span data-stu-id="2e9f1-119">To fix this warning, try splitting the feature into several features</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e9f1-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e9f1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e9f1-121">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="2e9f1-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



