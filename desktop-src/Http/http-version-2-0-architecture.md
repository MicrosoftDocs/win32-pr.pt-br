---
title: Arquitetura (API do servidor HTTP)
description: Os objetos de configuração de sessão de servidor, fila de solicitações e grupo de URLs permitem que os aplicativos configurem o serviço HTTP.
ms.assetid: 05a2d689-fd10-4065-85fc-2057bee42fbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3905a27708c87c43e141dd4cf8d84b2f0e7e66bc4dd189440733321ee951a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997097"
---
# <a name="architecture-http-server-api"></a>Arquitetura (API do servidor HTTP)

Os objetos de configuração de sessão de servidor, fila de solicitações e grupo de URLs permitem que os aplicativos configurem o serviço HTTP. As propriedades definidas nesses objetos substituem as configurações padrão de toda a API do servidor HTTP.

-   Sessão de servidor: o objeto de configuração de nível superior que define as configurações para todos os grupos de URLs criados na sessão.
-   Grupo de URLs: o grupo de URLs, criado na sessão de servidor, contém um conjunto de URLs que herdam as configurações definidas na sessão do servidor. As configurações do grupo de URLs substituem as configurações de sessão do servidor quando definidas pelo aplicativo. O grupo de URLs define uma parte do namespace em que o aplicativo está escutando e configura essa parte do namespace.
-   Fila de solicitações: este objeto define as configurações específicas para a fila de solicitações. Essas configurações são aplicadas a todas as URLs nos grupos associados à fila de solicitações.

O diagrama a seguir mostra a relação entre os objetos de configuração e o aplicativo. Normalmente, uma única sessão de servidor é criada para cada aplicativo com um ou mais grupos de URLs criados nele. As filas de solicitação são criadas independentemente do grupo de URLs ou da sessão de servidor. Os grupos de URLs devem ser associados a uma fila de solicitações para receber solicitações.

![relação entre os objetos de configuração e o aplicativo](images/architecture.png)

O recurso de fila de solicitação nomeado da API do servidor HTTP versão 2,0 permite que vários processos de trabalho recebam solicitações em uma fila de solicitações. A fila de solicitações é criada por um processo de controlador que identifica os processos de trabalho com acesso concedido à fila de solicitações. Para obter mais informações, consulte o tópico [fila de solicitações nomeadas](named-request-queue.md)

## <a name="property-configuration"></a>Configuração de propriedade

Para obter mais informações sobre como definir propriedades nos objetos de configuração, consulte os seguintes tópicos:

-   [Configurando a fila de solicitações](configuring-the-request-queue.md)
-   [Configurando a sessão do servidor](configuring-the-server-session.md)
-   [Configurando o grupo de URLs](configuring-the-url-group.md)

A tabela a seguir lista as propriedades que são definidas nos objetos de configuração. Para obter mais informações sobre as configurações de propriedade, consulte o tópico [Configurando propriedades no http versão 2,0](configuring-properties-in-http-version-2-0.md) .



| Nome           | Propriedade                                                                                                                                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sessão de servidor | HttpServerStateProperty<br/> HttpServerLoggingProperty<br/> HttpServerBandwidthProperty<br/> HttpServerTimeoutsProperty<br/> HttpServerAuthenticatonProperty<br/>                                                                               |
| Grupo de URLs      | HttpServerStateProperty<br/> HttpServerAuthenticatonProperty<br/> HttpServerLoggingProperty<br/> HttpServerConnectionsProperty<br/> HttpServerBandwidthProperty<br/> HttpServerBindingProperty<br/> HttpServerTimeoutsProperty<br/> |
| Fila de solicitação  | HttpServerStateProperty<br/> HttpServerQueueLengthProperty<br/> HttpServer503VerbosityProperty<br/>                                                                                                                                                         |



 

 

 





