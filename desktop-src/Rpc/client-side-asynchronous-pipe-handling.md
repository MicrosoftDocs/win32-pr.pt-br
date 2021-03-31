---
title: Manipulação de pipes assíncronos do lado do cliente
description: Antes de fazer uma chamada remota assíncrona, o cliente deve primeiro inicializar o identificador assíncrono.
ms.assetid: 3d54b233-d8b0-45d1-b759-0d2d24c1e247
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ff503f80c77b2403d683c2b644d89836365956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822903"
---
# <a name="client-side-asynchronous-pipe-handling"></a>Manipulação de pipes assíncronos do lado do cliente

Antes de fazer uma chamada remota assíncrona, o cliente deve primeiro inicializar o identificador assíncrono. Assim como ocorre com os procedimentos nonpipe, o cliente chama uma função assíncrona com o identificador assíncrono como o primeiro parâmetro e usa o identificador assíncrono para enviar e receber dados de pipe, consultar o status da chamada e receber a resposta.

O cliente faz a chamada de procedimento remoto assíncrona com o identificador assíncrono como o primeiro parâmetro. O cliente pode usar esse identificador para consultar o status da chamada e para receber a resposta. O modelo de pipe assíncrono é simétrico. Os aplicativos cliente e servidor enviam e recebem dados de pipe ativamente (em oposição ao RPC síncrono, em que os dados do pipe são enviados e recebidos passivamente).

O cliente envia dados de pipe assíncrono chamando a função **Push** no pipe assíncrono apropriado, com a variável de estado do pipe como o primeiro parâmetro. Quando a função **Push** retorna, o cliente pode modificar ou liberar o buffer de envio.

Se o \_ sinalizador de \_ notificação assíncrona de RPC \_ no \_ envio \_ for definido no identificador assíncrono e se APCs for usado como o mecanismo de notificação, uma APC será enfileirada quando o pipe Send for realmente concluído. Você pode aproveitar esse mecanismo para implementar o controle de fluxo. No entanto, observe que, se o cliente enviar outro buffer antes da conclusão do envio anterior, o cliente poderá, dependendo da velocidade da operação de transferência, receberá apenas uma notificação de envio por push, em vez de uma notificação para cada buffer ou cada operação de **envio** . Quando o cliente enviou todos os dados do pipe, ele faz uma chamada de **envio por push** final com o número de elementos definido como 0.

O programa cliente recebe dados de pipe assíncrono chamando a função **pull** no pipe assíncrono apropriado, com a variável de estado do pipe como o primeiro parâmetro. Se nenhum dado de pipe estiver disponível, a função **pull** retornará \_ a \_ chamada assíncrona de RPC S \_ \_ pendente.

Se o mecanismo de notificação for a APC e o servidor tiver retornado a \_ \_ chamada assíncrona de RPC S \_ \_ pendente, o cliente deverá aguardar até receber a APC **RpcReceiveComplete** do tempo de execução antes de chamar **pull** novamente.

 

 




