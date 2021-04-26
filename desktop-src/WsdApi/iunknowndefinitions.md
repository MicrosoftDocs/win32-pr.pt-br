---
description: Gera implementações para as funções QueryInterface, AddRef e Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Elemento IUnknownDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995143"
---
# <a name="iunknowndefinitions-element"></a><span data-ttu-id="87db7-103">Elemento IUnknownDefinitions</span><span class="sxs-lookup"><span data-stu-id="87db7-103">IUnknownDefinitions element</span></span>

<span data-ttu-id="87db7-104">Gera implementações para as funções QueryInterface, AddRef e Release.</span><span class="sxs-lookup"><span data-stu-id="87db7-104">Generates implementations for the QueryInterface, AddRef and Release functions.</span></span>

## <a name="usage"></a><span data-ttu-id="87db7-105">Uso</span><span class="sxs-lookup"><span data-stu-id="87db7-105">Usage</span></span>

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="87db7-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="87db7-106">Attributes</span></span>



| <span data-ttu-id="87db7-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="87db7-107">Attribute</span></span>                  | <span data-ttu-id="87db7-108">Type</span><span class="sxs-lookup"><span data-stu-id="87db7-108">Type</span></span>                         | <span data-ttu-id="87db7-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="87db7-109">Required</span></span>       | <span data-ttu-id="87db7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="87db7-110">Description</span></span>                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| <span data-ttu-id="87db7-111">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="87db7-111">**proxyClass**</span></span><br/>  | <span data-ttu-id="87db7-112">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="87db7-112">character\_string</span></span><br/> | <span data-ttu-id="87db7-113">Sim</span><span class="sxs-lookup"><span data-stu-id="87db7-113">Yes</span></span><br/> | <span data-ttu-id="87db7-114">O nome da classe de implementação.</span><span class="sxs-lookup"><span data-stu-id="87db7-114">The name of the implementing class.</span></span><br/> <br/> |
| <span data-ttu-id="87db7-115">**refCountVar**</span><span class="sxs-lookup"><span data-stu-id="87db7-115">**refCountVar**</span></span><br/> | <span data-ttu-id="87db7-116">Cadeia de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="87db7-116">character\_string</span></span><br/> | <span data-ttu-id="87db7-117">Sim</span><span class="sxs-lookup"><span data-stu-id="87db7-117">Yes</span></span><br/> | <span data-ttu-id="87db7-118">O nome da variável de contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="87db7-118">The reference count variable name.</span></span><br/> <br/>  |



## <a name="child-elements"></a><span data-ttu-id="87db7-119">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="87db7-119">Child elements</span></span>



| <span data-ttu-id="87db7-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="87db7-120">Element</span></span>                                   | <span data-ttu-id="87db7-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="87db7-121">Description</span></span>                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="87db7-122">**interface**</span><span class="sxs-lookup"><span data-stu-id="87db7-122">**interface**</span></span>](interface.md)<br/> | <span data-ttu-id="87db7-123">O nome da interface a ser retornada por QueryInterface.</span><span class="sxs-lookup"><span data-stu-id="87db7-123">The name of the interface to be returned by QueryInterface.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="87db7-124">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="87db7-124">Child element sequence</span></span>

``` syntax
interface
```

## <a name="parent-elements"></a><span data-ttu-id="87db7-125">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="87db7-125">Parent elements</span></span>



| <span data-ttu-id="87db7-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="87db7-126">Element</span></span>                         | <span data-ttu-id="87db7-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="87db7-127">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="87db7-128">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="87db7-128">**file**</span></span>](file.md)<br/> | <span data-ttu-id="87db7-129">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="87db7-129">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="87db7-130">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="87db7-130">Element information</span></span>



| <span data-ttu-id="87db7-131">Label</span><span class="sxs-lookup"><span data-stu-id="87db7-131">Label</span></span> | <span data-ttu-id="87db7-132">Valor</span><span class="sxs-lookup"><span data-stu-id="87db7-132">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="87db7-133">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87db7-133">Minimum supported system</span></span><br/> | <span data-ttu-id="87db7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87db7-134">Windows Vista</span></span> |
| <span data-ttu-id="87db7-135">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="87db7-135">Can be empty</span></span>                        | <span data-ttu-id="87db7-136">Não</span><span class="sxs-lookup"><span data-stu-id="87db7-136">No</span></span>            |



 

 




