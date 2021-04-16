---
description: ICEM10 verifica se um módulo de mesclagem contém apenas propriedades que são permitidas na tabela de propriedades.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752454"
---
# <a name="icem10"></a><span data-ttu-id="8ed7e-103">ICEM10</span><span class="sxs-lookup"><span data-stu-id="8ed7e-103">ICEM10</span></span>

<span data-ttu-id="8ed7e-104">ICEM10 verifica se um módulo de mesclagem contém apenas propriedades que são permitidas na [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ed7e-104">ICEM10 verifies that a merge module contains only properties that are allowed in the [Property Table](property-table.md).</span></span> <span data-ttu-id="8ed7e-105">As propriedades específicas do produto a seguir não são permitidas na tabela de propriedades:</span><span class="sxs-lookup"><span data-stu-id="8ed7e-105">The following product specific properties are not allowed in the Property Table:</span></span>

-   [<span data-ttu-id="8ed7e-106">**Propriedade ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="8ed7e-106">**ProductLanguage Property**</span></span>](productlanguage.md)
-   [<span data-ttu-id="8ed7e-107">**Propriedade ProductCode**</span><span class="sxs-lookup"><span data-stu-id="8ed7e-107">**ProductCode Property**</span></span>](productcode.md)
-   [<span data-ttu-id="8ed7e-108">**Propriedade ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="8ed7e-108">**ProductVersion Property**</span></span>](productversion.md)
-   [<span data-ttu-id="8ed7e-109">**Propriedade ProductName**</span><span class="sxs-lookup"><span data-stu-id="8ed7e-109">**ProductName Property**</span></span>](productname.md)
-   [<span data-ttu-id="8ed7e-110">**Propriedade manufacturer**</span><span class="sxs-lookup"><span data-stu-id="8ed7e-110">**Manufacturer Property**</span></span>](manufacturer.md)

## <a name="result"></a><span data-ttu-id="8ed7e-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="8ed7e-111">Result</span></span>

<span data-ttu-id="8ed7e-112">ICEM10 posta um erro quando um módulo de mesclagem contém uma propriedade que não é permitida na [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ed7e-112">ICEM10 posts an error when a merge module contains a property that is not allowed in the [Property Table](property-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="8ed7e-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8ed7e-113">Example</span></span>

<span data-ttu-id="8ed7e-114">ICEM10 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas.</span><span class="sxs-lookup"><span data-stu-id="8ed7e-114">ICEM10 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

<span data-ttu-id="8ed7e-115">A tabela a seguir mostra uma [tabela de propriedades](property-table.md)parcial.</span><span class="sxs-lookup"><span data-stu-id="8ed7e-115">The following table shows you a partial [Property Table](property-table.md).</span></span>



| <span data-ttu-id="8ed7e-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8ed7e-116">Property</span></span>                                   | <span data-ttu-id="8ed7e-117">Valores</span><span class="sxs-lookup"><span data-stu-id="8ed7e-117">Values</span></span>    |
|--------------------------------------------|-----------|
| <span data-ttu-id="8ed7e-118">Cor</span><span class="sxs-lookup"><span data-stu-id="8ed7e-118">Color</span></span>                                      | <span data-ttu-id="8ed7e-119">Vermelho</span><span class="sxs-lookup"><span data-stu-id="8ed7e-119">Red</span></span>       |
| [<span data-ttu-id="8ed7e-120">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="8ed7e-120">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="8ed7e-121">Microsoft</span><span class="sxs-lookup"><span data-stu-id="8ed7e-121">Microsoft</span></span> |
| [<span data-ttu-id="8ed7e-122">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="8ed7e-122">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="8ed7e-123">1046</span><span class="sxs-lookup"><span data-stu-id="8ed7e-123">1033</span></span>      |



 

<span data-ttu-id="8ed7e-124">O procedimento a seguir mostra como corrigir erros.</span><span class="sxs-lookup"><span data-stu-id="8ed7e-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="8ed7e-125">**Para corrigir os erros**</span><span class="sxs-lookup"><span data-stu-id="8ed7e-125">**To fix the errors**</span></span>

1.  <span data-ttu-id="8ed7e-126">Remova a propriedade '[**manufacturer**](manufacturer.md)' da [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ed7e-126">Remove the '[**Manufacturer**](manufacturer.md)' property from the [Property Table](property-table.md).</span></span>
2.  <span data-ttu-id="8ed7e-127">Remova a propriedade '[**ProductLanguage**](productlanguage.md)' da [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8ed7e-127">Remove the '[**ProductLanguage**](productlanguage.md)' property from the [Property Table](property-table.md).</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="8ed7e-128">Tabela usada durante a execução</span><span class="sxs-lookup"><span data-stu-id="8ed7e-128">Table Used During Execution</span></span>

<span data-ttu-id="8ed7e-129">A [tabela de propriedades](property-table.md) é usada durante a execução.</span><span class="sxs-lookup"><span data-stu-id="8ed7e-129">The [Property Table](property-table.md) is used during execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ed7e-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ed7e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ed7e-131">Referência de ICE do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="8ed7e-131">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



