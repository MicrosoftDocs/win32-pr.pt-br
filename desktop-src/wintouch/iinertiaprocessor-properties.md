---
title: Propriedades (IInertiaProcessor)
description: Esta seção contém as propriedades da interface IInertiaProcessor.
ms.assetid: 47fd1a49-8e14-4076-8ce6-f0c4917e8cf1
keywords:
- Windows Toque, interface IInertiaProcessor
- Windows Toque, propriedades da interface
- inércia, interface IInertiaProcessor
- Interface IInertiaProcessor, propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7825a97545c897f402144ce5113b79650b9eba31e19da7ceef1459ae6cdc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030120"
---
# <a name="properties-iinertiaprocessor"></a>Propriedades (IInertiaProcessor)

Esta seção contém as propriedades da interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .



| Propriedade                                                                               | Descrição                                                                                               |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InitialOriginX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginx)                             | Especifica o local horizontal inicial de um destino com Intertia.                                   |
| [**InitialOriginY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginy)                             | Especifica a localização vertical inicial de um destino com Intertia.                                     |
| [**InitialVelocityX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx)                         | Especifica o movimento inicial do objeto de destino no eixo horizontal.                              |
| [**InitialVelocityY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy)                         | Especifica a movimentação inicial do objeto de destino no eixo vertical.                                |
| [**InitialAngularVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity)             | Especifica a velocidade rotacional do destino quando o movimento começa.                                    |
| [**InitialExpansionVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity)         | Especifica a taxa de expansão RADIUS do destino quando o movimento começa.                               |
| [**InitialRadius**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialradius)                               | Especifica a distância da borda do destino até o seu centro antes de o objeto ser alterado.          |
| [**BoundaryLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryleft)                                 | Limita o quanto à esquerda da tela que o objeto de destino pode mover.                                 |
| [**BoundaryTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarytop)                                   | Limita a distância na parte superior da tela que o objeto de destino pode mover.                                  |
| [**BoundaryRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryright)                               | Limita a distância do lado direito da tela que o objeto de destino pode mover.                           |
| [**BoundaryBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarybottom)                             | Limita a distância na parte inferior da tela que o objeto de destino pode mover.                               |
| [**ElasticMarginLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginleft)                       | Especifica a região mais à esquerda para o ensaltamento do objeto de destino.                                            |
| [**ElasticMarginTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmargintop)                         | Especifica a região superior para o ensaltamento do objeto de destino.                                             |
| [**ElasticMarginRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginright)                     | Especifica a região mais à direita para o ensaltamento do objeto de destino.                                           |
| [**ElasticMarginBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginbottom)                   | Especifica a região inferior para o ensaltamento do objeto de destino.                                              |
| [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration)     | Especifica a taxa desejada que o objeto de destino deixará de rodar em radianos por MS.                |
| [**DesiredRotation**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation)                           | Especifica a distância desejada (em radianos) que um objeto será manipulado pelo processador inércia. |
| [**DesiredExpansion**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion)                         | Especifica a alteração desejada no raio médio do objeto.                                        |
| [**DesiredExpansionDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration) | Especifica a taxa na qual o objeto deixará de ser expandido.                                              |
| [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)                   | Especifica a taxa desejada na qual as operações de conversão serão desaceleradas.                              |
| [**DesiredDisplacement**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddisplacement)                   | Especifica a distância desejada que o objeto vai viajar.                                              |
| [**InitialTimestamp**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialtimestamp)                         | Especifica o carimbo de data/hora inicial para um objeto de destino que tem inércia.                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




