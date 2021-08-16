---
title: Propagando informações de erro
description: A propagação de informações de erro estendidas permite que os servidores que recebem um \_ erro RPC S \_ ou qualquer outro código de erro, para permitir que o tempo de execução de RPC propaguem as informações recebidas para seus chamadores.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510ecf011dbac01d2b4c931a463bebb3739a92322059eb3a7a342160c42a9e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927154"
---
# <a name="propagating-error-information"></a>Propagando informações de erro

A propagação de informações de erro estendidas permite que os servidores que recebem um erro de RPC \_ S \_ \* ou qualquer outro código de erro, para permitir que o tempo de execução de RPC propaguem as informações recebidas para seus chamadores. Tudo o que o servidor deve fazer é chamar [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) ou [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) após encontrar um erro fatal. O tempo de execução do RPC se encarrega de encadear as informações de erro estendidas, se houver, fazendo com que o erro fatal relate o erro fatal em si, desde que o código de erro fornecido a **RpcRaiseException** ou **RpcAsyncAbortCall** seja o mesmo que o código de erro causando o erro fatal.

 

 




