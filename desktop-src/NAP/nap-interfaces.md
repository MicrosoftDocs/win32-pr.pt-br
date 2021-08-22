---
title: NAP Interfaces
description: NAP Interfaces
ms.assetid: fff854b9-9c83-4db2-bceb-22509b261a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b704e8924886047b0a50aef7929f52be276a0417d118f2026e47706f95678a2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620815"
---
# <a name="nap-interfaces"></a>NAP Interfaces

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O sistema NAP é composto pelas interfaces a seguir.



| Nome da Interface                                                                   | Descrição                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapCertRelyingParty**](inapcertrelyingparty.md)                             | Fornece métodos que as partes que dependem de certificado devem usar para se comunicar com o NapAgent.                                                        |
| [**INapClientManagement**](inapclientmanagement.md)                             | Usado para gerenciamento de cliente NAP do cache SoH e gatilho de troca soH. Preterido.                                                                |
| [**INapClientManagement2**](inapclientmanagement2.md)                           | Usado para gerenciamento de cliente NAP do cache SoH e gatilho de troca soH.                                                                            |
| [**INapComponentConfig**](inapcomponentconfig.md)                               | Usado para configuração personalizada de componentes SHV. Preterido.                                                                                    |
| [**INapComponentConfig2**](inapcomponentconfig2.md)                             | Fornece métodos de configuração do sistema NAP para shVs (validadores de saúde do sistema) configurarem remotamente uma interface do usuário do NPS (servidor de políticas de rede).   |
| [**INapComponentConfig3**](inapcomponentconfig3.md)                             | Fornece métodos de configuração do sistema NAP para shVs (validadores de saúde do sistema) definirem e modificarem dados de configuração para uma ID de configuração específica. |
| [**INapComponentInfo**](inapcomponentinfo.md)                                   | Deve ser implementado por componentes de plug-in, como SHAs e SHVs, para que possam ser comunicados pelo sistema NAP.                          |
| [**INapEnforcementClientBinding**](inapenforcementclientbinding.md)             | Usado por clientes de imposição para se comunicar com o NapAgent.                                                                                       |
| [**INapEnforcementClientCallback**](inapenforcementclientcallback.md)           | Os clientes de imposição devem implementar essa interface para permitir que o NapAgent se comunique com eles.                                                  |
| [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)       | Permite o gerenciamento de conexões do cliente. Preterido.                                                                                                |
| [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)     | Permite o gerenciamento de conexões do cliente.                                                                                                            |
| [**INapServerCallback**](inapservercallback.md)                                 | SHVs usam o método único nessa interface para sinalizar a conclusão da solicitação assíncrona.                                                             |
| [**INapServerInfo**](inapserverinfo.md)                                         | Usado por clientes de gerenciamento (por exemplo, provedores WMI, ferramentas de linha de comando etc.) para consultar o status do sistema de servidores NAP.                             |
| [**INapServerManagement**](inapservermanagement.md)                             | Usado para gerenciamento básico do servidor NAP.                                                                                                        |
| [**INapSoHConstructor**](inapsohconstructor.md)                                 | Usado por SHAs para construir solicitações SoH e por SHVs para construir respostas SoH.                                                                      |
| [**INapSoHProcessor**](inapsohprocessor.md)                                     | Usado por SHAs para processar o conteúdo de respostas SoH e por SHVs para processar o conteúdo de solicitações SoH.                                          |
| [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)             | SHAs devem usar essa interface para se comunicar com o NapAgent. Preterido.                                                                          |
| [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)           | SHAs devem usar essa interface para se comunicar com o NapAgent.                                                                                      |
| [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)           | SHAs devem implementar essa interface para coordenar o processamento com o sistema NAP.                                                                    |
| [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)             | ShAs usam essa interface para se comunicar e coordenar seu processamento com o sistema NAP.                                                         |
| [**INapSystemHealthValidator**](inapsystemhealthvalidator.md)                   | Fornece métodos que um SHV deve implementar para que o sistema NAP possa se comunicar com ele.                                                         |
| [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)   | SHVs usam essa interface para comunicação de dados com seus equivalentes do lado do cliente. Preterido.                                                      |
| [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) | SHVs usam essa interface para comunicação de dados com seus equivalentes do lado do cliente.                                                                  |



 

 

 




