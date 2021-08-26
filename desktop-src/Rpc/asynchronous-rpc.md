---
title: RPC assíncrono
description: A RPC (chamada de procedimento remoto) assíncrona é uma extensão da Microsoft que aborda várias limitações do modelo de RPC tradicional, conforme definido pelo uso-DCE (ambiente de computação distribuída) da Open Software Foundation.
ms.assetid: 2586c10e-8284-419f-a200-4f6b11953688
keywords:
- RPC de chamada de procedimento remoto, descrito, RPC assíncrono
- RPC assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f4a5f160054f78f0a5737993d1a030957af930ab036e73dbcea0a039125964
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023536"
---
# <a name="asynchronous-rpc"></a>RPC assíncrono

A RPC (chamada de procedimento remoto) assíncrona é uma extensão da Microsoft que aborda várias limitações do modelo de RPC tradicional, conforme definido pelo uso-DCE (ambiente de computação distribuído) da Open Software Foundation. O RPC assíncrono separa uma chamada de procedimento remoto de seu valor de retorno, que resolve as seguintes limitações de RPC tradicional e síncrono:

-   **Várias chamadas pendentes de um cliente de thread único.** No modelo de RPC tradicional, um cliente é bloqueado em uma chamada de procedimento remoto até que a chamada seja retornada. Isso impede que um cliente tenha várias chamadas pendentes, enquanto ainda tem seu thread disponível para realizar outro trabalho.
-   **Clientes lentos ou atrasados.** Um cliente lento para produzir dados pode querer fazer uma chamada de procedimento remoto com dados iniciais e, em seguida, fornecer dados adicionais conforme eles são produzidos. Isso não é possível com o RPC convencional (síncrono).
-   **Servidores lentos ou atrasados.** Uma chamada de procedimento remoto que leva muito tempo para ser concluída irá vincular o thread de expedição durante a tarefa. Com o RPC assíncrono, o servidor pode iniciar uma operação separada (assíncrona) para processar a solicitação e enviar de volta a resposta quando ela estiver disponível. O servidor também pode enviar a resposta incrementalmente conforme os resultados são disponibilizados sem a necessidade de vincular um thread de expedição durante a chamada remota. Ao tornar o aplicativo cliente assíncrono, você pode impedir que um servidor lento se inscreva de forma desnecessariamente um aplicativo cliente.
-   **Transferência de grandes quantidades de dados.** A transferência de grandes quantidades de dados entre o cliente e o servidor, especialmente em links lentos, se une tanto ao thread do cliente quanto ao thread do Gerenciador do servidor pela duração da transferência. Com RPC e pipes assíncronos, a transferência de dados pode ocorrer incrementalmente e sem impedir que o cliente ou o servidor execute outras tarefas.

Você aproveita os mecanismos de RPC assíncronos declarando funções com o \[ [](/windows/desktop/Midl/async) \] atributo Async. Como você faz essa declaração em um arquivo de configuração de atributo (ACF), não é necessário fazer nenhuma alteração no arquivo IDL (linguagem de definição de interface); o RPC assíncrono não tem nenhum efeito sobre o protocolo de conexão (como os dados são transmitidos entre o cliente e o servidor). Isso significa que os clientes síncronos e assíncronos podem se comunicar com um aplicativo de servidor assíncrono.

Esta seção apresenta uma visão geral de como desenvolver aplicativos distribuídos usando o RPC assíncrono. A visão geral é apresentada nas seguintes seções:

-   [Declarando funções assíncronas](declaring-asynchronous-functions.md)
-   [RPC assíncrono do lado do cliente](client-side-asynchronous-rpc.md)
-   [RPC assíncrono do lado do servidor](server-side-asynchronous-rpc.md)
-   [Causal ordenação de chamadas assíncronas](causal-ordering-of-asynchronous-calls.md)
-   [Tratamento de erro](error-handling.md)
-   [RPC assíncrono sobre o protocolo de pipe nomeado](asynchronous-rpc-over-the-named-pipe-protocol.md)
-   [Usando RPC assíncrono com pipes de DCE](using-asynchronous-rpc-with-dce-pipes.md)
-   [DCOM assíncrono](asynchronous-dcom.md)

 

 