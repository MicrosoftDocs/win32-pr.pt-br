---
description: Objetos de provedor de hardware
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: Objetos de provedor de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1aaebf61e97487b48a6b8bf0dbd91cc6aa3e0bd
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105770588"
---
# <a name="hardware-provider-objects"></a>Objetos de provedor de hardware

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O modelo de objeto do VDS inclui um conjunto de objetos para consultar e configurar entidades de provedor de hardware. (Observe que, embora o VDS inclua um provedor de software, você deve adquirir um provedor de hardware e o hardware associado separadamente para tirar proveito dos objetos de provedor de hardware.) Esses objetos de provedor de hardware representam dispositivos físicos (como subsistemas, unidades e controladores) e dispositivos virtuais (como LUNs e plexes de LUN).

Um provedor de hardware deve criar um objeto COM para cada dispositivo físico ou virtual.

A ilustração a seguir mostra a relação entre o objeto de provedor e o conjunto de objetos de provedor de hardware, bem como a relação entre os vários objetos de provedor de hardware em si.

![Diagrama que mostra a relação entre o ' provedor ' e o ' subsistema ', ' controlador ', ' LUN ', ' LUN Plex ', ' unidade ' e ' eixo '. ](images/vdshwobjects.png)

Um objeto de provedor pode conter qualquer número de subsistemas. Todos os provedores de hardware são capazes de gerenciar várias instâncias do mesmo modelo de subsistema. Muitos provedores de hardware também são capazes de gerenciar várias instâncias de diferentes modelos de subsistema. Um único computador pode hospedar qualquer número de provedores de hardware.

Um objeto de subsistema pode conter qualquer número de controladores e unidades e pode trazer qualquer número de LUNs. Um objeto de LUN é composto de pelo menos um plex de LUN e cada Plex de LUN é mapeado para uma ou mais unidades, dependendo do tipo de plex. Os objetos do controlador podem gerenciar a entrada/saída de dados para qualquer número de objetos de LUN.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> </dl>

 

 
