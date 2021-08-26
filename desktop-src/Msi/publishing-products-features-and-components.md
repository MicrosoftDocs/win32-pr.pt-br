---
description: Para publicar um produto, componente ou recurso, use uma das ações de publicação.
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: Publicando produtos, recursos e componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dd62e080cf58188405e20d1fd69507f849dd37ceddd01eaf1f4bbe7c59ea76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041986"
---
# <a name="publishing-products-features-and-components"></a>Publicando produtos, recursos e componentes

Para [publicar](components-and-features.md) um produto, componente ou recurso, use uma das ações de publicação. A [ação PublishProduct](publishproduct-action.md) registra as informações do produto com o sistema. Depois de executar a ação PublishProduct, publique os componentes com a [ação PublishComponents](publishcomponents-action.md), que por sua vez usa a [tabela PublishComponent](publishcomponent-table.md) para determinar os componentes definidos como anunciados. Para publicar por recurso, invoque a [ação PublishFeatures](publishfeatures-action.md). Essa ação usa a [tabela FeatureComponents](featurecomponents-table.md) como dados para resolver quais recursos são anunciados.

Há também duas ações correspondentes que despublicam um recurso ou um componente: a [ação UnpublishComponents](unpublishcomponents-action.md) e a [ação UnpublishFeatures](unpublishfeatures-action.md).

 

 



