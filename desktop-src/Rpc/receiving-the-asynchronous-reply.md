---
title: Recebendo a resposta assíncrona
description: Depois de ser notificado de que o servidor enviou uma resposta, o cliente chama RpcAsyncCompleteCall com o identificador assíncrono para que ele possa receber a resposta.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366590"
---
# <a name="receiving-the-asynchronous-reply"></a>Recebendo a resposta assíncrona

Depois de ser notificado de que o servidor enviou uma resposta, o cliente chama [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) com o identificador assíncrono para que ele possa receber a resposta. Quando **RpcAsyncCompleteCall** for concluído com êxito, o parâmetro de *resposta* apontará para um buffer que contém o valor de retorno da função remota. Todos os buffers fornecidos pelo programa cliente como \[ [**out**](/windows/desktop/Midl/out-idl) \] ou \[ [**in**](/windows/desktop/Midl/in), parâmetros de **saída** \] para a função remota assíncrona contêm dados válidos. Se o cliente chamar **RpcAsyncCompleteCall** antes que o servidor tenha enviado a resposta, essa chamada falhará e retornará um valor de \_ chamada de RPC S \_ Async \_ \_ pendente.

Se o programa cliente usar portas de conclusão de e/s ou eventos para notificação, ele deverá chamar [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para liberar a porta ou o identificador quando ele não precisar mais delas.

 

 