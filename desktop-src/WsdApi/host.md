---
description: Define os elementos ServiceId e types para o host de serviço.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: elemento host
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f051f6665715ecaa519a060e18a3cbf4912210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993793"
---
# <a name="host-element"></a><span data-ttu-id="37707-103">elemento host</span><span class="sxs-lookup"><span data-stu-id="37707-103">host element</span></span>

<span data-ttu-id="37707-104">Define os elementos [**ServiceId**](serviceid.md) e [**Types**](types.md) para o host de serviço.</span><span class="sxs-lookup"><span data-stu-id="37707-104">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="37707-105">Uso</span><span class="sxs-lookup"><span data-stu-id="37707-105">Usage</span></span>

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a><span data-ttu-id="37707-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="37707-106">Attributes</span></span>

<span data-ttu-id="37707-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="37707-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="37707-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="37707-108">Child elements</span></span>



| <span data-ttu-id="37707-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="37707-109">Element</span></span>                                   | <span data-ttu-id="37707-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="37707-110">Description</span></span>                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="37707-111">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="37707-111">**ServiceID**</span></span>](serviceid.md)<br/> | <span data-ttu-id="37707-112">Define o identificador de serviço para o host de serviço.</span><span class="sxs-lookup"><span data-stu-id="37707-112">Defines the service identifier for the service host.</span></span><br/> <br/> |
| [<span data-ttu-id="37707-113">**Tipos**</span><span class="sxs-lookup"><span data-stu-id="37707-113">**Types**</span></span>](types.md)<br/>         | <span data-ttu-id="37707-114">Define uma lista de nomes qualificados XSD.</span><span class="sxs-lookup"><span data-stu-id="37707-114">Defines a list of XSD qualified names.</span></span><br/> <br/>               |



### <a name="child-element-sequence"></a><span data-ttu-id="37707-115">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="37707-115">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a><span data-ttu-id="37707-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="37707-116">Parent elements</span></span>



| <span data-ttu-id="37707-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="37707-117">Element</span></span>                                         | <span data-ttu-id="37707-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="37707-118">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="37707-119">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="37707-119">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="37707-120">Os metadados de hospedagem para o dispositivo a ser implementado.</span><span class="sxs-lookup"><span data-stu-id="37707-120">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="37707-121">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="37707-121">Element information</span></span>



| <span data-ttu-id="37707-122">Label</span><span class="sxs-lookup"><span data-stu-id="37707-122">Label</span></span> | <span data-ttu-id="37707-123">Valor</span><span class="sxs-lookup"><span data-stu-id="37707-123">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="37707-124">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37707-124">Minimum supported system</span></span><br/> | <span data-ttu-id="37707-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37707-125">Windows Vista</span></span> |
| <span data-ttu-id="37707-126">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="37707-126">Can be empty</span></span>                        | <span data-ttu-id="37707-127">Não</span><span class="sxs-lookup"><span data-stu-id="37707-127">No</span></span>            |



 

 




