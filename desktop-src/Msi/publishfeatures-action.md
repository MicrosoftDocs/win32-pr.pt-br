---
description: A ação PublishFeatures grava o estado de cada recurso no registro do sistema.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Ação PublishFeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759210"
---
# <a name="publishfeatures-action"></a><span data-ttu-id="04e0f-103">Ação PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="04e0f-103">PublishFeatures Action</span></span>

<span data-ttu-id="04e0f-104">A ação PublishFeatures grava o estado de cada recurso no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="04e0f-104">The PublishFeatures action writes each feature's state into the system registry.</span></span> <span data-ttu-id="04e0f-105">O estado do recurso pode estar ausente, anunciado ou instalado.</span><span class="sxs-lookup"><span data-stu-id="04e0f-105">The feature state may be either absent, advertised, or installed.</span></span> <span data-ttu-id="04e0f-106">A ação PublishFeatures também grava o mapeamento de componente de recurso no registro do sistema para cada recurso instalado.</span><span class="sxs-lookup"><span data-stu-id="04e0f-106">The PublishFeatures action also writes the feature-component mapping into the system registry for each installed feature.</span></span>

<span data-ttu-id="04e0f-107">A ação PublishFeatures consulta a tabela [FeatureComponents](featurecomponents-table.md), a [tabela de recursos](feature-table.md)e a tabela de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="04e0f-107">The PublishFeatures action queries the [FeatureComponents table](featurecomponents-table.md), [Feature table](feature-table.md), and [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="04e0f-108">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="04e0f-108">Sequence Restrictions</span></span>

<span data-ttu-id="04e0f-109">A ação PublishFeatures deve vir antes de [PublishProduct](publishproduct-action.md).</span><span class="sxs-lookup"><span data-stu-id="04e0f-109">The PublishFeatures action must come before [PublishProduct](publishproduct-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="04e0f-110">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="04e0f-110">ActionData Messages</span></span>



| <span data-ttu-id="04e0f-111">Campo</span><span class="sxs-lookup"><span data-stu-id="04e0f-111">Field</span></span> | <span data-ttu-id="04e0f-112">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="04e0f-112">Description of action data</span></span>        |
|-------|-----------------------------------|
| <span data-ttu-id="04e0f-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="04e0f-113">\[1\]</span></span> | <span data-ttu-id="04e0f-114">Identificador do recurso anunciado.</span><span class="sxs-lookup"><span data-stu-id="04e0f-114">Identifier of advertised feature.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="04e0f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="04e0f-115">Remarks</span></span>

<span data-ttu-id="04e0f-116">A ação PublishFeatures publica a composição de todos os recursos selecionados para serem anunciados ou instalados.</span><span class="sxs-lookup"><span data-stu-id="04e0f-116">The PublishFeatures action publishes the composition of all features that are selected to be advertised or installed.</span></span>

 

 



