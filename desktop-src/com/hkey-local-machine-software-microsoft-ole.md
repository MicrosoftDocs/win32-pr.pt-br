---
title: HKEY_LOCAL_MACHINESOFTWAREMicrosoftOle
description: Os valores do registro associados com a HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE Key controlam as configurações de permissão de acesso e de inicialização padrão e os recursos de segurança de nível de chamada para aplicativos baseados em com que não chamam CoInitializeSecurity.
ms.assetid: 871ae88f-ed2c-4078-8160-b0a490390426
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02406bca5dd69098f8cd49c2fba5f067852fcc5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006080"
---
# <a name="hkey_local_machinesoftwaremicrosoftole"></a>HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE

Os valores do registro associados com a **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE** Key controlam as configurações de permissão de acesso e de inicialização padrão e os recursos de segurança de nível de chamada para aplicativos baseados em com que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Somente administradores, o criador do objeto e o sistema têm acesso completo a essa parte do registro. Todos os outros usuários têm acesso somente leitura.



| Valor do Registro                                                                         | Descrição                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md)                 | Define o detalhamento das entradas do log de eventos sobre solicitações com falha para inicialização e ativação do componente.                                                                            |
| [**CallFailureLoggingLevel**](callfailurelogginglevel.md)                             | Define o detalhamento das entradas do log de eventos sobre as chamadas com falha para os componentes.                                                                                                     |
| [**DCOMSCMRemoteCallFlags**](dcomscmremotecallflags.md)                               | Controla o comportamento de chamadas do Gerenciador de controle de serviço (DCOMSCM) local DCOM para um DCOMSCM remoto.                                                                     |
| [**DefaultAccessPermission**](defaultaccesspermission.md)                             | Define a lista de permissões de acesso padrão para o computador.                                                                                                                      |
| [**DefaultLaunchPermission**](defaultlaunchpermission.md)                             | Define a ACL de inicialização padrão para o computador.                                                                                                                                  |
| [**EnableDCOM**](enabledcom.md)                                                       | Define a política de ativação global para o computador.                                                                                                                           |
| [**InvalidSecurityDescriptorLoggingLevel**](invalidsecuritydescriptorlogginglevel.md) | Define o detalhamento das entradas do log de eventos sobre descritores de segurança inválidos para permissões de acesso e de inicialização do componente.                                                       |
| [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)                         | Define o nível de autenticação padrão.                                                                                                                                        |
| [**LegacyImpersonationLevel**](legacyimpersonationlevel.md)                           | Define o nível de representação padrão.                                                                                                                                         |
| [**LegacySecureReferences**](legacysecurereferences.md)                               | Determina o nível de segurança das invocações de liberação de **AddRef** /  .                                                                                                              |
| [**MachineAccessRestriction**](machineaccessrestriction.md)                           | Define a política de restrição de todo o computador para acesso ao componente.                                                                                                               |
| [**MachineLaunchRestriction**](machinelaunchrestriction.md)                           | Define a política de restrição de todo o computador para inicialização e ativação de componentes.                                                                                                |
| [**NonRedist**](nonredist.md)                                                         | Adiciona nomes à lista de arquivos que não devem ser exportados quando aplicativos COM+ são empacotados para instalação em outros computadores. Observe que essa é uma subchave, não um valor. |
| [**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)                   | Determina se os níveis de confiança da política de restrição de software (SRP) são usados durante as ativações do ActivateAsActivator.                                                            |
| [**SRPRunningObjectChecks**](srprunningobjectchecks.md)                               | Determina se as tentativas de conexão com objetos em execução são filtradas para os níveis de confiança da política de restrição de software (SRP) compatíveis.                                         |



 

 

 




