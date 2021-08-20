---
title: Considerações sobre segurança do ponto de controle
description: Ao criar um ponto de controle, você precisa levar em consideração os seguintes problemas de segurança.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85378d7f530177bb42a6751a13f643bad984e994ae65178c0ab06cd5ce4792a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126003"
---
# <a name="control-point-security-considerations"></a>Considerações sobre segurança do ponto de controle

Ao criar um ponto de controle, você precisa levar em consideração os seguintes problemas de segurança.

-   Todas as pesquisas de ponto de controle são enviadas por padrão com um TTL de 1. Isso significa que apenas dispositivos dentro da mesma sub-rede são descobertos. Você pode configurar um TTL mais alto no Registro.
-   A descrição do dispositivo e do serviço de um dispositivo só será baixada se ele estiver presente no mesmo dispositivo que enviou o comunicado do dispositivo.
-   Um dispositivo só recebe solicitações de controle e assinatura se suas URLs de controle e assinatura estão no mesmo dispositivo que enviou os comunicados do dispositivo.

 

 




