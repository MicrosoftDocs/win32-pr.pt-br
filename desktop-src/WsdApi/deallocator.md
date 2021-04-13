---
description: Especifica o tipo de desalocação a ser usado por uma função de stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: elemento dealocador
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165311"
---
# <a name="deallocator-element"></a><span data-ttu-id="e093e-103">elemento dealocador</span><span class="sxs-lookup"><span data-stu-id="e093e-103">deallocator element</span></span>

<span data-ttu-id="e093e-104">Especifica o tipo de desalocação a ser usado por uma função de stub.</span><span class="sxs-lookup"><span data-stu-id="e093e-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="e093e-105">Uso</span><span class="sxs-lookup"><span data-stu-id="e093e-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="e093e-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="e093e-106">Attributes</span></span>

<span data-ttu-id="e093e-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="e093e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e093e-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e093e-108">Child elements</span></span>

<span data-ttu-id="e093e-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="e093e-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e093e-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e093e-110">Parent elements</span></span>



| <span data-ttu-id="e093e-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="e093e-111">Element</span></span>                                               | <span data-ttu-id="e093e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e093e-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e093e-113">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="e093e-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="e093e-114">Gera implementações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="e093e-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e093e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e093e-115">Remarks</span></span>

<span data-ttu-id="e093e-116">O tipo de desalocação deve ser colocado em um par de <deallocator></deallocator> marcas.</span><span class="sxs-lookup"><span data-stu-id="e093e-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="e093e-117">As cadeias de caracteres a seguir são valores válidos de dealocador:</span><span class="sxs-lookup"><span data-stu-id="e093e-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="e093e-118">nenhum</span><span class="sxs-lookup"><span data-stu-id="e093e-118">none</span></span>
-   <span data-ttu-id="e093e-119">WSDFreeLinkedMemory</span><span class="sxs-lookup"><span data-stu-id="e093e-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="e093e-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="e093e-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="e093e-121">free</span><span class="sxs-lookup"><span data-stu-id="e093e-121">free</span></span>
-   <span data-ttu-id="e093e-122">excluir</span><span class="sxs-lookup"><span data-stu-id="e093e-122">delete</span></span>
-   <span data-ttu-id="e093e-123">deleteArray</span><span class="sxs-lookup"><span data-stu-id="e093e-123">deleteArray</span></span>
-   <span data-ttu-id="e093e-124">Versão</span><span class="sxs-lookup"><span data-stu-id="e093e-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="e093e-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e093e-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e093e-126">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e093e-126">Minimum supported system</span></span><br/> | <span data-ttu-id="e093e-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e093e-127">Windows Vista</span></span> |
| <span data-ttu-id="e093e-128">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="e093e-128">Can be empty</span></span>                        | <span data-ttu-id="e093e-129">Sim</span><span class="sxs-lookup"><span data-stu-id="e093e-129">Yes</span></span>           |



 

 




