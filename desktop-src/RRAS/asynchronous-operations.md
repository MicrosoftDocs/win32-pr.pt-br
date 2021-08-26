---
title: Operações assíncronas
description: Quando RasDial é invocado como uma operação assíncrona, a função retorna imediatamente.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db03b1d9d3c98e84bc9a2f4fd80ec7206d9a4524608cdbc96cca83f89d0ea00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030556"
---
# <a name="asynchronous-operations"></a>Operações assíncronas

Quando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) é invocado como uma operação assíncrona, a função retorna imediatamente. No modo assíncrono, a chamada **RasDial** deve especificar um [manipulador de notificação](notification-handlers.md) que o Gerenciador de conexões de acesso remoto usa para informar o cliente sempre que a operação de conexão mudar de estado ou ocorrer um erro.

O manipulador de notificação pode ser uma janela para receber mensagens ou uma função de retorno de chamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)ou [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) . O Gerenciador de conexões de acesso remoto faz suas notificações assíncronas no contexto do thread que fez a chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Por esse motivo, o thread de chamada não deve terminar até que a operação de conexão tenha sido estabelecida com êxito ou um erro ocorra. Como no modo síncrono, o aplicativo cliente pode ser encerrado com segurança depois que a conexão é estabelecida e deve [desligar a operação de conexão](disconnecting.md) se ocorrer um erro.

 

 




