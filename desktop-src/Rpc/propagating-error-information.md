---
title: Propagando informações de erro
description: A propagação de informações de erro estendidas permite que os servidores que recebem um \_ erro RPC S \_ ou qualquer outro código de erro, para permitir que o tempo de execução de RPC propaguem as informações recebidas para seus chamadores.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822894"
---
# <a name="propagating-error-information"></a>Propagando informações de erro

A propagação de informações de erro estendidas permite que os servidores que recebem um erro de RPC \_ S \_ \* ou qualquer outro código de erro, para permitir que o tempo de execução de RPC propaguem as informações recebidas para seus chamadores. Tudo o que o servidor deve fazer é chamar [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) ou [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) após encontrar um erro fatal. O tempo de execução do RPC se encarrega de encadear as informações de erro estendidas, se houver, fazendo com que o erro fatal relate o erro fatal em si, desde que o código de erro fornecido a **RpcRaiseException** ou **RpcAsyncAbortCall** seja o mesmo que o código de erro causando o erro fatal.

 

 




