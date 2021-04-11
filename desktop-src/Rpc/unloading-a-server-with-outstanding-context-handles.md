---
title: Descarregando um servidor com identificadores de contexto pendentes
description: Tradicionalmente, o descarregamento de uma DLL que serviços chamadas RPC usando identificadores de contexto, sem antes parar o processo de hospedagem, tem sido problemático.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160334"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a>Descarregando um servidor com identificadores de contexto pendentes

Tradicionalmente, o descarregamento de uma DLL que serviços chamadas RPC usando identificadores de contexto, sem antes parar o processo de hospedagem, tem sido problemático. Isso ocorre porque a rotina de execução não é mais válida quando a DLL está sendo descarregada. Quando um cliente com um identificador de contexto aberto anteriormente falha e o tempo de execução de RPC tenta fechar o identificador de contexto, sua tentativa de chamar o acesso de rotina de execução é violado e o servidor falha.

A partir do Windows XP, uma nova API chamada [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) foi adicionada. **RpcServerUnregisterIfEx** fecha identificadores de contexto abertos pela interface que está sendo cancelada no registro; a função [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) não. O uso de **RpcServerUnregisterIfEx** não é necessário quando todo o processo é desligado, mas é necessário se uma ou mais DLLs que hospedam as rotinas de execução forem descarregadas enquanto houver identificadores de contexto pendentes.

 

 




