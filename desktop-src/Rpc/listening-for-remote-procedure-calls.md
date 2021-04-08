---
title: Ouvindo chamadas de procedimento remoto
description: Depois que um programa de servidor registra suas informações de associação e anuncia sua presença em um banco de dados de serviço de nome, ele pode começar a escutar o ponto de extremidade para chamadas de procedimento remoto.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004804"
---
# <a name="listening-for-remote-procedure-calls"></a>Ouvindo chamadas de procedimento remoto

Depois que um programa de servidor registra suas informações de associação e anuncia sua presença em um banco de dados de serviço de nome, ele pode começar a escutar o ponto de extremidade para chamadas de procedimento remoto. Os programas de servidor chamam a função [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para monitorar pontos de extremidade para invocações de cliente de procedimentos remotos.

A especificação DCE de [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indica que ele não deve retornar até que uma função no programa de servidor chame [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening). A implementação RPC da Microsoft do **RpcServerListen** usa dois parâmetros que não aparecem na especificação do DCE: *DontWait* e *MinimumCallThreads*. O programa do servidor pode passar um valor diferente de zero para o parâmetro *DontWait* . Se tiver, a função **RpcServerListen** retornará imediatamente. Use a rotina [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) para executar a operação de espera geralmente associada a **RpcServerListen**.

 

 




