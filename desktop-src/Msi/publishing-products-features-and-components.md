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
# <a name="publishing-products-features-and-components"></a>Publicando produtos, recursos e componentes

Para [publicar](components-and-features.md) um produto, componente ou recurso, use uma das ações de publicação. A [ação PublishProduct](publishproduct-action.md) registra as informações do produto com o sistema. Depois de executar a ação PublishProduct, publique os componentes com a [ação PublishComponents](publishcomponents-action.md), que por sua vez usa a [tabela PublishComponent](publishcomponent-table.md) para determinar os componentes definidos como anunciados. Para publicar por recurso, invoque a [ação PublishFeatures](publishfeatures-action.md). Essa ação usa a [tabela FeatureComponents](featurecomponents-table.md) como dados para resolver quais recursos são anunciados.

Há também duas ações correspondentes que despublicam um recurso ou um componente: a [ação UnpublishComponents](unpublishcomponents-action.md) e a [ação UnpublishFeatures](unpublishfeatures-action.md).

 

 



