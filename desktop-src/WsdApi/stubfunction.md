---
description: Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações unidirecionais e bidirecionais.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77f37aed20dae4f04eea087e3d1eac2d23369af
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994143"
---
# <a name="stubfunction-element"></a><span data-ttu-id="bd992-103">elemento stubFunction</span><span class="sxs-lookup"><span data-stu-id="bd992-103">stubFunction element</span></span>

<span data-ttu-id="bd992-104">Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações unidirecionais e bidirecionais.</span><span class="sxs-lookup"><span data-stu-id="bd992-104">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span>

## <a name="usage"></a><span data-ttu-id="bd992-105">Uso</span><span class="sxs-lookup"><span data-stu-id="bd992-105">Usage</span></span>

``` syntax
<stubFunction/>
```

## <a name="attributes"></a><span data-ttu-id="bd992-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="bd992-106">Attributes</span></span>

<span data-ttu-id="bd992-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="bd992-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bd992-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bd992-108">Child elements</span></span>

<span data-ttu-id="bd992-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="bd992-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="bd992-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="bd992-110">Parent elements</span></span>



| <span data-ttu-id="bd992-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="bd992-111">Element</span></span>                                                       | <span data-ttu-id="bd992-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd992-112">Description</span></span>                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="bd992-113">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="bd992-113">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/> | <span data-ttu-id="bd992-114">Gera constantes C para tipos de porta.</span><span class="sxs-lookup"><span data-stu-id="bd992-114">Generates C constants for port types.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="bd992-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd992-115">Remarks</span></span>

<span data-ttu-id="bd992-116">As referências de função de stub são usadas em cenários de hospedagem para operações unidirecionais e bidirecionais.</span><span class="sxs-lookup"><span data-stu-id="bd992-116">Stub function references are used in hosting scenarios for one-way and two-way operations.</span></span>

<span data-ttu-id="bd992-117">Os valores válidos para esse elemento são 1 (referências de função TRUE/stub incluídas) e 0 (FALSE/nenhuma referência de função de stub incluída).</span><span class="sxs-lookup"><span data-stu-id="bd992-117">Valid values for this element are 1 (TRUE/stub function references included) and 0 (FALSE/no stub function references included).</span></span>

## <a name="element-information"></a><span data-ttu-id="bd992-118">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="bd992-118">Element information</span></span>



| <span data-ttu-id="bd992-119">Label</span><span class="sxs-lookup"><span data-stu-id="bd992-119">Label</span></span> | <span data-ttu-id="bd992-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bd992-120">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="bd992-121">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd992-121">Minimum supported system</span></span><br/> | <span data-ttu-id="bd992-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd992-122">Windows Vista</span></span> |
| <span data-ttu-id="bd992-123">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="bd992-123">Can be empty</span></span>                        | <span data-ttu-id="bd992-124">Sim</span><span class="sxs-lookup"><span data-stu-id="bd992-124">Yes</span></span>           |



 

 




