---
title: Descarregando um servidor com alças de contexto pendentes
description: Tradicionalmente, o descarregamento de uma DLL que serviços chama RPC usando alças de contexto, sem primeiro interromper o processo de hospedagem, tem sido problemático.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e581ff142c7453f4a9e9f1e40a5ab9991257a350a84b2fcb2ea08a0e157288cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010944"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a>Descarregando um servidor com alças de contexto pendentes

Tradicionalmente, o descarregamento de uma DLL que serviços chama RPC usando alças de contexto, sem primeiro interromper o processo de hospedagem, tem sido problemático. Isso acontece porque a rotina de run down não é mais válida quando a DLL está sendo descarregada. Quando um cliente com um alça de contexto aberto anteriormente falha e o tempo de executar RPC tenta fechar o handle de contexto, sua tentativa de chamar o acesso de rotina de run down viola e o servidor falha.

A partir Windows XP, uma nova API chamada [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) foi adicionada. **RpcServerUnregisterIfEx fecha** os alças de contexto abertos pela interface que está sendo não listada; A [**função RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) não. O **uso de RpcServerUnregisterIfEx** não é necessário quando todo o processo é desligado, mas é necessário se uma ou mais DLLs que hospedam as rotinas de run down são descarregadas enquanto existem alças de contexto pendentes.

 

 




