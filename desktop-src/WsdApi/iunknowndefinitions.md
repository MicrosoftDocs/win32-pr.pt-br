---
description: Gera implementações para as funções QueryInterface, AddRef e Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763111"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="9d3f0-103">Elemento IUnknownDefinitions</span><span class="sxs-lookup"><span data-stu-id="9d3f0-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="9d3f0-104">Gera implementações para as funções QueryInterface, AddRef e Release.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="9d3f0-105">Uso</span><span class="sxs-lookup"><span data-stu-id="9d3f0-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="9d3f0-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d3f0-106">Attributes</span></span>



| <span data-ttu-id="9d3f0-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="9d3f0-107">Attribute</span></span>                  | <span data-ttu-id="9d3f0-108">Type</span><span class="sxs-lookup"><span data-stu-id="9d3f0-108">Type</span></span>                         | <span data-ttu-id="9d3f0-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9d3f0-109">Required</span></span>       | <span data-ttu-id="9d3f0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d3f0-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="9d3f0-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="9d3f0-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="9d3f0-112">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="9d3f0-112">character\_string</span></span><br/> | <span data-ttu-id="9d3f0-113">Yes</span><span class="sxs-lookup"><span data-stu-id="9d3f0-113">Yes</span></span><br/> | <span data-ttu-id="9d3f0-114">O nome da classe de implementação.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="9d3f0-115">**refCountVar**</span><span class="sxs-lookup"><span data-stu-id="9d3f0-115">**refCountVar**</span></span><br/> | <span data-ttu-id="9d3f0-116">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="9d3f0-116">character\_string</span></span><br/> | <span data-ttu-id="9d3f0-117">Yes</span><span class="sxs-lookup"><span data-stu-id="9d3f0-117">Yes</span></span><br/> | <span data-ttu-id="9d3f0-118">O nome da variável de contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="9d3f0-119">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9d3f0-119">Child elements</span></span>



| <span data-ttu-id="9d3f0-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="9d3f0-120">Element</span></span>                                   | <span data-ttu-id="9d3f0-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d3f0-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d3f0-122">**interface**</span><span class="sxs-lookup"><span data-stu-id="9d3f0-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="9d3f0-123">O nome da interface a ser retornada por QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="9d3f0-124">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="9d3f0-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="9d3f0-125">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9d3f0-125">Parent elements</span></span>



| <span data-ttu-id="9d3f0-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="9d3f0-126">Element</span></span>                         | <span data-ttu-id="9d3f0-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d3f0-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9d3f0-128">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="9d3f0-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="9d3f0-129">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="9d3f0-130">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9d3f0-130">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="9d3f0-131">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d3f0-131">Minimum supported system</span></span><br/> | <span data-ttu-id="9d3f0-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d3f0-132">Windows Vista</span></span> |
| <span data-ttu-id="9d3f0-133">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="9d3f0-133">Can be empty</span></span>                        | <span data-ttu-id="9d3f0-134">Não</span><span class="sxs-lookup"><span data-stu-id="9d3f0-134">No</span></span>            |



 

 




