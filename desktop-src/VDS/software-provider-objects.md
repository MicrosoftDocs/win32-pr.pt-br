---
description: Objetos de provedor de software
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Objetos de provedor de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "103837547"
---
# <a name="software-provider-objects"></a>Objetos de provedor de software

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Objetos de provedor de software modelam dispositivos físicos, como discos IDE e CD-ROMs, e elementos virtuais como pacotes, volumes e plexes de volume. A ilustração a seguir mostra a relação entre o objeto de provedor e o conjunto de objetos de provedor de software, bem como a relação entre os vários objetos de provedor de software.

![Diagrama que mostra a relação entre um ' provedor ' e objetos de provedor de software, como ' Pack ' e ' volume '.](images/vdsswobjects.png)

Um objeto de provedor pode conter zero ou mais pacotes. Um objeto de pacote pode conter zero ou mais discos e volumes. Um volume que consiste em pelo menos um plex de volume e cada Plex de volume pode ser mapeado para um ou mais discos, dependendo do tipo de plex. O VDS gerencia discos não alocados diretamente, sem um contêiner de pacote. Os tópicos restantes desta seção descrevem os objetos de pacote, disco, volume e Plex de volume.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> </dl>

 

 
