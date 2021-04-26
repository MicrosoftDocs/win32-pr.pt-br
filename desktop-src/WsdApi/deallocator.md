---
description: Especifica o tipo de desalocação a ser usado por uma função de stub.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: elemento dealocador
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692ed2e57b3e649c0ee7af171f205c949496f9b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994933"
---
# <a name="deallocator-element"></a><span data-ttu-id="7905b-103">elemento dealocador</span><span class="sxs-lookup"><span data-stu-id="7905b-103">deallocator element</span></span>

<span data-ttu-id="7905b-104">Especifica o tipo de desalocação a ser usado por uma função de stub.</span><span class="sxs-lookup"><span data-stu-id="7905b-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="7905b-105">Uso</span><span class="sxs-lookup"><span data-stu-id="7905b-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="7905b-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="7905b-106">Attributes</span></span>

<span data-ttu-id="7905b-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="7905b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7905b-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7905b-108">Child elements</span></span>

<span data-ttu-id="7905b-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="7905b-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7905b-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7905b-110">Parent elements</span></span>



| <span data-ttu-id="7905b-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="7905b-111">Element</span></span>                                               | <span data-ttu-id="7905b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7905b-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7905b-113">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="7905b-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="7905b-114">Gera implementações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="7905b-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7905b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7905b-115">Remarks</span></span>

<span data-ttu-id="7905b-116">O tipo de desalocação deve ser colocado em um par de <deallocator></deallocator> marcas.</span><span class="sxs-lookup"><span data-stu-id="7905b-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="7905b-117">As cadeias de caracteres a seguir são valores válidos de dealocador:</span><span class="sxs-lookup"><span data-stu-id="7905b-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="7905b-118">nenhum</span><span class="sxs-lookup"><span data-stu-id="7905b-118">none</span></span>
-   <span data-ttu-id="7905b-119">WSDFreeLinkedMemory</span><span class="sxs-lookup"><span data-stu-id="7905b-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="7905b-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="7905b-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="7905b-121">free</span><span class="sxs-lookup"><span data-stu-id="7905b-121">free</span></span>
-   <span data-ttu-id="7905b-122">excluir</span><span class="sxs-lookup"><span data-stu-id="7905b-122">delete</span></span>
-   <span data-ttu-id="7905b-123">deleteArray</span><span class="sxs-lookup"><span data-stu-id="7905b-123">deleteArray</span></span>
-   <span data-ttu-id="7905b-124">Versão</span><span class="sxs-lookup"><span data-stu-id="7905b-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="7905b-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7905b-125">Element information</span></span>



| <span data-ttu-id="7905b-126">Label</span><span class="sxs-lookup"><span data-stu-id="7905b-126">Label</span></span> | <span data-ttu-id="7905b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7905b-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="7905b-128">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7905b-128">Minimum supported system</span></span><br/> | <span data-ttu-id="7905b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7905b-129">Windows Vista</span></span> |
| <span data-ttu-id="7905b-130">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="7905b-130">Can be empty</span></span>                        | <span data-ttu-id="7905b-131">Sim</span><span class="sxs-lookup"><span data-stu-id="7905b-131">Yes</span></span>           |



 

 




