---
description: O IP Conferencing MSP implementa várias interfaces específicas do provedor para o controle de participante. Essas interfaces são expostas no objeto de chamada, se este MSP estiver associado à chamada.
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: Interfaces MSP IPConf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091318"
---
# <a name="ipconf-msp-interfaces"></a>Interfaces MSP IPConf

\[ As interfaces IPConf MSP não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O IP Conferencing MSP implementa várias interfaces específicas do provedor para o controle de participante. Essas interfaces são expostas no objeto de chamada, se este MSP estiver associado à chamada.

As interfaces [**ITParticipantEvent**](itparticipantevent.md) e [**IEnumParticipant**](ienumparticipant.md) são objetos autônomos e são listadas aqui para conveniência de referência.



| Interface                                            | Descrição                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMulticastControl**](imulticastcontrol.md)       | Permite que um aplicativo defina e obtenha o modo de loopback [**( \_ \_ modo de loopback multicast**](multicast-loopback-mode.md)) para um objeto de conferência multicast. |
| [**ITParticipant**](itparticipant.md)               | Permite que um aplicativo recupere informações sobre os participantes da conferência e obtenha ponteiros para os fluxos associados a esses participantes.             |
| [**ITParticipantControl**](itparticipantcontrol.md) | Permite que um aplicativo recupere ponteiros para os participantes em uma conferência.                                                                           |
| [**ITParticipantEvent**](itparticipantevent.md)     | Permite que um aplicativo recupere informações de evento relacionadas a um participante da conferência.                                                                  |
| [**IEnumParticipant**](ienumparticipant.md)         | Enumera [**ITParticipant**](itparticipant.md).                                                                                                        |



 

 

 



