---
description: Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações unidirecionais e bidirecionais.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7282e7280c8d701710094b70b84a65756f7230ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171091"
---
# <a name="stubfunction-element"></a><span data-ttu-id="b9f31-103">elemento stubFunction</span><span class="sxs-lookup"><span data-stu-id="b9f31-103">stubFunction element</span></span>

<span data-ttu-id="b9f31-104">Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações unidirecionais e bidirecionais.</span><span class="sxs-lookup"><span data-stu-id="b9f31-104">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span>

## <a name="usage"></a><span data-ttu-id="b9f31-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b9f31-105">Usage</span></span>

``` syntax
<stubFunction/>
```

## <a name="attributes"></a><span data-ttu-id="b9f31-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b9f31-106">Attributes</span></span>

<span data-ttu-id="b9f31-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="b9f31-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b9f31-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b9f31-108">Child elements</span></span>

<span data-ttu-id="b9f31-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="b9f31-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b9f31-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b9f31-110">Parent elements</span></span>



| <span data-ttu-id="b9f31-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="b9f31-111">Element</span></span>                                                       | <span data-ttu-id="b9f31-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9f31-112">Description</span></span>                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="b9f31-113">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b9f31-113">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/> | <span data-ttu-id="b9f31-114">Gera constantes C para tipos de porta.</span><span class="sxs-lookup"><span data-stu-id="b9f31-114">Generates C constants for port types.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b9f31-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9f31-115">Remarks</span></span>

<span data-ttu-id="b9f31-116">As referências de função de stub são usadas em cenários de hospedagem para operações unidirecionais e bidirecionais.</span><span class="sxs-lookup"><span data-stu-id="b9f31-116">Stub function references are used in hosting scenarios for one-way and two-way operations.</span></span>

<span data-ttu-id="b9f31-117">Os valores válidos para esse elemento são 1 (referências de função TRUE/stub incluídas) e 0 (FALSE/nenhuma referência de função de stub incluída).</span><span class="sxs-lookup"><span data-stu-id="b9f31-117">Valid values for this element are 1 (TRUE/stub function references included) and 0 (FALSE/no stub function references included).</span></span>

## <a name="element-information"></a><span data-ttu-id="b9f31-118">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b9f31-118">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b9f31-119">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9f31-119">Minimum supported system</span></span><br/> | <span data-ttu-id="b9f31-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9f31-120">Windows Vista</span></span> |
| <span data-ttu-id="b9f31-121">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="b9f31-121">Can be empty</span></span>                        | <span data-ttu-id="b9f31-122">Sim</span><span class="sxs-lookup"><span data-stu-id="b9f31-122">Yes</span></span>           |



 

 




