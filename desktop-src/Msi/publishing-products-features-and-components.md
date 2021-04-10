---
description: Para publicar um produto, componente ou recurso, use uma das ações de publicação.
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: Publicando produtos, recursos e componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdd8c8445491646399c7d118a69ae497d27faff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169393"
---
# <a name="publishing-products-features-and-components"></a><span data-ttu-id="9b09c-103">Publicando produtos, recursos e componentes</span><span class="sxs-lookup"><span data-stu-id="9b09c-103">Publishing Products, Features, and Components</span></span>

<span data-ttu-id="9b09c-104">Para [publicar](components-and-features.md) um produto, componente ou recurso, use uma das ações de publicação.</span><span class="sxs-lookup"><span data-stu-id="9b09c-104">To [publish](components-and-features.md) a product, component, or feature, use one of the publishing actions.</span></span> <span data-ttu-id="9b09c-105">A [ação PublishProduct](publishproduct-action.md) registra as informações do produto com o sistema.</span><span class="sxs-lookup"><span data-stu-id="9b09c-105">The [PublishProduct action](publishproduct-action.md) registers the product information with the system.</span></span> <span data-ttu-id="9b09c-106">Depois de executar a ação PublishProduct, publique os componentes com a [ação PublishComponents](publishcomponents-action.md), que por sua vez usa a [tabela PublishComponent](publishcomponent-table.md) para determinar os componentes definidos como anunciados.</span><span class="sxs-lookup"><span data-stu-id="9b09c-106">After executing the PublishProduct action, publish the components with the [PublishComponents action](publishcomponents-action.md), which in turn uses the [PublishComponent table](publishcomponent-table.md) to determine the components that are set as advertised.</span></span> <span data-ttu-id="9b09c-107">Para publicar por recurso, invoque a [ação PublishFeatures](publishfeatures-action.md).</span><span class="sxs-lookup"><span data-stu-id="9b09c-107">To publish on a per-feature basis, invoke the [PublishFeatures action](publishfeatures-action.md).</span></span> <span data-ttu-id="9b09c-108">Essa ação usa a [tabela FeatureComponents](featurecomponents-table.md) como dados para resolver quais recursos são anunciados.</span><span class="sxs-lookup"><span data-stu-id="9b09c-108">This action uses the [FeatureComponents table](featurecomponents-table.md) as data to resolve which features are advertised.</span></span>

<span data-ttu-id="9b09c-109">Há também duas ações correspondentes que despublicam um recurso ou um componente: a [ação UnpublishComponents](unpublishcomponents-action.md) e a [ação UnpublishFeatures](unpublishfeatures-action.md).</span><span class="sxs-lookup"><span data-stu-id="9b09c-109">There are also two corresponding actions that unpublish a feature or a component: the [UnpublishComponents action](unpublishcomponents-action.md) and the [UnpublishFeatures action](unpublishfeatures-action.md).</span></span>

 

 



