---
title: Gerando informações de erro
description: Se um servidor ou aplicativo encontrar um erro fatal ao ser chamado por meio de RPC, ele deverá indicar ao tempo de execução de RPC que encontrou uma falha e, idealmente, adicionar informações sobre a falha para facilitar a solução de problemas.
ms.assetid: 6658c387-94df-4d85-9749-53858f9e0f5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b06a13e932034e6840479443e0b78f4c322c0b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759597"
---
# <a name="generating-error-information"></a>Gerando informações de erro

Se um servidor ou aplicativo encontrar um erro fatal ao ser chamado por meio de RPC, ele deverá indicar ao tempo de execução de RPC que encontrou uma falha e, idealmente, adicionar informações sobre a falha para facilitar a solução de problemas.

## <a name="indicating-fatal-errors-to-the-rpc-run-time"></a>Indicando erros fatais para o tempo de execução de RPC

Para indicar uma falha ao tempo de execução RPC, chame a função [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) enquanto estiver no thread RPC em que a exceção foi chamada ou [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) se estiver processando a chamada de forma assíncrona em outro thread. Retornar um código de erro da rotina de servidor, como a rotina de Gerenciador, não é suficiente – de acordo com a especificação RPC, o valor de retorno da função não tem semântica de erro no servidor, independentemente das configurações de arquivo IDL/ACF.

Quando ocorrer um erro fatal em seu componente, execute qualquer limpeza considerada necessária e, em seguida, chame a função [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) com o código de erro. A única diferença entre **RpcRaiseException** e retornar um código de erro é quando o **RpcRaiseException** é chamado, os parâmetros de saída não são empacotados. Isso geralmente é uma vantagem, pois evitar que parâmetros de saída não inicializados se torne desnecessário.

## <a name="generating-additional-extended-error-information"></a>Gerando informações adicionais de erro estendido

Assim como o tempo de execução de RPC cria uma cadeia de registros de erro, seu servidor ou aplicativo pode adicionar seus próprios registros à cadeia. Essa abordagem geralmente ajuda no processo de solução de problemas. Por exemplo, um servidor pode tentar abrir um determinado arquivo e receber um erro de arquivo não encontrado. Simplesmente retornar o erro 2 não seria útil para determinar qual arquivo está ausente.

Em vez disso, o servidor poderia chamar a função [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) e fornecer um parâmetro de cadeia de caracteres, ANSI ou Unicode, no registro de erro indicando o caminho completo do arquivo que estava procurando. Quando todas essas informações aparecem na tela do usuário em um computador remoto, a solução de problemas torna-se trivial; uma verificação simples de se o arquivo existe pode ser feita, especialmente porque o nome do computador em questão já foi fornecido pelo tempo de execução RPC.

A chamada de função [**RpcErrorAddRecord**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerroraddrecord) poderá falhar se memória suficiente não estiver disponível, mesmo que exija apenas alguns bytes de espaço de heap. Além disso, os registros adicionados pelo **RpcErrorAddRecord** são acumulados em um determinado thread. O tempo de execução normalmente limpa esses registros antes de chamar a rotina do servidor, mas se as informações de erro estendidas forem usadas fora do RPC, tome cuidado com a limpeza do erro estendido acumulado no thread chamando [**RpcErrorClearInformation**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcerrorclearinformation).

 

 




