---
title: Criando e ligando a uma fila de solicitações
description: Uma fila de solicitações é uma fila de serviço que mantém solicitações pendentes para um aplicativo específico.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945b8451f9128357b7da0ddc64600b74deffd0d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364243"
---
# <a name="creating-and-binding-to-a-request-queue"></a>Criando e ligando a uma fila de solicitações

Uma fila de solicitações é uma fila de serviço que mantém solicitações pendentes para um aplicativo específico. Um aplicativo cria a fila de solicitações independentemente do grupo de URLs ou da sessão de servidor chamando a função [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) e define as propriedades da fila de solicitações chamando a função [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) . Essas propriedades são o detalhamento de 503 respostas, o comprimento máximo da fila e o estado da atividade.

Para fazer com que as solicitações sejam roteadas para sua fila de solicitações, o aplicativo associa o grupo de URLs criado como parte da [configuração de tempo de execução](run-time-configuration.md) à fila chamando [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) com **HttpServerBindingProperty** especificado no parâmetro *Property* . As solicitações de entrada das URLs no grupo são então roteadas para a fila de solicitações especificada.

 

 




