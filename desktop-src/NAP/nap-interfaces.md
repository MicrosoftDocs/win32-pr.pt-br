---
title: Interfaces NAP
description: Interfaces NAP
ms.assetid: fff854b9-9c83-4db2-bceb-22509b261a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff67fe21922c5b1baf9c2825dc7ea2852f14331
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006028"
---
# <a name="nap-interfaces"></a>Interfaces NAP

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O sistema NAP é composto pelas seguintes interfaces.



| Nome da Interface                                                                   | Descrição                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapCertRelyingParty**](inapcertrelyingparty.md)                             | Fornece métodos que as partes confiáveis de certificado devem usar para se comunicar com o NapAgent.                                                        |
| [**INapClientManagement**](inapclientmanagement.md)                             | Usado para o gerenciamento de cliente NAP do cache SoH e o disparo de intercâmbio SoH. Preterido.                                                                |
| [**INapClientManagement2**](inapclientmanagement2.md)                           | Usado para o gerenciamento de cliente NAP do cache SoH e o disparo de intercâmbio SoH.                                                                            |
| [**INapComponentConfig**](inapcomponentconfig.md)                               | Usado para a configuração personalizada dos componentes SHV. Preterido.                                                                                    |
| [**INapComponentConfig2**](inapcomponentconfig2.md)                             | Fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema) para configurar uma interface de usuário do servidor de diretivas de rede (NPS) remotamente.   |
| [**INapComponentConfig3**](inapcomponentconfig3.md)                             | Fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema) para definir e modificar dados de configuração para uma ID de configuração específica. |
| [**INapComponentInfo**](inapcomponentinfo.md)                                   | Deve ser implementado por componentes de plug-in, como SHAs e SHVs, para que eles possam ser comunicados pelo sistema NAP.                          |
| [**INapEnforcementClientBinding**](inapenforcementclientbinding.md)             | Usado por clientes de imposição para se comunicar com o NapAgent.                                                                                       |
| [**INapEnforcementClientCallback**](inapenforcementclientcallback.md)           | Os clientes de imposição devem implementar essa interface para permitir que o NapAgent se comunique com eles.                                                  |
| [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)       | Permite o gerenciamento de conexão do cliente. Preterido.                                                                                                |
| [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)     | Permite o gerenciamento de conexão do cliente.                                                                                                            |
| [**INapServerCallback**](inapservercallback.md)                                 | Os SHVs usam o método único nessa interface para sinalizar a conclusão da solicitação assíncrona.                                                             |
| [**INapServerInfo**](inapserverinfo.md)                                         | Usado por clientes de gerenciamento (por exemplo, provedores WMI, ferramentas de linha de comando, etc.) para consultar o status do sistema de servidor NAP.                             |
| [**INapServerManagement**](inapservermanagement.md)                             | Usado para o gerenciamento básico do servidor NAP.                                                                                                        |
| [**INapSoHConstructor**](inapsohconstructor.md)                                 | Usado por SHAs para construir solicitações SoH e por SHVs para construir respostas SoH.                                                                      |
| [**INapSoHProcessor**](inapsohprocessor.md)                                     | Usado por SHAs para processar o conteúdo de SoH-Responses e por SHVs para processar o conteúdo de SoH-requests.                                          |
| [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)             | Os SHAs devem usar essa interface para se comunicar com o NapAgent. Preterido.                                                                          |
| [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)           | Os SHAs devem usar essa interface para se comunicar com o NapAgent.                                                                                      |
| [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)           | Os SHAs devem implementar essa interface para coordenar o processamento com o sistema NAP.                                                                    |
| [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)             | Os SHAs usam essa interface para se comunicar e coordenar seu processamento com o sistema NAP.                                                         |
| [**INapSystemHealthValidator**](inapsystemhealthvalidator.md)                   | Fornece métodos que um SHV deve implementar para que o sistema NAP possa se comunicar com ele.                                                         |
| [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)   | Os SHVs usam essa interface para a comunicação de dados com a contraparte do lado do cliente. Preterido.                                                      |
| [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) | Os SHVs usam essa interface para a comunicação de dados com a contraparte do lado do cliente.                                                                  |



 

 

 




