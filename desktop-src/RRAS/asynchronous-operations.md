---
title: Operações assíncronas
description: Quando RasDial é invocado como uma operação assíncrona, a função retorna imediatamente.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db434b7e6d080933e7e21de056f9af5ea7d57dfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364113"
---
# <a name="asynchronous-operations"></a>Operações assíncronas

Quando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) é invocado como uma operação assíncrona, a função retorna imediatamente. No modo assíncrono, a chamada **RasDial** deve especificar um [manipulador de notificação](notification-handlers.md) que o Gerenciador de conexões de acesso remoto usa para informar o cliente sempre que a operação de conexão mudar de estado ou ocorrer um erro.

O manipulador de notificação pode ser uma janela para receber mensagens ou uma função de retorno de chamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)ou [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) . O Gerenciador de conexões de acesso remoto faz suas notificações assíncronas no contexto do thread que fez a chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Por esse motivo, o thread de chamada não deve terminar até que a operação de conexão tenha sido estabelecida com êxito ou um erro ocorra. Como no modo síncrono, o aplicativo cliente pode ser encerrado com segurança depois que a conexão é estabelecida e deve [desligar a operação de conexão](disconnecting.md) se ocorrer um erro.

 

 




