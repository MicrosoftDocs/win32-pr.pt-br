---
title: Implementando um dispositivo hospedado
description: O host do dispositivo com tecnologia UPnP implementa a descoberta, a descrição, o controle e o evento dos protocolos UPnP principais.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fd12788c40d21dc84e896f1aba83085b440b86fbb54b68b4fbcfddbbe910c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008046"
---
# <a name="implementing-a-hosted-device"></a>Implementando um dispositivo hospedado

O host do dispositivo com tecnologia UPnP implementa os principais protocolos UPnP: descoberta, descrição, controle e eventos. O desenvolvedor que implementa um dispositivo hospedado só precisa fornecer:

-   Uma descrição do dispositivo e seus serviços.
-   Uma implementação da funcionalidade do dispositivo.

Por exemplo, o desenvolvedor de um dispositivo de relógio deve fornecer descrições de dispositivo e serviço baseadas em UPnP para ele e uma implementação das funções de relógio (como manter o tempo, definir o tempo e responder a consultas para a hora atual). O host do dispositivo:

-   Anuncia o dispositivo de acordo com o protocolo de descoberta UPnP.
-   Responde a consultas para a descrição do dispositivo.
-   Roteia solicitações de controle para a parte do código do dispositivo que implementa as funções de relógio.
-   Mantém assinaturas de evento para serviços.
-   Envia notificações de eventos aos assinantes quando o estado do serviço é alterado.

 

 




