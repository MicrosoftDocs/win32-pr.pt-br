---
title: Recursos em ladrilho
description: Os recursos ao lado dos ladrilhos podem ser considerados como recursos lógicos grandes que usam pequenas quantidades de memória física.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c7e6aaf60f58f55274c9d7a135b9107933f640
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822334"
---
# <a name="tiled-resources"></a>Recursos em ladrilho

Os recursos ao lado dos ladrilhos podem ser considerados como recursos lógicos grandes que usam pequenas quantidades de memória física.

Esta seção descreve o motivo pelo qual os recursos do lado do xadrez são necessários e como você cria e usa recursos em ladrilho.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Por que os recursos do lado do xadrez são necessários?](why-are-tiled-resources-needed-.md)<br/>       | Os recursos do lado do ladrilho são necessários, portanto, menos memória de GPU (unidade de processamento gráfico) é desperdiçada armazenando regiões de superfícies que o aplicativo sabe que não será acessado, e o hardware pode entender como filtrar por blocos adjacentes.<br/>     |
| [Criando recursos em ladrilhos](creating-tiled-resources.md)<br/>                     | Os recursos em ladrilho são criados especificando-se o sinalizador de [**\_ \_ \_ lado diverso do recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) ao criar um recurso.<br/>                                                                                          |
| [APIs de recursos de lado](tiled-resource-apis.md)<br/>                               | As APIs descritas nesta seção funcionam com os recursos de lado e o pool de blocos.<br/>                                                                                                                                                              |
| [Acesso ao pipeline para recursos lado a lado](pipeline-access-to-tiled-resources.md)<br/> | Os recursos do lado do xadrez podem ser usados em modos de exibição de recurso de sombreador (SRV), exibições de destino de renderização (RTV), exibições de estêncil de profundidade (DSV) e exibições de acesso não ordenado (UAV), bem como alguns pontos de ligação em que as exibições não são usadas, como associações de buffer de vértice. <br/> |
| [Recursos de azulejos recursos camadas](tiled-resources-features-tiers.md)<br/>         | O Direct3D 11,2 expõe os recursos com suporte de ladrilhos em duas camadas com os valores de [**\_ \_ \_ camada de recursos lado**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) -a-D3D11. <br/>                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





