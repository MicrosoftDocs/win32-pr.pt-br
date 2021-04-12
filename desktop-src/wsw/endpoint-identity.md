---
title: Identidade de ponto de extremidade
description: Os tipos definidos nesta seção são usados para definir a identidade de segurança de um endereço de ponto de extremidade.
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Serviços Web de identidade do ponto de extremidade para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7a3f7b95d5fc1b926d8bafb49b06f96c7d68fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363693"
---
# <a name="endpoint-identity"></a>Identidade de ponto de extremidade

Os tipos definidos nesta seção são usados para definir a identidade de segurança de um endereço de ponto de extremidade.

Os seguintes elementos de API fazem parte do recuo do ponto de extremidade:



| Enumeração                                                       | Descrição                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**tipo de identidade do ponto de \_ extremidade WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | O tipo da identidade do ponto de extremidade, usado como um seletor de subtipos de [**\_ \_ identidade do ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity). |



 



| Estrutura                                                               | Descrição                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_identidade do \_ ponto de extremidade WS CERT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | O tipo de identidade do ponto de extremidade do certificado.                                                 |
| [**\_identidade do \_ ponto de extremidade do DNS do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | O tipo para especificar uma identidade de ponto de extremidade representada por um nome DNS.                      |
| [**\_identidade do ponto de extremidade WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | O tipo base para todas as identidades do ponto de extremidade.                                                   |
| [**\_identidade de \_ ponto de extremidade RSA WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | Tipo para identidade de ponto de extremidade RSA.                                                              |
| [**\_identidade do \_ ponto de extremidade WS SPN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | O tipo para especificar uma identidade de ponto de extremidade representada por um SPN (nome da entidade de serviço). |
| [**\_identidade de \_ ponto de extremidade desconhecido WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | O tipo de uma identidade de ponto de extremidade desconhecida.                                                   |
| [**\_identidade do \_ ponto de extremidade UPN do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | O tipo para especificar uma identidade de ponto de extremidade representada por um UPN (nome principal do usuário).     |



 

 

 




