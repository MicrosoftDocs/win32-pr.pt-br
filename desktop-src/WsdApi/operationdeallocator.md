---
description: Especifica a desalocação de tipo a ser usada por uma função de stub de operações.
ms.assetid: 52e6235d-90e6-4559-b17c-14ca3be896ff
title: elemento operationDeallocator
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c214b5dbc3245f63797c55880fe052d5c3ced15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763497"
---
# <a name="operationdeallocator-element"></a><span data-ttu-id="6fed4-103">elemento operationDeallocator</span><span class="sxs-lookup"><span data-stu-id="6fed4-103">operationDeallocator element</span></span>

<span data-ttu-id="6fed4-104">Especifica a desalocação de tipo a ser usada pela função de stub de uma operação.</span><span class="sxs-lookup"><span data-stu-id="6fed4-104">Specifies the type deallocator to be used by an operation's stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="6fed4-105">Uso</span><span class="sxs-lookup"><span data-stu-id="6fed4-105">Usage</span></span>

``` syntax
<operationDeallocator
  operation = "character_string"
  deallocator = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="6fed4-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="6fed4-106">Attributes</span></span>



| <span data-ttu-id="6fed4-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="6fed4-107">Attribute</span></span>                  | <span data-ttu-id="6fed4-108">Type</span><span class="sxs-lookup"><span data-stu-id="6fed4-108">Type</span></span>                         | <span data-ttu-id="6fed4-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6fed4-109">Required</span></span>       | <span data-ttu-id="6fed4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fed4-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------|------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fed4-111">**desalocador**</span><span class="sxs-lookup"><span data-stu-id="6fed4-111">**deallocator**</span></span><br/> | <span data-ttu-id="6fed4-112">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="6fed4-112">character\_string</span></span><br/> | <span data-ttu-id="6fed4-113">Yes</span><span class="sxs-lookup"><span data-stu-id="6fed4-113">Yes</span></span><br/> | <span data-ttu-id="6fed4-114">O desalocador a ser usado para a operação.</span><span class="sxs-lookup"><span data-stu-id="6fed4-114">The deallocator to use for the operation.</span></span><br/> <br/> <span data-ttu-id="6fed4-115">As cadeias de caracteres a seguir são valores válidos.</span><span class="sxs-lookup"><span data-stu-id="6fed4-115">The following strings are valid values.</span></span><br/> <br/> <dl><span data-ttu-id="6fed4-116"><span id="none"></span><span id="NONE"></span>\* \* \* \* <dt>nenhum \* \* \* \*</dt> <span id="WSDFreeLinkedMemory"></span> <span id="wsdfreelinkedmemory"></span> <span id="WSDFREELINKEDMEMORY"></span> \* \* \* \* <dt>WSDFreeLinkedMemory \* \* \* \*</dt> <span id="CoTaskMemFree"></span> <span id="cotaskmemfree"></span> <span id="COTASKMEMFREE"></span> \* \* \* \* <dt>CoTaskMemFree \* \* \* \*</dt> <span id="free"></span> <span id="FREE"></span> \* \* \* \* <dt>gratuito \* *</dt> <span id="delete"></span> <span id="DELETE"></span> \* \* <dt>* \* \* \* excluir \* \* \* \*</dt> <span id="deleteArray"></span> <span id="deletearray"></span> <span id="DELETEARRAY"></span> \* \* \* \* <dt>deleteArray \* \* \* \*</dt> <span id="Release"></span> <span id="release"></span> <span id="RELEASE"></span> \* \* \* \* <dt>Versão \*</dt> \* \* \*</span><span class="sxs-lookup"><span data-stu-id="6fed4-116"><span id="none"></span><span id="NONE"></span><dt>\*\*\*\*none\*\*\*\*</dt><span id="WSDFreeLinkedMemory"></span><span id="wsdfreelinkedmemory"></span><span id="WSDFREELINKEDMEMORY"></span><dt>\*\*\*\*WSDFreeLinkedMemory\*\*\*\*</dt><span id="CoTaskMemFree"></span><span id="cotaskmemfree"></span><span id="COTASKMEMFREE"></span><dt>\*\*\*\*CoTaskMemFree\*\*\*\*</dt><span id="free"></span><span id="FREE"></span><dt>\*\*\*\*free\*\*\*\*</dt><span id="delete"></span><span id="DELETE"></span><dt>\*\*\*\*delete\*\*\*\*</dt><span id="deleteArray"></span><span id="deletearray"></span><span id="DELETEARRAY"></span><dt>\*\*\*\*deleteArray\*\*\*\*</dt><span id="Release"></span><span id="release"></span><span id="RELEASE"></span><dt>\*\*\*\*Release\*\*\*\*</dt></span></span> </dl> |
| <span data-ttu-id="6fed4-117">**operation**</span><span class="sxs-lookup"><span data-stu-id="6fed4-117">**operation**</span></span><br/>   | <span data-ttu-id="6fed4-118">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="6fed4-118">character\_string</span></span><br/> | <span data-ttu-id="6fed4-119">Yes</span><span class="sxs-lookup"><span data-stu-id="6fed4-119">Yes</span></span><br/> | <span data-ttu-id="6fed4-120">O nome da operação.</span><span class="sxs-lookup"><span data-stu-id="6fed4-120">The name of the operation.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="child-elements"></a><span data-ttu-id="6fed4-121">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6fed4-121">Child elements</span></span>

<span data-ttu-id="6fed4-122">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="6fed4-122">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6fed4-123">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6fed4-123">Parent elements</span></span>



| <span data-ttu-id="6fed4-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="6fed4-124">Element</span></span>                                               | <span data-ttu-id="6fed4-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fed4-125">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fed4-126">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="6fed4-126">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="6fed4-127">Gera implementações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="6fed4-127">Generates implementations for stub functions for port type operations.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="6fed4-128">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="6fed4-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="6fed4-129">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fed4-129">Minimum supported system</span></span><br/> | <span data-ttu-id="6fed4-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fed4-130">Windows Vista</span></span> |
| <span data-ttu-id="6fed4-131">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="6fed4-131">Can be empty</span></span>                        | <span data-ttu-id="6fed4-132">Sim</span><span class="sxs-lookup"><span data-stu-id="6fed4-132">Yes</span></span>           |



 

 




