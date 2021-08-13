---
description: Objetos do provedor de hardware
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Objetos do provedor de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c0050b6a9754b25b6a5027d9470cb2fc46911bf4ab3ef852454d1f0698a1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125956"
---
# <a name="hardware-provider-objects"></a>Objetos do provedor de hardware

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O modelo de objeto VDS inclui um conjunto de objetos para consultar e configurar entidades de provedor de hardware. (Observe que, embora o VDS inclua um provedor de software, você deve comprar um provedor de hardware e o hardware associado separadamente para aproveitar os objetos do provedor de hardware.) Esses objetos de provedor de hardware representam dispositivos físicos (como subsistemas, unidades e controladores) e dispositivos virtuais (como LUNs e plexes lun).

Um provedor de hardware deve criar um objeto COM para cada dispositivo físico ou virtual.

A ilustração a seguir mostra a relação entre o objeto de provedor e o conjunto de objetos do provedor de hardware, bem como a relação entre os próprios objetos do provedor de hardware.

![Diagrama que mostra a relação entre 'Provider' e 'Subsystem', 'Controller', 'LUN', 'LUN plex', 'Drive' e 'Eixo'. ](images/vdshwobjects.png)

Um objeto de provedor pode conter qualquer número de subsistemas. Todos os provedores de hardware são capazes de gerenciar várias instâncias do mesmo modelo de subsistema. Muitos provedores de hardware também são capazes de gerenciar várias instâncias de modelos de subsistema diferentes. Um único computador pode hospedar qualquer número de provedores de hardware.

Um objeto de subsistema pode conter qualquer número de controladores e unidades e pode surgir qualquer número de LUNs. Um objeto LUN é composto por pelo menos um plex lun e cada lunplex é mapeado para uma ou mais unidades, dependendo do tipo de plex. Os objetos do controlador podem gerenciar a entrada/saída de dados para qualquer número de objetos LUN.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> </dl>

 

 
