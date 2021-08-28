---
title: Recursos lado a lado
description: Os recursos lado a lado podem ser pensados como recursos lógicos grandes que usam pequenas quantidades de memória física.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73835d6603d1d8d7e708cd422e3991bb88ac1f91cebf016ccce36f2466270c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124084"
---
# <a name="tiled-resources"></a>Recursos lado a lado

Os recursos lado a lado podem ser pensados como recursos lógicos grandes que usam pequenas quantidades de memória física.

Esta seção descreve por que os recursos lado a lado são necessários e como você cria e usa recursos lado a lado.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Por que os recursos lado a lado são necessários?](why-are-tiled-resources-needed-.md)<br/>       | Os recursos lado a lado são necessários para que menos memória de GPU (unidade de processamento gráfico) seja perdida para armazenar regiões de superfícies que o aplicativo sabe que não serão acessadas e o hardware pode entender como filtrar entre blocos adjacentes.<br/>     |
| [Criando recursos lado a lado](creating-tiled-resources.md)<br/>                     | Os recursos lado a lado são criados especificando o sinalizador [**D3D11 \_ RESOURCE \_ MISC \_ TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) quando você cria um recurso.<br/>                                                                                          |
| [APIs de recursos lado a lado](tiled-resource-apis.md)<br/>                               | As APIs descritas nesta seção funcionam com recursos lado a lado e pool de blocos.<br/>                                                                                                                                                              |
| [Acesso de pipeline a recursos lado a lado](pipeline-access-to-tiled-resources.md)<br/> | Os recursos lado a lado podem ser usados em SRV (exibições de recurso de sombreador), exibições de destino de renderização (RTV), DSV (exibições de estêncil de profundidade) e UAV (exibições de acesso não organizado), bem como alguns pontos de associação em que as exibições não são usadas, como vinculações de buffer de vértice. <br/> |
| [Camadas de recursos de recursos lado a lado](tiled-resources-features-tiers.md)<br/>         | O Direct3D 11.2 expõe o suporte a recursos lado a lado em duas camadas com os valores [**D3D11 \_ TILED \_ RESOURCES \_ TIER.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) <br/>                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





