---
title: Configurações de associação de segurança
description: As configurações de associação de segurança controlam a maneira como um token de segurança é obtido ou usado.
ms.assetid: 4bc03cb4-1ac2-4ad1-a45d-eae8f50f5355
keywords:
- Serviços Web de configurações de associação de segurança para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5a3d27627c3360560a38ef9cb85e3fb5ece434
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103642981"
---
# <a name="security-binding-settings"></a>Configurações de associação de segurança

As configurações de associação de segurança controlam a maneira como um token de segurança é obtido ou usado. Elas são representadas como uma coleção de pares propriedade-valor, com as chaves de propriedade definidas pela [**Propriedade Enumeração WS \_ Security \_ Binding \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property). Cada propriedade na coleção tem um valor padrão razoável. Como resultado, é possível definir e usar uma descrição de segurança sem especificar nenhuma das configurações de associação de segurança.


Para obter informações sobre configurações de segurança de todo o canal, com propriedades cujas chaves são definidas pela enumeração de ID de propriedade de segurança do WS, consulte [configurações de canal de segurança](security-channel-settings.md). [**\_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

Os seguintes elementos de API são usados com as configurações de associação de segurança.

| Enumeração                                                                          | Descrição                                                                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ falha no WS CERT**](/windows/win32/api/webservices/ne-webservices-ws_value_type)                                         | Define falhas relacionadas à validação de certificado.                                                                                                               |
| [**\_esquema de \_ autenticação de cabeçalho http \_ do WS \_**](https://technet.microsoft.com/windows/dd401907(v=vs.60))                 | Define as opções para executar a autenticação de cliente usando cabeçalhos de autenticação HTTP.                                                                       |
| [**\_destino de \_ autenticação de cabeçalho http \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_http_header_auth_target)                 | Define o destino para a associação de segurança de autenticação de cabeçalho HTTP.                                                                                           |
| [**\_ação de \_ token de segurança de solicitação WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_action)     | Define qual conjunto de ações usar ao negociar tokens de segurança usando WS-Trust.                                                                              |
| [**\_nome do \_ conjunto de algoritmos de segurança do \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_suite_name)     | Um conjunto de algoritmos de segurança usado para tarefas como assinatura e encryting.                                                                                      |
| [**\_ID da \_ propriedade de associação de segurança WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)       | Identifica as propriedades usadas para especificar as configurações de associação de segurança.                                                                                              |
| [**\_modo de \_ entropia de chave de segurança WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode)             | Define como a aleatoriedade deve ser contribuída para a chave emitida durante uma negociação de token de segurança feita com a mensagem e a segurança de modo misto.                     |
| [**\_tipo de \_ chave de segurança do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_type)                              | O tipo de chave de um token de segurança.                                                                                                                                 |
| [**\_modo de \_ referência de token de segurança do WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_reference_mode)     | o mecanismo a ser usado para se referir a um token de segurança de assinaturas, itens criptografados e tokens derivados no contexto das associações de segurança de modo misto e de mensagem. |
| [**\_versão de confiança do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version)                                       | Define a versão de especificação de WS-Trust a ser usada com segurança de mensagem e segurança de modo misto.                                                              |
| [**\_pacote de \_ \_ autenticação integrada do Windows \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_package) | Define o pacote SSP específico a ser usado para a autenticação integrada do Windows.                                                                                |



 



| Estrutura                                                               | Descrição                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [**\_propriedade de \_ Associação de segurança WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) | Especifica uma configuração de associação de segurança específica. |



 

 

 




