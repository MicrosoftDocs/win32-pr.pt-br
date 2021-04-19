---
description: ICE22 usa a tabela FeatureComponents para validar o mapeamento de recursos e componentes referenciados na tabela PublishComponent.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754643"
---
# <a name="ice22"></a><span data-ttu-id="45c85-103">ICE22</span><span class="sxs-lookup"><span data-stu-id="45c85-103">ICE22</span></span>

<span data-ttu-id="45c85-104">ICE22 usa a [tabela FeatureComponents](featurecomponents-table.md) para validar o mapeamento de recursos e componentes referenciados na [tabela PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="45c85-104">ICE22 uses the [FeatureComponents table](featurecomponents-table.md) to validate the mapping of features and components referenced in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="45c85-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="45c85-105">Result</span></span>

<span data-ttu-id="45c85-106">O ICE22 posta uma mensagem de erro se os recursos e componentes estiverem mapeados incorretamente na [tabela PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="45c85-106">ICE22 posts an error message if the features and components are mapped incorrectly in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="45c85-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="45c85-107">Example</span></span>

<span data-ttu-id="45c85-108">Para o exemplo a seguir, ICE22 posta um erro que não {00000003-0004-0000-0000-624474732465} tem o mapeamento correto para as \_ colunas de recurso e componente \_ .</span><span class="sxs-lookup"><span data-stu-id="45c85-108">For the following example ICE22 posts an error that {00000003-0004-0000-0000-624474732465} does not have the correct mapping for the Feature\_ and Component\_ columns.</span></span>

<span data-ttu-id="45c85-109">[Tabela PublishComponent](publishcomponent-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="45c85-109">[PublishComponent Table](publishcomponent-table.md) (partial)</span></span>



| <span data-ttu-id="45c85-110">ComponentId</span><span class="sxs-lookup"><span data-stu-id="45c85-110">ComponentId</span></span>                            | <span data-ttu-id="45c85-111">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="45c85-111">Feature\_</span></span> | <span data-ttu-id="45c85-112">Componente\_</span><span class="sxs-lookup"><span data-stu-id="45c85-112">Component\_</span></span> |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="45c85-113">Feat1</span><span class="sxs-lookup"><span data-stu-id="45c85-113">Feat1</span></span>     | <span data-ttu-id="45c85-114">Comp1</span><span class="sxs-lookup"><span data-stu-id="45c85-114">Comp1</span></span>       |
| {00000003-0004-0000-0000-624474732465} | <span data-ttu-id="45c85-115">Feat1</span><span class="sxs-lookup"><span data-stu-id="45c85-115">Feat1</span></span>     | <span data-ttu-id="45c85-116">Comp2</span><span class="sxs-lookup"><span data-stu-id="45c85-116">Comp2</span></span>       |



 

<span data-ttu-id="45c85-117">[Tabela FeatureComponents](featurecomponents-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="45c85-117">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="45c85-118">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="45c85-118">Feature\_</span></span> | <span data-ttu-id="45c85-119">Componente\_</span><span class="sxs-lookup"><span data-stu-id="45c85-119">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="45c85-120">Feat1</span><span class="sxs-lookup"><span data-stu-id="45c85-120">Feat1</span></span>     | <span data-ttu-id="45c85-121">Comp1</span><span class="sxs-lookup"><span data-stu-id="45c85-121">Comp1</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="45c85-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45c85-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45c85-123">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="45c85-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



