---
title: Tratamento de exceção (RPC)
description: O RPC usa a mesma abordagem para tratamento de exceções que a API do Windows.
ms.assetid: 7133d3f4-ed84-4cde-bc77-88e73ced9073
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25de594a648cddb70f26b42e8b0dbf1d6a9dd51d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454558"
---
# <a name="exception-handling-rpc"></a>Tratamento de exceção (RPC)

O RPC usa a mesma abordagem para tratamento de exceções que a API do Windows.

A estrutura [**RpcTryFinally**](rpctryfinally.md)  /  [**RpcFinally**](/previous-versions/aa375699(v=vs.80))  /  [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) é equivalente à instrução **try-finally** do Windows. A construção de exceção RPC [**RpcTryExcept**](rpctryexcept.md)  /  [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)  /  [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) é equivalente à instrução **try-Except** do Windows.

Quando você usa os manipuladores de exceção RPC, o código-fonte do lado do cliente é portátil. Os diferentes arquivos de cabeçalho RPC fornecidos para cada plataforma resolvem as macros **RpcTry** e [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) para cada plataforma. No ambiente do Windows, essas macros são mapeadas diretamente para as instruções **try-finally** e **try-Except** do Windows. Em outros ambientes, essas macros são mapeadas para outras implementações de manipuladores de exceção específicas da plataforma.

As possíveis exceções geradas por essas estruturas incluem o conjunto de códigos de erro retornados pelas funções RPC com os prefixos RPC \_ S \_ e RPC \_ X e o conjunto de exceções retornado pelo Windows. Para obter detalhes, consulte [valores de retorno de RPC](rpc-return-values.md).

Embora as macros **RpcTry** e [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) forneçam uma maneira independente de plataforma personalizável para lidar com exceções, no Windows Vista e em versões posteriores do Windows, o [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) é a maneira recomendada de lidar com exceções. Ele não exige que filtros personalizados sejam escritos para capturar muitas das exceções estruturadas mais comuns; no entanto, os filtros de exceção personalizados ainda exigem **RpcExcept**.

As exceções que ocorrem no aplicativo do servidor, no stub do servidor e na biblioteca de tempo de execução do servidor (acima da camada de transporte) são propagadas para o cliente. Nenhuma exceção é propagada do nível de transporte do servidor. O método recomendado para uma rotina de servidor retornar erros para o tempo de execução de RPC é gerar uma exceção. Uma rotina de servidor pode usar qualquer método apropriado para comunicar erros entre rotinas de servidor, mas se encontrar um erro que impeça a execução do procedimento remoto, ele deverá gerar uma exceção após a limpeza e antes de retornar ao tempo de execução de RPC, em vez de retornar um valor para RPC que apenas a rotina de servidor reconhece como erro.

A figura a seguir mostra como as exceções são retornadas do servidor para o cliente.

![as exceções são retornadas do servidor para o cliente por meio do respectivo tempo de execução RPC de cada componente](images/prog-a20.png)

Os manipuladores de exceção RPC diferem ligeiramente **das macros** de tratamento de exceção do uso-DCE (Foundation-Distributed software aberto), **por fim**, e **Catch**. Vários fornecedores fornecem arquivos de inclusão que mapeiam as funções RPC uso-DCE para as funções RPC da Microsoft, incluindo **try**, **Catch**, **Catch** \_ **All** e **ENDTRY**. Esses arquivos de cabeçalho também mapeiam os \_ códigos de erro RPC s \_ \* para as contrapartes de exceção uso-DCE, RPC \_ S \_ \* e mapeiam os \_ \_ \* códigos de erro RPC x para RPC \_ x \_ \* . Para portabilidade uso-DCE, use esses arquivos de inclusão. Para obter mais informações sobre os manipuladores de exceção RPC, consulte [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter), [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept), [**RpcFinally**](/previous-versions/aa375699(v=vs.80)). Para obter mais informações sobre os manipuladores de exceção do Windows, consulte [manipulação de exceção estruturada](/windows/desktop/Debug/structured-exception-handling).

 

 
