---
title: Serviços de Área de Trabalho Remota classes de configuração
description: O provedor WMI de configuração de Serviços de Área de Trabalho Remota fornece as seguintes classes. Segue uma ilustração.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc9c58be85b8b4efc35495f35902ab67b35ad153
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366059"
---
# <a name="remote-desktop-services-configuration-classes"></a>Serviços de Área de Trabalho Remota classes de configuração

O provedor WMI de configuração de Serviços de Área de Trabalho Remota fornece as seguintes classes. Segue uma ilustração.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dd>

Representa a associação entre os elementos do sistema gerenciado e a classe de configuração definida para eles.

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

A classe base para todos os componentes do sistema que representam componentes do sistema abstratos, como perfis, processos ou recursos do sistema, na forma de dispositivos lógicos.

</dd> <dt>

[**\_MANAGEDSYSTEMELEMENT CIM**](cim-managedsystemelement.md)
</dt> <dd>

A classe base para a hierarquia de elementos do sistema.

</dd> <dt>

[**Configuração de CIM \_**](cim-setting.md)
</dt> <dd>

Representa parâmetros operacionais e relacionados à configuração para um ou mais elementos do sistema gerenciado.

</dd> <dt>

[**Terminal do Win32 \_**](win32-terminal.md)
</dt> <dd>

representa um terminal.

</dd> <dt>

[**\_TerminalError Win32**](win32-terminalerror.md)
</dt> <dd>

Representa um erro de terminal.

</dd> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dd>

uma subclasse da classe de [**\_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) . [**Win32 \_ TerminalService**](win32-terminalservice.md) representa a propriedade **Element** da Associação [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .

</dd> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> <dd>

representa a configuração de um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).

</dd> <dt>

[**\_TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md)
</dt> <dd>

representa a associação entre uma instância da classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e a configuração de uma determinada propriedade [**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) .

</dd> <dt>

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> <dd>

representa as configurações que podem ser aplicadas a um terminal.

</dd> <dt>

[**\_TerminalTerminalSetting Win32**](win32-terminalterminalsetting.md)
</dt> <dd>

representa a associação entre um terminal e seus parâmetros de configuração.

</dd> <dt>

[**\_TSAccount Win32**](win32-tsaccount.md)
</dt> <dd>

permite a exclusão de uma conta que existe no [**\_ terminal do Win32**](win32-terminal.md) e a modificação de permissões existentes.

</dd> <dt>

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> <dd>

define as definições de configuração para a classe de [**\_ terminal Win32**](win32-terminal.md) relacionada à política de conexão.

</dd> <dt>

[**\_TSDiscoveredLicenseServer Win32**](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

Fornece detalhes sobre o servidor de licença Área de Trabalho Remota descoberto.

</dd> <dt>

[**\_TSEnvironmentSetting Win32**](win32-tsenvironmentsetting.md)
</dt> <dd>

define as definições de configuração para a classe de [**\_ terminal do Win32**](win32-terminal.md) , incluindo a diretiva de programa inicial.

</dd> <dt>

[**\_TSGeneralSetting Win32**](win32-tsgeneralsetting.md)
</dt> <dd>

representa as configurações gerais do terminal, como o nível de criptografia e o protocolo de transporte.

</dd> <dt>

[**\_TSLogonSetting Win32**](win32-tslogonsetting.md)
</dt> <dd>

define as definições de configuração para a classe de [**\_ terminal Win32**](win32-terminal.md) relacionada ao logon do cliente.

</dd> <dt>

[**\_TSNetworkAdapterListSetting Win32**](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

enumera a lista de adaptadores de rede que podem ser configurados para um [**\_ terminal do Win32**](win32-terminal.md), com base no protocolo de terminal e no método de transporte especificados.

</dd> <dt>

[**\_TSNetworkAdapterSetting Win32**](win32-tsnetworkadaptersetting.md)
</dt> <dd>

define várias definições de configuração para a classe de [**\_ terminal do Win32**](win32-terminal.md) , incluindo propriedades relacionadas ao adaptador de rede e o número máximo de conexões permitidas.

</dd> <dt>

[**\_TSPermissionsSetting Win32**](win32-tspermissionssetting.md)
</dt> <dd>

inclui um método para adicionar novas contas ao terminal e um método para restaurar as permissões padrão para um terminal.

</dd> <dt>

[**\_TSRemoteControlSetting Win32**](win32-tsremotecontrolsetting.md)
</dt> <dd>

define as definições de configuração de controle remoto para a classe [**\_ terminal do Win32**](win32-terminal.md) .

</dd> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> <dd>

Define as definições de configuração do agente de Conexão de Área de Trabalho Remota (agente de conexão RD) para a classe [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .

</dd> <dt>

[**\_TSSessionDirectorySetting Win32**](win32-tssessiondirectorysetting.md)
</dt> <dd>

Representa a associação entre uma instância da classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e uma instância da classe [**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) .

</dd> <dt>

[**\_TSSessionSetting Win32**](win32-tssessionsetting.md)
</dt> <dd>

define as definições de configuração para a classe de [**\_ terminal do Win32**](win32-terminal.md) , tais como limites de tempo e ações de desconexão e reconexão.

</dd> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> <dd>

Define as configurações de virtualização de protocolo Internet (IP) para um servidor Host da Sessão RD.

</dd> <dt>

[**\_TSVirtualIPSetting Win32**](win32-tsvirtualipsetting.md)
</dt> <dd>

Representa a associação entre uma classe de elemento [**\_ TerminalService do Win32**](win32-terminalservice.md) e uma classe de configuração [**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md) .

</dd> </dl>

A ilustração a seguir mostra as relações entre essas classes.

![as relações entre as classes com suporte](images/tswmi.png)

 

 