---
title: Configurações de canal de segurança
description: As configurações de canal de segurança controlam a maneira como a segurança é aplicada e verificada em um canal.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Serviços Web de configurações de canal de segurança para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104085010"
---
# <a name="security-channel-settings"></a>Configurações de canal de segurança

As configurações de canal de segurança controlam a maneira como a segurança é aplicada e verificada em um canal. Cada configuração de canal de segurança é representada por uma coleção de pares de propriedade-valor, com as chaves de propriedade definidas pela [**\_ identificação de \_ propriedade \_ de segurança WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)de enumeração. Cada propriedade na coleção tem um valor padrão razoável. Devido a esses valores padrão, é possível definir e usar uma descrição de segurança sem especificar as configurações de canal de segurança.


[As configurações de associação de segurança](security-binding-settings.md) contêm coleções semelhantes de pares de propriedade-valor cujas chaves são definidas pela estrutura de propriedade de [**Associação de segurança do WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) . A diferença entre esses dois tipos de configurações é que as configurações de canal de segurança têm como escopo uma descrição de segurança (ou seja, elas contêm propriedades de segurança de todo o canal), enquanto as configurações de associação de segurança têm como escopo uma das associações de segurança, e pode haver muitas associações de segurança. Consequentemente, por exemplo, uma descrição de segurança personalizada que contenha três associações de segurança terá um recipiente de configurações de canal de segurança para todo o canal e três pacotes de configurações de ligação de segurança, um para cada associação de segurança.

As seguintes enumerações são usadas com as configurações de canal de segurança:

-   [**\_nível de proteção do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [**\_ID da \_ Propriedade do token de segurança da solicitação WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [**\_ID do \_ algoritmo de segurança do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [**\_ID da \_ Propriedade do algoritmo de segurança do WS \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [**\_layout do \_ cabeçalho de segurança do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [**\_versão do \_ cabeçalho de segurança do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [**\_ID da \_ propriedade de segurança do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_uso do \_ carimbo de data/hora do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [**\_ID da \_ Propriedade do token de segurança \_ \_ do WS XML \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

As seguintes estruturas são usadas com as configurações de canal de segurança:

-   [**\_propriedade de \_ token de segurança de solicitação WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [**\_Propriedade do \_ algoritmo de segurança do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [**\_conjunto de \_ algoritmos de segurança do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [**\_propriedade de segurança WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [**\_Propriedade do \_ token de segurança \_ \_ do WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




