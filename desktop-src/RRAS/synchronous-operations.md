---
title: Operações síncronas
description: Quando RasDial é invocado como uma operação síncrona, a função não retorna até que a conexão tenha sido estabelecida ou ocorra um erro.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006002"
---
# <a name="synchronous-operations"></a>Operações síncronas

Quando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) é invocado como uma operação síncrona, a função não retorna até que a conexão tenha sido estabelecida ou ocorra um erro. O modo síncrono fornece uma maneira simples para um cliente RAS estabelecer uma conexão. O cliente pode simplesmente chamar **RasDial**, aguardar a função retornar e, em seguida, chamar a função [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para determinar se a operação de conexão foi bem-sucedida. Depois que a conexão tiver sido estabelecida, o aplicativo cliente poderá ser encerrado sem interromper a conexão. Se ocorrer um erro, o aplicativo cliente deverá [desligar a operação de conexão antes de](disconnecting.md) encerrar.

A desvantagem do modo síncrono é que o cliente não recebe notificações de progresso à medida que a operação de conexão continua. Como solução alternativa para essa falta de notificações de progresso, um cliente de modo síncrono pode usar um thread separado que chama [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para sondar e exibir o estado atual. No entanto, para clientes RAS que desejam receber informações de progresso, a técnica preferida é invocar [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de forma assíncrona.

 

 




