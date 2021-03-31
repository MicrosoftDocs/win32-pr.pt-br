---
title: Elemento Application
description: Representa o elemento de nível superior na especificação de marcação do Windows Ribbon Framework.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Faixa de das janelas do elemento de aplicativo
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103642953"
---
# <a name="application-element"></a><span data-ttu-id="a4af5-104">Elemento Application</span><span class="sxs-lookup"><span data-stu-id="a4af5-104">Application element</span></span>

<span data-ttu-id="a4af5-105">Representa o elemento de nível superior na especificação de marcação do Windows Ribbon Framework.</span><span class="sxs-lookup"><span data-stu-id="a4af5-105">Represents the top-level element in the Windows Ribbon framework markup specification.</span></span>

## <a name="usage"></a><span data-ttu-id="a4af5-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a4af5-106">Usage</span></span>

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a><span data-ttu-id="a4af5-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a4af5-107">Attributes</span></span>



| <span data-ttu-id="a4af5-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="a4af5-108">Attribute</span></span>            | <span data-ttu-id="a4af5-109">Type</span><span class="sxs-lookup"><span data-stu-id="a4af5-109">Type</span></span>                 | <span data-ttu-id="a4af5-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a4af5-110">Required</span></span>       | <span data-ttu-id="a4af5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4af5-111">Description</span></span>                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4af5-112">**xmlns**</span><span class="sxs-lookup"><span data-stu-id="a4af5-112">**xmlns**</span></span><br/> | <span data-ttu-id="a4af5-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="a4af5-113">xs:string</span></span><br/> | <span data-ttu-id="a4af5-114">Sim</span><span class="sxs-lookup"><span data-stu-id="a4af5-114">Yes</span></span><br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> <span data-ttu-id="a4af5-115">O URI para a associação de namespace de marcação da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="a4af5-115">The URI for the Ribbon markup namespace binding.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="a4af5-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a4af5-116">Child elements</span></span>



| <span data-ttu-id="a4af5-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="a4af5-117">Element</span></span>                                                                               | <span data-ttu-id="a4af5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4af5-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="a4af5-119">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="a4af5-119">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> | <span data-ttu-id="a4af5-120">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="a4af5-120">May occur at most once</span></span><br/> <br/>  |
| [<span data-ttu-id="a4af5-121">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="a4af5-121">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/>       | <span data-ttu-id="a4af5-122">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="a4af5-122">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a4af5-123">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a4af5-123">Parent elements</span></span>

<span data-ttu-id="a4af5-124">Não há elementos pai.</span><span class="sxs-lookup"><span data-stu-id="a4af5-124">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4af5-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4af5-125">Remarks</span></span>

<span data-ttu-id="a4af5-126">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a4af5-126">Required.</span></span>

<span data-ttu-id="a4af5-127">Deve ocorrer exatamente uma vez como o contêiner para toda a marcação da faixa de forma.</span><span class="sxs-lookup"><span data-stu-id="a4af5-127">Must occur exactly once as the container for all of the Ribbon markup.</span></span>

<span data-ttu-id="a4af5-128">Os elementos filho do elemento **Application** devem ocorrer na ordem especificada:</span><span class="sxs-lookup"><span data-stu-id="a4af5-128">The child elements of the **Application** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="a4af5-129">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="a4af5-129">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
2.  [<span data-ttu-id="a4af5-130">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="a4af5-130">**Application.Views**</span></span>](windowsribbon-element-application-views.md)

## <a name="examples"></a><span data-ttu-id="a4af5-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4af5-131">Examples</span></span>

<span data-ttu-id="a4af5-132">O exemplo a seguir mostra uma declaração de elemento de **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="a4af5-132">The following example shows an **Application** element declaration.</span></span>


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a><span data-ttu-id="a4af5-133">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a4af5-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="a4af5-134">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4af5-134">Minimum supported system</span></span><br/> | <span data-ttu-id="a4af5-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a4af5-135">Windows 7</span></span> |
| <span data-ttu-id="a4af5-136">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="a4af5-136">Can be empty</span></span>                        | <span data-ttu-id="a4af5-137">Não</span><span class="sxs-lookup"><span data-stu-id="a4af5-137">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="a4af5-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4af5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4af5-139">Declarando comandos e controles com marcação de faixa de medida</span><span class="sxs-lookup"><span data-stu-id="a4af5-139">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 





