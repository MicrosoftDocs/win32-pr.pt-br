---
title: Operações síncronas
description: Quando RasDial é invocado como uma operação síncrona, a função não retorna até que a conexão seja estabelecida ou ocorra um erro.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c923a22758e7d6b9563cde9e4c9b2ce6036afa47f85116c0c18ed523996e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025606"
---
# <a name="synchronous-operations"></a>Operações síncronas

Quando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) é invocado como uma operação síncrona, a função não retorna até que a conexão seja estabelecida ou ocorra um erro. O modo síncrono fornece uma maneira simples para um cliente RAS estabelecer uma conexão. O cliente pode simplesmente chamar **RasDial**, aguardar o retorno da função e, em seguida, chamar a [**função RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para determinar se a operação de conexão foi bem-sucedida. Depois que a conexão tiver sido estabelecida, o aplicativo cliente poderá terminar sem interromper a conexão. Se ocorrer um erro, o aplicativo cliente deverá [desligar a operação de conexão](disconnecting.md) antes de encerrar.

A desvantagem do modo síncrono é que o cliente não recebe notificações de progresso à medida que a operação de conexão continua. Como solução alternativa para essa falta de notificações de progresso, um cliente de modo síncrono pode usar um thread separado que chama [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para sondar e exibir o estado atual. No entanto, para clientes RAS que querem receber informações de progresso, a técnica preferencial é invocar [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de forma assíncrona.

 

 




