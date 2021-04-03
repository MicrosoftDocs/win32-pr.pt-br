---
title: Considerações de segurança do ponto de controle
description: Ao criar um ponto de controle, você precisa levar em consideração os seguintes problemas de segurança.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916486"
---
# <a name="control-point-security-considerations"></a>Considerações de segurança do ponto de controle

Ao criar um ponto de controle, você precisa levar em consideração os seguintes problemas de segurança.

-   Todas as pesquisas de ponto de controle são enviadas por padrão com um TTL igual a 1. Isso significa que somente os dispositivos na mesma sub-rede são descobertos. Você pode configurar uma TTL mais alta no registro.
-   A descrição do dispositivo e do serviço de um dispositivo será baixada somente se estiver presente no mesmo dispositivo que enviou o comunicado do dispositivo.
-   Um dispositivo só receberá solicitações de controle e assinatura se suas URLs de controle e assinatura estiverem no mesmo dispositivo que enviou os anúncios do dispositivo.

 

 




