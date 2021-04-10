---
title: Enviando a chamada para o programa do servidor
description: Depois que o tempo de execução RPC do lado do cliente tiver se conectado ao ponto de extremidade do servidor, ele marshalle os argumentos e os envia para o servidor.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Chamada de procedimento remoto RPC, tarefas, enviando a chamada para o servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292635"
---
# <a name="sending-the-call-to-the-server-program"></a>Enviando a chamada para o programa do servidor

Depois que o tempo de execução RPC do lado do cliente tiver se conectado ao ponto de extremidade do servidor, ele marshalle os argumentos e os envia para o servidor. O tempo de execução RPC do servidor fornece os argumentos marshalled para o stub que os desempacota e, em seguida, os passa para as rotinas do servidor. Quando as rotinas do servidor retornam, o stub pega \[ os \] parâmetros out e \[ in, out \] e Value de retorno, faz marshaling deles e envia os dados marshalled para o tempo de execução do RPC do servidor. O tempo de execução RPC envia os dados de volta para o cliente, em que o tempo de execução RPC do cliente os entrega para o stub do lado do cliente que os desempacota e os retorna ao chamador.

 

 




