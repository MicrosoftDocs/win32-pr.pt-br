---
description: Define um serviço a ser hospedado em uma função do construtor de hosts.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: elemento hostedService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfcf2f4c67cadf90279221fd5bdfd518e285e844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827825"
---
# <a name="hostedservice-element"></a><span data-ttu-id="15698-103">elemento hostedService</span><span class="sxs-lookup"><span data-stu-id="15698-103">hostedService element</span></span>

<span data-ttu-id="15698-104">Define um serviço a ser hospedado em uma função do construtor de hosts.</span><span class="sxs-lookup"><span data-stu-id="15698-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="15698-105">Uso</span><span class="sxs-lookup"><span data-stu-id="15698-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="15698-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="15698-106">Attributes</span></span>

<span data-ttu-id="15698-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="15698-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="15698-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="15698-108">Child elements</span></span>



| <span data-ttu-id="15698-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="15698-109">Element</span></span>                                     | <span data-ttu-id="15698-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="15698-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15698-111">**Codinome**</span><span class="sxs-lookup"><span data-stu-id="15698-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="15698-112">Especifica o nome a ser usado para o tipo de porta no código gerado.</span><span class="sxs-lookup"><span data-stu-id="15698-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="15698-113">Por padrão, o nome do código é gerado a partir do nome qualificado do tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="15698-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="15698-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="15698-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="15698-115">Tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="15698-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="15698-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="15698-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="15698-117">Nome da classe a ser gerada a partir da função do construtor.</span><span class="sxs-lookup"><span data-stu-id="15698-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="15698-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="15698-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="15698-119">Um URI que representa o identificador de serviço.</span><span class="sxs-lookup"><span data-stu-id="15698-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="15698-120">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="15698-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="15698-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="15698-121">Parent elements</span></span>



| <span data-ttu-id="15698-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="15698-122">Element</span></span>                         | <span data-ttu-id="15698-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="15698-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="15698-124">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="15698-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="15698-125">A especificação do arquivo de saída para o gerador de código.</span><span class="sxs-lookup"><span data-stu-id="15698-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="15698-126">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="15698-126">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="15698-127">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15698-127">Minimum supported system</span></span><br/> | <span data-ttu-id="15698-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15698-128">Windows Vista</span></span> |
| <span data-ttu-id="15698-129">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="15698-129">Can be empty</span></span>                        | <span data-ttu-id="15698-130">Não</span><span class="sxs-lookup"><span data-stu-id="15698-130">No</span></span>            |



 

 




