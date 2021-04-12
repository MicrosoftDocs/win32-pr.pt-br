---
description: A configuração de serviços permite que o Windows Installer Personalize os serviços em um computador.
ms.assetid: 164280b2-1c75-49d2-ac04-c3654be84134
title: Usando a configuração de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6e3040d51b1056a370490fc5328a6bafe07555
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457241"
---
# <a name="using-services-configuration"></a>Usando a configuração de serviços

A configuração de serviços permite que o Windows Installer Personalize os [Serviços](../services/services.md) em um computador. Os desenvolvedores podem criar um pacote de Windows Installer para instalar, parar, iniciar e excluir serviços durante uma instalação usando [as tabelas](servicecontrol-table.md) de serviço e de [desinstalação](serviceinstall-table.md) e as ações [installservices](installservices-action.md), [StopServices](stopservices-action.md) e [DeleteServices](deleteservices-action.md) .

A partir de pacotes escritos para o Windows Installer 5,0, os desenvolvedores também podem usar a ação padrão [MsiConfigureServices](msiconfigureservices-action.md) e a [tabela MsiServiceConfig](msiserviceconfig-table.md) para configurar as opções de personalização de serviço estendidas disponíveis com o Windows 7 e o Windows Server 2008 R2 e o Windows Vista e o Windows Server 2008. Os pacotes de instalação existentes gravados para versões do Windows Installer que não incluíram a tabela MsiServiceConfig ainda podem ser instalados usando Windows Installer 5,0. O recurso de configuração de serviços do Windows Installer não pode configurar contas de serviço de rede, instalar processos de host de serviço compartilhado (svchost) ou reiniciar serviços interrompidos como parte da instalação.

**Windows XP e Windows Server 2003 ou anterior:** Sem suporte. As tabelas de configuração de serviço e as ações padrão estão disponíveis a partir do Windows Installer 5,0 em execução no Windows 7 e no Windows Server 2008 R2 e Windows Installer 4,5 em execução no Windows Vista e no Windows Server 2008.

Você deve incluir a ação [MsiConfigureServices](msiconfigureservices-action.md) na tabela [InstallExecuteSequence](installexecutesequence-table.md) para solicitar as configurações de serviço que você especificar na [tabela MsiServiceConfig](msiserviceconfig-table.md). O Windows Installer usa as informações na tabela MsiServiceConfig somente quando a ação padrão MsiConfigureServices é incluída em uma tabela de sequência. A ação padrão MsiConfigureServices também usa informações nas tabelas de [controle](servicecontrol-table.md) e de [instalação](serviceinstall-table.md) .

Para solicitar que o sistema conceda apenas os privilégios necessários a um serviço específico, especifique o serviço e a opção de configuração de **\_ \_ \_ \_ informações de privilégios necessários para configuração do serviço** na [tabela MsiServiceConfig](msiserviceconfig-table.md). Remova os privilégios desnecessários do token de processo do serviço. Essa opção pode ser usada para configurar os serviços executados no contexto de segurança das [contas de usuário do serviço](../services/service-user-accounts.md)LocalSystem, LocalService ou NetworkService.

Para solicitar que o sistema atrase o início automático de um serviço por um tempo após o início de todos os outros serviços de início automático, especifique o serviço e a opção de **\_ \_ \_ \_ início automático atrasado do serviço de configuração** na [tabela MsiServiceConfig](msiserviceconfig-table.md). O serviço que está sendo atrasado deve ser instalado pelo pacote atual com o \_ início automático do serviço \_ especificado na tabela de serviços de [instalação](serviceinstall-table.md) ou o serviço já deve estar instalado como um serviço de início automático.

Para solicitar que o sistema Reserve um recurso para o uso exclusivo de um serviço específico, especifique o serviço, o tipo de SID do serviço e a opção de configuração **\_ \_ \_ \_ informações de Sid** do serviço de configuração de serviço na [tabela MsiServiceConfig](msiserviceconfig-table.md). Adicione o SID do serviço à lista de controle de acesso (ACL) do recurso para o recurso.

Para solicitar que o SCM ( [Gerenciador de controle de serviço](../services/service-control-manager.md) ) Aguarde depois de enviar a notificação de **\_ \_ pré-desligamento de controle de serviço** para um serviço, faça o seguinte. Especifique o serviço, o período de tempo que o SCM deve aguardar e a opção de configuração **informações de pré-desligamento do serviço de \_ \_ \_ configuração** na [tabela MsiServiceConfig](msiserviceconfig-table.md).

Para configurar quando o sistema deve executar ações após a falha de um serviço, especifique o serviço e a opção de **sinalizador de ações de falha de configuração de serviço \_ \_ \_ \_** na [tabela MsiServiceConfig](msiserviceconfig-table.md). Adicione as ações a serem executadas na [tabela MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md).

Para obter mais informações sobre os recursos de personalização de serviço estendidos introduzidos com os sistemas operacionais Windows Vista e Windows Server 2008, consulte [alterações de serviço para o Windows Vista](../services/service-changes-for-windows-vista.md).

 

 
