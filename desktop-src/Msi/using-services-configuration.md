---
description: A configuração de serviços permite Windows instalador de dados para personalizar os serviços em um computador.
ms.assetid: 164280b2-1c75-49d2-ac04-c3654be84134
title: Usando a configuração de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe1e34cce317ee00c3cc9d6ee4aac449e500499dc2dee4e97df65ba91bca2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012695"
---
# <a name="using-services-configuration"></a>Usando a configuração de serviços

A configuração de serviços permite Windows instalador de dados para personalizar os [serviços](../services/services.md) em um computador. Os desenvolvedores podem Windows pacote do Instalador do Windows para instalar, parar, iniciar e excluir serviços durante uma instalação usando as tabelas [ServiceControl](servicecontrol-table.md) e [ServiceInstall](serviceinstall-table.md) e as ações [InstallServices,](installservices-action.md) [StopServices](stopservices-action.md) e [DeleteServices.](deleteservices-action.md)

A partir dos pacotes escritos para o Instalador do Windows 5.0, os desenvolvedores também podem usar a ação padrão [MsiConfigureServices](msiconfigureservices-action.md) e a tabela [MsiServiceConfig](msiserviceconfig-table.md) para configurar as opções de personalização de serviço estendido disponíveis com o Windows 7 e o Windows Server 2008 R2 e Windows Vista e Windows Server 2008. Pacotes de instalação existentes escritos para versões do Windows Installer que não incluíram a tabela MsiServiceConfig ainda podem ser instalados usando o Windows Installer 5.0. O recurso de configuração de serviços do Windows Instalador não pode configurar contas de serviço de rede, instalar processos de host de serviço compartilhado (svchost) ou reiniciar serviços interrompidos como parte da instalação.

**Windows XP e Windows Server 2003 ou anterior:** Sem suporte. As tabelas de configuração de serviço e as ações padrão estão disponíveis a partir do Windows Installer 5.0 em execução no Windows 7 e no Windows Server 2008 R2 e no Windows Installer 4.5 em execução no Windows Vista e Windows Server 2008.

Você deve incluir a [ação MsiConfigureServices](msiconfigureservices-action.md) na tabela [InstallExecuteSequence](installexecutesequence-table.md) para solicitar as configurações de serviço especificadas na tabela [MsiServiceConfig](msiserviceconfig-table.md). O Windows instalador usa as informações na tabela MsiServiceConfig somente quando a ação padrão MsiConfigureServices é incluída em uma tabela de sequência. A ação padrão MsiConfigureServices também usa informações nas tabelas [ServiceControl](servicecontrol-table.md) e [ServiceInstall.](serviceinstall-table.md)

Para solicitar que o sistema dê somente os privilégios necessários a um serviço específico, especifique o serviço e a opção de configuração DE INFORMAÇÕES DE PRIVILÉGIOS **\_ \_ \_ NECESSÁRIOS \_** DA CONFIGURAÇÃO DE SERVIÇO na tabela [MsiServiceConfig](msiserviceconfig-table.md). Remova os privilégios desaconsumentados do token de processo do serviço. Essa opção pode ser usada para configurar serviços executados no contexto de segurança das contas de usuário do serviço LocalSystem, LocalService ou [NetworkService](../services/service-user-accounts.md).

Para solicitar que o sistema atrase o início automático de um serviço por um tempo após o início de todos os outros serviços de início automático, especifique o serviço e a opção **SERVICE \_ CONFIG \_ DELAYED \_ AUTO \_ START** na tabela [MsiServiceConfig](msiserviceconfig-table.md). O serviço que está sendo atrasado deve ser instalado pelo pacote atual com SERVICE AUTO START especificado na tabela ServiceInstall ou o serviço já deve estar instalado como um serviço de \_ \_ início automático. [](serviceinstall-table.md)

Para solicitar que o sistema reserve um recurso para o uso exclusivo de um serviço específico, especifique o serviço, o tipo sid de serviço e a opção de configuração DE INFORMAÇÕES DO SID DO SERVIÇO **\_ DE CONFIGURAÇÃO \_ \_ \_** NA tabela [MsiServiceConfig](msiserviceconfig-table.md). Adicione o SID do serviço à ACL (Lista de Controle de Acesso) do recurso para o recurso.

Para solicitar que o SCM [(Service Control Manager)](../services/service-control-manager.md) aguarde depois de enviar a notificação **SERVICE CONTROL \_ \_ PRESHUTDOWN** para um serviço, faça o seguinte. Especifique o serviço, o período de tempo que o SCM deve aguardar e a opção de configuração **\_ SERVICE CONFIG \_ PRESHUTDOWN \_ INFO** na [tabela MsiServiceConfig](msiserviceconfig-table.md).

Para configurar quando o sistema deve executar ações após a falha de um serviço, especifique o serviço e a opção **SERVICE \_ CONFIG \_ FAILURE ACTIONS \_ \_ FLAG** na [tabela MsiServiceConfig](msiserviceconfig-table.md). Adicione as ações a serem executados à [tabela MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md).

Para obter mais informações sobre os recursos de personalização de serviço estendido introduzidos com os sistemas operacionais Windows Vista e Windows Server 2008, consulte Alterações de serviço [para Windows Vista](../services/service-changes-for-windows-vista.md).

 

 
