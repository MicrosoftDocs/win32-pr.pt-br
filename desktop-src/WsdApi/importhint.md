---
description: 'Especifica o local de download para uma diretiva <WSDL: Import> que não especifica explicitamente um local.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: elemento importHint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce8da0a7fa45ed00489d405aaba8f1f6d7ab8fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760673"
---
# <a name="importhint-element"></a><span data-ttu-id="094a1-103">elemento importHint</span><span class="sxs-lookup"><span data-stu-id="094a1-103">importHint element</span></span>

<span data-ttu-id="094a1-104">Especifica o local de download para uma diretiva <WSDL: Import> que não especifica explicitamente um local.</span><span class="sxs-lookup"><span data-stu-id="094a1-104">Specifies the download location for a <wsdl:import> directive that does not explicitly specify a location.</span></span>

## <a name="usage"></a><span data-ttu-id="094a1-105">Uso</span><span class="sxs-lookup"><span data-stu-id="094a1-105">Usage</span></span>

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a><span data-ttu-id="094a1-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="094a1-106">Attributes</span></span>

<span data-ttu-id="094a1-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="094a1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="094a1-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="094a1-108">Child elements</span></span>



| <span data-ttu-id="094a1-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="094a1-109">Element</span></span>                                   | <span data-ttu-id="094a1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="094a1-110">Description</span></span>                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="094a1-111">**local**</span><span class="sxs-lookup"><span data-stu-id="094a1-111">**location**</span></span>](location.md)<br/>   | <span data-ttu-id="094a1-112">O local do arquivo a ser importado.</span><span class="sxs-lookup"><span data-stu-id="094a1-112">The location of the file to import.</span></span> <span data-ttu-id="094a1-113">O local pode ser um caminho relativo, um caminho absoluto ou uma URL HTTP.</span><span class="sxs-lookup"><span data-stu-id="094a1-113">The location may be a relative path, an absolute path, or an HTTP URL.</span></span><br/> <br/> |
| [<span data-ttu-id="094a1-114">**nameSpace**</span><span class="sxs-lookup"><span data-stu-id="094a1-114">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="094a1-115">O namespace a ser importado.</span><span class="sxs-lookup"><span data-stu-id="094a1-115">The namespace to import.</span></span> <span data-ttu-id="094a1-116">Isso deve corresponder ao namespace especificado no elemento <WSDL: Import>.</span><span class="sxs-lookup"><span data-stu-id="094a1-116">This should match the namespace specified in the <wsdl:import> element.</span></span><br/> <br/>     |



### <a name="child-element-sequence"></a><span data-ttu-id="094a1-117">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="094a1-117">Child element sequence</span></span>

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a><span data-ttu-id="094a1-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="094a1-118">Parent elements</span></span>



| <span data-ttu-id="094a1-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="094a1-119">Element</span></span>                         | <span data-ttu-id="094a1-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="094a1-120">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="094a1-121">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="094a1-121">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="094a1-122">Especifica um arquivo WSDL para processar informações de contrato.</span><span class="sxs-lookup"><span data-stu-id="094a1-122">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="094a1-123">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="094a1-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="094a1-124">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="094a1-124">Minimum supported system</span></span><br/> | <span data-ttu-id="094a1-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="094a1-125">Windows Vista</span></span> |
| <span data-ttu-id="094a1-126">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="094a1-126">Can be empty</span></span>                        | <span data-ttu-id="094a1-127">Não</span><span class="sxs-lookup"><span data-stu-id="094a1-127">No</span></span>            |



 

 




