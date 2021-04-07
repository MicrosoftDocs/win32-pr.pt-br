---
description: Define os elementos ServiceId e types para o host de serviço.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: elemento host
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec073a89cf1911ab363d757d36cd264c85c8a5c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827826"
---
# <a name="host-element"></a><span data-ttu-id="80b9d-103">elemento host</span><span class="sxs-lookup"><span data-stu-id="80b9d-103">host element</span></span>

<span data-ttu-id="80b9d-104">Define os elementos [**ServiceId**](serviceid.md) e [**Types**](types.md) para o host de serviço.</span><span class="sxs-lookup"><span data-stu-id="80b9d-104">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the service host.</span></span>

## <a name="usage"></a><span data-ttu-id="80b9d-105">Uso</span><span class="sxs-lookup"><span data-stu-id="80b9d-105">Usage</span></span>

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a><span data-ttu-id="80b9d-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="80b9d-106">Attributes</span></span>

<span data-ttu-id="80b9d-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="80b9d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="80b9d-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="80b9d-108">Child elements</span></span>



| <span data-ttu-id="80b9d-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="80b9d-109">Element</span></span>                                   | <span data-ttu-id="80b9d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="80b9d-110">Description</span></span>                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="80b9d-111">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="80b9d-111">**ServiceID**</span></span>](serviceid.md)<br/> | <span data-ttu-id="80b9d-112">Define o identificador de serviço para o host de serviço.</span><span class="sxs-lookup"><span data-stu-id="80b9d-112">Defines the service identifier for the service host.</span></span><br/> <br/> |
| [<span data-ttu-id="80b9d-113">**Tipos**</span><span class="sxs-lookup"><span data-stu-id="80b9d-113">**Types**</span></span>](types.md)<br/>         | <span data-ttu-id="80b9d-114">Define uma lista de nomes qualificados XSD.</span><span class="sxs-lookup"><span data-stu-id="80b9d-114">Defines a list of XSD qualified names.</span></span><br/> <br/>               |



### <a name="child-element-sequence"></a><span data-ttu-id="80b9d-115">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="80b9d-115">Child element sequence</span></span>

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a><span data-ttu-id="80b9d-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="80b9d-116">Parent elements</span></span>



| <span data-ttu-id="80b9d-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="80b9d-117">Element</span></span>                                         | <span data-ttu-id="80b9d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="80b9d-118">Description</span></span>                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="80b9d-119">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="80b9d-119">**hostMetadata**</span></span>](hostmetadata.md)<br/> | <span data-ttu-id="80b9d-120">Os metadados de hospedagem para o dispositivo a ser implementado.</span><span class="sxs-lookup"><span data-stu-id="80b9d-120">The hosting metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="80b9d-121">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="80b9d-121">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="80b9d-122">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80b9d-122">Minimum supported system</span></span><br/> | <span data-ttu-id="80b9d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80b9d-123">Windows Vista</span></span> |
| <span data-ttu-id="80b9d-124">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="80b9d-124">Can be empty</span></span>                        | <span data-ttu-id="80b9d-125">Não</span><span class="sxs-lookup"><span data-stu-id="80b9d-125">No</span></span>            |



 

 




