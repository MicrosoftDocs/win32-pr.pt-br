---
title: Serviços de Área de Trabalho Remota classes de Configuração do Serviços de Área de Trabalho Remota
description: O provedor WMI Serviços de Área de Trabalho Remota Configuration fornece as classes a seguir. Uma ilustração a seguir.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de40784e1e0c9e0387b8d6ff60193639032f7e0cbe5e34c4a8b35aeb32cc37cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000117"
---
# <a name="remote-desktop-services-configuration-classes"></a>Serviços de Área de Trabalho Remota classes de Configuração do Serviços de Área de Trabalho Remota

O provedor WMI Serviços de Área de Trabalho Remota Configuration fornece as classes a seguir. Uma ilustração a seguir.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**Elemento \_ CIMSetting**](cim-elementsetting.md)
</dt> <dd>

Representa a associação entre elementos do sistema gerenciado e a classe de configuração definida para eles.

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

A classe base para todos os componentes do sistema que representam componentes abstratos do sistema, como perfis, processos ou recursos do sistema, na forma de dispositivos lógicos.

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

A classe base para a hierarquia de elementos do sistema.

</dd> <dt>

[**Configuração cim \_**](cim-setting.md)
</dt> <dd>

Representa parâmetros operacionais e relacionados à configuração para um ou mais elementos do sistema gerenciado.

</dd> <dt>

[**Win32 \_ Terminal**](win32-terminal.md)
</dt> <dd>

representa um terminal.

</dd> <dt>

[**Win32 \_ TerminalError**](win32-terminalerror.md)
</dt> <dd>

Representa um erro de terminal.

</dd> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dd>

uma subclasse da [**classe Serviço \_ Win32.**](/windows/desktop/CIMWin32Prov/win32-service) [**Win32 \_ TerminalService**](win32-terminalservice.md) representa **a propriedade Element** da associação [**Win32 \_ TerminalServiceToSetting.**](win32-terminalservicetosetting.md)

</dd> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> <dd>

representa a configuração de um Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) .

</dd> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dd>

representa a associação entre uma instância da classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e a configuração de uma propriedade [**\_ TerminalServiceSetting do Win32**](win32-terminalservicesetting.md) específica.

</dd> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dd>

representa as configurações que podem ser aplicadas a um terminal.

</dd> <dt>

[**Terminal Do \_ Win32TerminalSetting**](win32-terminalterminalsetting.md)
</dt> <dd>

representa a associação entre um terminal e suas definições de configuração.

</dd> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> <dd>

permite a exclusão de uma conta que existe no [**\_ Terminal do Win32 e**](win32-terminal.md) a modificação das permissões existentes.

</dd> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> <dd>

define as definições de configuração para a [**classe \_ do Terminal Win32**](win32-terminal.md) relacionada à política de conexão.

</dd> <dt>

[**Win32 \_ TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

Fornece detalhes sobre o servidor de Área de Trabalho Remota licença descoberto.

</dd> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> <dd>

define as definições de configuração para a [**classe \_ do Terminal Win32,**](win32-terminal.md) incluindo a política de programa inicial.

</dd> <dt>

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> <dd>

representa configurações gerais do terminal, como o nível de criptografia e o protocolo de transporte.

</dd> <dt>

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> <dd>

define as definições de configuração para a [**classe \_ do Terminal Win32**](win32-terminal.md) relacionada ao logon do cliente.

</dd> <dt>

[**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

enumera a lista de adaptadores de rede que podem ser configurados para um [**\_ Terminal Win32,**](win32-terminal.md)com base no protocolo terminal e no método de transporte especificados.

</dd> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> <dd>

define várias definições de configuração para a [**classe \_ do Terminal Win32,**](win32-terminal.md) incluindo propriedades relacionadas ao adaptador de rede e o número máximo de conexões permitidas.

</dd> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> <dd>

inclui um método para adicionar novas contas ao terminal e um método para restaurar as permissões padrão para um terminal.

</dd> <dt>

[**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md)
</dt> <dd>

define as definições de configuração de controle remoto para a [**classe \_ do Terminal Win32.**](win32-terminal.md)

</dd> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> <dd>

Define as definições de configuração Conexão de Área de Trabalho Remota Broker (Agente de Conexão de Área de Trabalho Avançada) para a [**classe Win32 \_ TSSessionDirectorySetting.**](win32-tssessiondirectorysetting.md)

</dd> <dt>

[**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md)
</dt> <dd>

Representa a associação entre uma instância da classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e uma instância da classe [**\_ Win32 TSSessionDirectory.**](win32-tssessiondirectory.md)

</dd> <dt>

[**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md)
</dt> <dd>

define definições de configuração para a [**classe \_ do Terminal Win32,**](win32-terminal.md) como limites de tempo e ações de desconexão e reconexão.

</dd> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> <dd>

Define configurações de virtualização de IP (protocolo IP) para um Host da Sessão RD servidor.

</dd> <dt>

[**Win32 \_ TSVirtualIPSetting**](win32-tsvirtualipsetting.md)
</dt> <dd>

Representa a associação entre uma classe de elemento [**Win32 \_ TerminalService**](win32-terminalservice.md) e uma classe de configuração [**\_ Win32 TSVirtualIP.**](win32-tsvirtualip.md)

</dd> </dl>

A ilustração a seguir mostra as relações entre essas classes.

![as relações entre classes com suporte](images/tswmi.png)

 

 