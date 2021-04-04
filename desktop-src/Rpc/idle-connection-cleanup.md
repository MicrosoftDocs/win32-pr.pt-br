---
title: Limpeza de conexão ociosa
description: Por padrão, as conexões no pool de threads não são fechadas até que toda a associação seja desligada.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822371"
---
# <a name="idle-connection-cleanup"></a>Limpeza de conexão ociosa

Por padrão, as conexões no pool de threads não são fechadas até que toda a associação seja desligada. Essa política permite que clientes com um grande número de threads ou identidades de segurança façam chamadas RPC para o servidor de maneira eficiente. A desvantagem é que uma quantidade inordenada de recursos pode ser confirmada para manter essas conexões. Para gerenciar o processo, o RPC fornece a função [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) . Essa função habilita a limpeza de conexão ociosa; o cliente verifica periodicamente o pool de conexões e fecha as conexões que não foram usadas recentemente. Se a associação tiver mantido identificadores de contexto, a limpeza de conexão ociosa fechará todas as conexões ociosas, mas garantirá que pelo menos uma conexão seja deixada aberta, mesmo se a conexão estiver ociosa (caso contrário, o servidor obterá a execução do identificador de contexto). Se a associação não mantiver identificadores de contexto, a limpeza de conexão ociosa fechará todas as conexões ociosas, mesmo que isso não deixe nenhuma conexão no pool.

No Windows XP, o tempo de execução RPC controla o número de conexões abertas em uma associação e ativa automaticamente a limpeza de conexão ociosa se o número de conexões em qualquer associação exceder um determinado limite.

 

 




