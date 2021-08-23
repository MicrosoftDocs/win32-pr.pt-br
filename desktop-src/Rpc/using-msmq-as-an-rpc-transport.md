---
title: Usando o MSMQ como um transporte RPC
description: O subsistema RPC dá suporte ao uso do MSMQ como um transporte em modos síncronos e assíncronos.
ms.assetid: c3f96a91-b7bb-4c2a-8699-2100324af165
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab18f4476815929e8a7e6fb4e4a1eef0a4e4e34754ac134f023c8551899e0138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010674"
---
# <a name="using-msmq-as-an-rpc-transport"></a>Usando o MSMQ como um transporte RPC

O subsistema RPC dá suporte ao uso do MSMQ como um transporte em modos síncronos e assíncronos.

O modo síncrono usa chamadas de procedimento remoto convencionais. Essas chamadas usam pontos de extremidade bem conhecidos e o transporte de fila de mensagens, o [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq), como o protocolo de transporte. No modo síncrono, os procedimentos remotos podem ter \[ parâmetros [de entrada](/windows/desktop/Midl/in) \] e \[ [saída](/windows/desktop/Midl/out-idl) \] e podem usar os serviços de segurança RPC padrão. O subsistema RPC cria uma fila de resposta para chamadas remotas que contêm parâmetros de **\[ saída \]** . O modo síncrono é útil para aplicativos em que o cliente precisa receber dados do servidor. A principal limitação desse modo é que, assim como ocorre com chamadas de procedimento remoto convencionais, o cliente e o servidor devem estar em execução e permanecer em execução durante a chamada.

O modo assíncrono permite que os aplicativos cliente façam chamadas para o servidor e retornam imediatamente, independentemente do estado do aplicativo do servidor ou do computador do servidor. Ele também torna um subconjunto de recursos do MSMQ disponíveis para gerenciar filas de mensagens e fluxo de informações. A função [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) permite controlar a qualidade do serviço, a prioridade da chamada, o registro em log, a segurança e o tempo de vida da fila de processos do servidor. A função [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) permite que você especifique atributos da fila de processo do servidor, como persistência de fila, autenticação e criptografia.

Implemente o MSMQ assíncrono como você faria com o MSMQ síncrono. Você deve usar pontos de extremidade bem conhecidos e definir o protocolo de transporte para ser [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq). No arquivo IDL, aplique o atributo [Message](/windows/desktop/Midl/message) às funções que usam o enfileiramento de mensagens assíncrona. Observe que as funções de mensagem podem ter \[ \] apenas parâmetros.

 

 