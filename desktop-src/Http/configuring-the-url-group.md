---
title: Configurando o grupo de URLs
description: .
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d9be6969b2b197d0bdcb404ad6b8965c278235
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916462"
---
# <a name="configuring-the-url-group"></a>Configurando o grupo de URLs

A ID do grupo de URLs é criada com a função [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) e usada na chamada para [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). O parâmetro *pPropertyInformation* aponta para a estrutura de configuração para o tipo de propriedade definido. O parâmetro **PropertyInformationLength** especifica o tamanho, em bytes, da estrutura de configuração. Por exemplo, ao definir **HttpServerTimeoutsProperty** , o parâmetro *pPropertyInformation* deve apontar para um buffer que não pode ser menor do que a estrutura de [**\_ \_ \_ informações de limite de tempo limite http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) . As configurações do grupo de URLs são consultadas chamando [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty).

Depois que o grupo de URLs é criado, as URLs são adicionadas ao grupo com [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup). O grupo de URLs deve estar associado a uma fila de solicitação da versão 2,0 para receber solicitações. Para associar o grupo de URLs a uma fila de solicitações, o aplicativo chama [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) e especifica **HttpServerBindingProperty** no parâmetro *Property* . Se essa propriedade não for definida, as solicitações correspondentes para o grupo de URLs não serão entregues a uma fila de solicitações e a API do servidor HTTP gerará uma resposta 503. O aplicativo só pode adicionar URLs que foram reservadas anteriormente com o serviço a um grupo de URLs durante a execução com baixo privilégio. Para obter mais informações, consulte o tópico [reservas, registros e roteamento de namespace](namespace-reservations-registrations-and-routing.md) .

 

 




