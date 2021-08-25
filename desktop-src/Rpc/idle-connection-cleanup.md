---
title: Limpeza de conexão ociosa
description: Por padrão, as conexões no pool de threads não são fechadas até que toda a associação seja encerrada.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc7a7d4cefcead53e9b92678867cd76ceb6fab7f1ab5f1a573cf75378cf2a5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020796"
---
# <a name="idle-connection-cleanup"></a>Limpeza de conexão ociosa

Por padrão, as conexões no pool de threads não são fechadas até que toda a associação seja encerrada. Essa política permite que clientes com um grande número de threads ou identidades de segurança façam chamadas RPC para o servidor de maneira eficiente. A desvantagem é que uma quantidade excessiva de recursos pode ser comprometida para manter essas conexões. Para gerenciar o processo, o RPC fornece a [**função RpcMgmtEnableIdleCleanup.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) Essa função permite a limpeza de conexão ociosa; O cliente verifica periodicamente o pool de conexões e fecha conexões que não foram usadas recentemente. Se a associação tiver mantido os controles de contexto, a limpeza de conexão ociosa fechará todas as conexões ociosas, mas garantirá que pelo menos uma conexão seja deixada aberta, mesmo se a conexão estiver ociosa (caso contrário, o servidor obtém as insutenções do alça de contexto). Se a associação não tiver mantido os controles de contexto, a limpeza de conexão ociosa fechará todas as conexões ociosas, mesmo que isso não deixe nenhuma conexão no pool.

No Windows XP, o tempo de executar RPC mantém o controle do número de conexões abertas em uma associação e automaticamente liga a limpeza de conexão ociosa se o número de conexões em qualquer associação exceder um determinado limite.

 

 




