---
title: Acesso thread-safe
description: Todas as funções nessa API são seguras para chamar simultaneamente de threads diferentes. No entanto, cada objeto passado como um parâmetro para as funções tem um comportamento de Threading específico, conforme descrito abaixo.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Serviços Web de segurança de thread para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25528f3315fcfae95d07d973d4743548eb35ec84bf754fdaafe067bcaccc56f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054456"
---
# <a name="thread-safety"></a>Acesso thread-safe

Todas as funções nessa API são seguras para chamar simultaneamente de threads diferentes. No entanto, cada objeto passado como um parâmetro para as funções tem um comportamento de Threading específico, conforme descrito abaixo.


Os seguintes identificadores são thread único e não oferecem suporte a operações simultâneas para uma determinada instância:

-   [HEAP do WS \_](ws-heap.md)
-   [\_mensagem WS](ws-message.md)
-   [\_buffer XML do WS \_](ws-xml-buffer.md)
-   [\_leitor de XML do WS \_](ws-xml-reader.md)
-   [gravador do WS \_ XML \_](ws-xml-writer.md)
-   [\_erro WS](ws-error.md)
-   [\_contexto de operação WS \_](ws-operation-context.md)
-   [\_política WS](ws-policy.md)
-   [metadados do WS \_](ws-metadata.md)
-   [\_token de segurança do WS \_](ws-security-token.md)
-   [\_contexto de segurança do WS \_](ws-security-context.md)

Os seguintes identificadores são threads livres e oferecem suporte a operações simultâneas para uma determinada instância:

-   [WS \_ Channel](ws-channel.md)
-   [\_ouvinte WS](ws-listener.md)
-   [\_host de serviço WS \_](ws-service-host.md)
-   [\_proxy de serviço WS \_](ws-service-proxy.md)

Para todos esses identificadores, o threading é definido em termos de operações (não chamadas de função). Uma operação é definida de maneira diferente para funções invocadas de forma síncrona versus funções invocadas de forma assíncrona:

-   Para funções invocadas de forma síncrona, a operação está pendente durante a execução da função.
-   Para funções invocadas de forma assíncrona, se a função retornar um código de retorno diferente de **WS \_ S \_ Async** , a operação estará pendente durante a execução da função. No entanto, se a função retornar **WS \_ S \_ Async** , a operação estará pendente até que o [**retorno de \_ \_ chamada WS assíncrono**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) seja invocado. Para obter mais informações sobre como invocar funções de forma assíncrona, consulte o tópico [modelo assíncrono](asynchronous-model.md) . para códigos de erro, consulte [Windows valores de retorno de serviços Web](windows-web-services-return-values.md).

A falha ao seguir o contrato de threading de um objeto resultará em um comportamento indefinido.

 

 




