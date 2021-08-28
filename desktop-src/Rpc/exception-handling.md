---
title: Tratamento de exceção (RPC)
description: O RPC usa a mesma abordagem para tratamento de exceções que a API Windows.
ms.assetid: 7133d3f4-ed84-4cde-bc77-88e73ced9073
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b88cea6e1a2046b957baf5afe72be4cbec9f82d7da32215d2434fbf681f64d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080866"
---
# <a name="exception-handling-rpc"></a>Tratamento de exceção (RPC)

O RPC usa a mesma abordagem para tratamento de exceções que a API Windows.

A [**estrutura RpcTryFinally**](rpctryfinally.md)  /  [**RpcFinally**](/previous-versions/aa375699(v=vs.80))  /  [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) é equivalente à Windows **instrução try-finally.** O constructo de exceção [**RPC RpcTryExcept**](rpctryexcept.md)  /  [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)  /  [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) é equivalente à Windows **instrução try-except.**

Quando você usa os manipuladores de exceção RPC, o código-fonte do lado do cliente é portátil. Os diferentes arquivos de header RPC fornecidos para cada plataforma resolvem as macros **RpcTry** e [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) para cada plataforma. No ambiente Windows, essas macros mapeiam diretamente para o Windows **instruções try-finally** **e try-except.** Em outros ambientes, essas macros são mapeáveis para outras implementações específicas da plataforma de manipuladores de exceção.

As possíveis exceções ativas por essas estruturas incluem o conjunto de códigos de erro retornados pelas funções RPC com os prefixos RPC S e RPC X e o conjunto de exceções retornado \_ \_ por \_ Windows. Para obter detalhes, consulte [Valores de retorno RPC](rpc-return-values.md).

Embora as macros **RpcTry** e [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) forneçam uma maneira personalizável de lidar com exceções, no Windows Vista e em versões posteriores do Windows, [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) é a maneira recomendada de lidar com exceções. Ele não exige que filtros personalizados sejam gravados para capturar muitas das exceções estruturadas mais comuns; no entanto, os filtros de exceção personalizados ainda **exigem RpcExcept.**

Exceções que ocorrem no aplicativo de servidor, no stub do servidor e na biblioteca de tempo de run-time do servidor (acima da camada de transporte) são propagadas para o cliente. Nenhuma exceção é propagada do nível de transporte do servidor. O método recomendado para uma rotina de servidor retornar erros para o tempo de executar RPC é lançar uma exceção. Uma rotina de servidor pode usar qualquer método apropriado para comunicar erros entre rotinas de servidor, mas se encontrar um erro que impeça a execução do procedimento remoto, ele deverá aumentá-lo após a limpeza e antes de retornar ao tempo de execução RPC, em vez de retornar um valor para rPC que apenas a rotina do servidor reconheça como um erro.

A figura a seguir mostra como as exceções são retornadas do servidor para o cliente.

![exceções são retornadas do servidor para o cliente por meio do respectivo runtime rpc de cada componente](images/prog-a20.png)

Os manipuladores de exceção RPC diferem ligeiramente das **macros** TRY, **FINALLY** e **CATCH** do OSF-DCE (Open Software Foundation-Distributed Computing Environment). Vários fornecedores fornecem arquivos de inclusão que mapeiam as funções RPC osF-DCE para as funções RPC da Microsoft, incluindo **TRY,** **CATCH,** **CATCH** \_ **ALL** e **ENDTRY**. Esses arquivos de header também mapeiam os códigos de erro RPC S para as contrapartes de exceção \_ \_ \* osF-DCE, rpc \_ s \_ \* e mapeiam \_ \_ \* \_ \_ \* códigos de erro RPC X para rpc x . Para portabilidade do OSF-DCE, use estes arquivos de inclusão. Para obter mais informações sobre os manipuladores de exceção RPC, consulte [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter), [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept), [**RpcFinally**](/previous-versions/aa375699(v=vs.80)). Para obter mais informações sobre os manipuladores Windows de exceção, consulte [Tratamento de exceções estruturadas.](/windows/desktop/Debug/structured-exception-handling)

 

 
