---
title: Criando e vinculando a uma fila de solicitação
description: Uma fila de solicitações é uma fila de serviço que contém solicitações pendentes para um aplicativo específico.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c3a36fbbb9a8bcaa1c4e708240e99c276b09448ca56615df7da3d2cdf26836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914276"
---
# <a name="creating-and-binding-to-a-request-queue"></a>Criando e vinculando a uma fila de solicitação

Uma fila de solicitações é uma fila de serviço que contém solicitações pendentes para um aplicativo específico. Um aplicativo cria a fila de solicitação independentemente do grupo de URL ou da sessão do servidor chamando a função [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) e define as propriedades da fila de solicitação chamando a [**função HttpSetRequestQueueProperty.**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) Essas propriedades são o detalhado de 503 respostas, o comprimento máximo da fila e o estado da atividade.

Para fazer com que as solicitações sejam roteadas para sua fila [](run-time-configuration.md) de solicitações, o aplicativo vincula o grupo de URL criado como parte da configuração de tempo de execução à fila chamando [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) com **HttpServerBindingProperty** especificado no parâmetro *Property.* As solicitações de entrada das URLs no grupo são roteadas para a fila de solicitações especificada.

 

 




