---
description: ICE14 valida a tabela de recursos de um banco de dados Windows Installer.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296914"
---
# <a name="ice14"></a><span data-ttu-id="c082c-103">ICE14</span><span class="sxs-lookup"><span data-stu-id="c082c-103">ICE14</span></span>

<span data-ttu-id="c082c-104">O ICE14 valida o seguinte para os recursos:</span><span class="sxs-lookup"><span data-stu-id="c082c-104">ICE14 validates the following for features:</span></span>

-   <span data-ttu-id="c082c-105">Os recursos pai raiz não têm o conjunto de bits msidbFeatureAttributesFollowParent na coluna atributos da tabela de [recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c082c-105">That root parent features do not have the msidbFeatureAttributesFollowParent bit set in the Attributes column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="c082c-106">Um recurso raiz não tem um pai.</span><span class="sxs-lookup"><span data-stu-id="c082c-106">A root feature does not have a parent.</span></span>
-   <span data-ttu-id="c082c-107">Que nenhum recurso tenha a mesma entrada nas \_ colunas pai de recurso e recurso da [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c082c-107">That no feature has the same entry in the Feature and Feature\_Parent columns of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="c082c-108">Nenhum recurso pode ser seu próprio pai.</span><span class="sxs-lookup"><span data-stu-id="c082c-108">No feature can be its own parent.</span></span>

## <a name="result"></a><span data-ttu-id="c082c-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="c082c-109">Result</span></span>

<span data-ttu-id="c082c-110">ICE14 posta uma mensagem de erro se encontrar um recurso raiz com o conjunto de bits msidbFeatureAttributesFollowParent ou um recurso com entradas idênticas nas \_ colunas pai do recurso e do recurso da tabela de recursos.</span><span class="sxs-lookup"><span data-stu-id="c082c-110">ICE14 posts an error message if it finds a root feature with the msidbFeatureAttributesFollowParent bit set or a feature with identical entries in the Feature and Feature\_Parent columns of the Feature table.</span></span>

## <a name="example"></a><span data-ttu-id="c082c-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c082c-111">Example</span></span>

<span data-ttu-id="c082c-112">ICE14 retornaria os seguintes erros para o exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="c082c-112">ICE14 would return the following errors for the following example:</span></span>

-   <span data-ttu-id="c082c-113">O esporte do recurso tem o mesmo valor nas colunas pai do recurso e \_ do recurso da tabela de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c082c-113">The feature Sport has the same value in the Feature and Feature\_Parent columns of the File table.</span></span>
-   <span data-ttu-id="c082c-114">O esporte do recurso raiz tem o conjunto de bits msidbFeatureAttributesFollowParent.</span><span class="sxs-lookup"><span data-stu-id="c082c-114">The root feature Sport has the msidbFeatureAttributesFollowParent bit set.</span></span>

<span data-ttu-id="c082c-115">Na árvore de recursos deste exemplo, esporte é o recurso raiz e um pai dos recursos de nada e de futebol.</span><span class="sxs-lookup"><span data-stu-id="c082c-115">In the feature tree of this example, Sport is the root feature and a parent of the Swimming and Football features.</span></span> <span data-ttu-id="c082c-116">Freestyle é um recurso filho de nada.</span><span class="sxs-lookup"><span data-stu-id="c082c-116">Freestyle is a child feature of Swimming.</span></span> <span data-ttu-id="c082c-117">TouchFootball é um recurso filho de futebol.</span><span class="sxs-lookup"><span data-stu-id="c082c-117">TouchFootball is a child feature of Football.</span></span>

<span data-ttu-id="c082c-118">[Tabela de recursos](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c082c-118">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="c082c-119">Recurso</span><span class="sxs-lookup"><span data-stu-id="c082c-119">Feature</span></span>       | <span data-ttu-id="c082c-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="c082c-120">Attributes</span></span> | <span data-ttu-id="c082c-121">Pai do recurso \_</span><span class="sxs-lookup"><span data-stu-id="c082c-121">Feature\_Parent</span></span> |
|---------------|------------|-----------------|
| <span data-ttu-id="c082c-122">Esporte</span><span class="sxs-lookup"><span data-stu-id="c082c-122">Sport</span></span>         | <span data-ttu-id="c082c-123">4</span><span class="sxs-lookup"><span data-stu-id="c082c-123">4</span></span>          | <span data-ttu-id="c082c-124">Esporte</span><span class="sxs-lookup"><span data-stu-id="c082c-124">Sport</span></span>           |
| <span data-ttu-id="c082c-125">Swimming</span><span class="sxs-lookup"><span data-stu-id="c082c-125">Swimming</span></span>      | <span data-ttu-id="c082c-126">1</span><span class="sxs-lookup"><span data-stu-id="c082c-126">1</span></span>          | <span data-ttu-id="c082c-127">Esporte</span><span class="sxs-lookup"><span data-stu-id="c082c-127">Sport</span></span>           |
| <span data-ttu-id="c082c-128">Comemorar</span><span class="sxs-lookup"><span data-stu-id="c082c-128">Football</span></span>      | <span data-ttu-id="c082c-129">4</span><span class="sxs-lookup"><span data-stu-id="c082c-129">4</span></span>          | <span data-ttu-id="c082c-130">Esporte</span><span class="sxs-lookup"><span data-stu-id="c082c-130">Sport</span></span>           |
| <span data-ttu-id="c082c-131">Freestyle</span><span class="sxs-lookup"><span data-stu-id="c082c-131">Freestyle</span></span>     | <span data-ttu-id="c082c-132">1</span><span class="sxs-lookup"><span data-stu-id="c082c-132">1</span></span>          | <span data-ttu-id="c082c-133">Swimming</span><span class="sxs-lookup"><span data-stu-id="c082c-133">Swimming</span></span>        |
| <span data-ttu-id="c082c-134">TouchFootball</span><span class="sxs-lookup"><span data-stu-id="c082c-134">TouchFootball</span></span> | <span data-ttu-id="c082c-135">4</span><span class="sxs-lookup"><span data-stu-id="c082c-135">4</span></span>          | <span data-ttu-id="c082c-136">Comemorar</span><span class="sxs-lookup"><span data-stu-id="c082c-136">Football</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c082c-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c082c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c082c-138">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="c082c-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



