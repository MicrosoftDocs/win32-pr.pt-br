---
title: Classe Win32_TerminalServiceSetting
description: Representa a configuração de um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 4cd047db-921f-4ccb-946b-d2c7b8d6beea
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TerminalServiceSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting.Caption
- Win32_TerminalServiceSetting.Description
- Win32_TerminalServiceSetting.InstallDate
- Win32_TerminalServiceSetting.Name
- Win32_TerminalServiceSetting.Status
- Win32_TerminalServiceSetting.ServerName
- Win32_TerminalServiceSetting.TerminalServerMode
- Win32_TerminalServiceSetting.GetCapabilitiesID
- Win32_TerminalServiceSetting.LicensingType
- Win32_TerminalServiceSetting.PolicySourceLicensingType
- Win32_TerminalServiceSetting.PossibleLicensingTypes
- Win32_TerminalServiceSetting.LicensingName
- Win32_TerminalServiceSetting.LicensingDescription
- Win32_TerminalServiceSetting.ActiveDesktop
- Win32_TerminalServiceSetting.UserPermission
- Win32_TerminalServiceSetting.DeleteTempFolders
- Win32_TerminalServiceSetting.PolicySourceDeleteTempFolders
- Win32_TerminalServiceSetting.UseTempFolders
- Win32_TerminalServiceSetting.PolicySourceUseTempFolders
- Win32_TerminalServiceSetting.AllowTSConnections
- Win32_TerminalServiceSetting.PolicySourceAllowTSConnections
- Win32_TerminalServiceSetting.SingleSession
- Win32_TerminalServiceSetting.PolicySourceSingleSession
- Win32_TerminalServiceSetting.ProfilePath
- Win32_TerminalServiceSetting.PolicySourceProfilePath
- Win32_TerminalServiceSetting.HomeDirectory
- Win32_TerminalServiceSetting.PolicySourceHomeDirectory
- Win32_TerminalServiceSetting.TimeZoneRedirection
- Win32_TerminalServiceSetting.PolicySourceTimeZoneRedirection
- Win32_TerminalServiceSetting.Logons
- Win32_TerminalServiceSetting.DirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceDirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceConfiguredLicenseServers
- Win32_TerminalServiceSetting.DisableForcibleLogoff
- Win32_TerminalServiceSetting.PolicySourceDisableForcibleLogoff
- Win32_TerminalServiceSetting.FallbackPrintDriverType
- Win32_TerminalServiceSetting.PolicySourceFallbackPrintDriverType
- Win32_TerminalServiceSetting.SessionBrokerDrainMode
- Win32_TerminalServiceSetting.LimitedUserSessions
- Win32_TerminalServiceSetting.EnableDFSS
- Win32_TerminalServiceSetting.PolicySourceEnableDFSS
- Win32_TerminalServiceSetting.EnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.PolicySourceEnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.EnableAutomaticReconnection
- Win32_TerminalServiceSetting.PolicySourceEnableAutomaticReconnection
- Win32_TerminalServiceSetting.UseRDEasyPrintDriver
- Win32_TerminalServiceSetting.PolicySourceUseRDEasyPrintDriver
- Win32_TerminalServiceSetting.RedirectSmartCards
- Win32_TerminalServiceSetting.PolicySourceRedirectSmartCards
- Win32_TerminalServiceSetting.EnableDiskFSS
- Win32_TerminalServiceSetting.EnableNetworkFSS
- Win32_TerminalServiceSetting.NetworkFSSUserSessionWeight
- Win32_TerminalServiceSetting.NetworkFSSLocalSystemWeight
- Win32_TerminalServiceSetting.NetworkFSSCatchAllWeight
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a4d7aefdd3f0a684c91fda3ab73d17de32327f34e8d20d5a7f844ea07e21906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769886"
---
# <a name="win32_terminalservicesetting-class"></a>\_Classe Win32 TerminalServiceSetting

A classe WMI **\_ TerminalServiceSetting do Win32** representa a configuração de um servidor de host da sessão da área de trabalho remota (host da Sessão RD). Configurações incluem recursos como Host da Sessão RD modo de servidor, licenciamento, Active Desktop, permissões, exclusão de pastas temporárias e diretórios temporários para sessões.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética. Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICESETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   ServerName;
  uint32   TerminalServerMode;
  uint32   GetCapabilitiesID;
  uint32   LicensingType;
  uint32   PolicySourceLicensingType;
  uint32   PossibleLicensingTypes;
  string   LicensingName;
  string   LicensingDescription;
  uint32   ActiveDesktop;
  uint32   UserPermission;
  uint32   DeleteTempFolders;
  uint32   PolicySourceDeleteTempFolders;
  uint32   UseTempFolders;
  uint32   PolicySourceUseTempFolders;
  uint32   AllowTSConnections;
  uint32   PolicySourceAllowTSConnections;
  uint32   SingleSession;
  uint32   PolicySourceSingleSession;
  string   ProfilePath;
  uint32   PolicySourceProfilePath;
  string   HomeDirectory;
  uint32   PolicySourceHomeDirectory;
  uint32   TimeZoneRedirection;
  uint32   PolicySourceTimeZoneRedirection;
  string   Logons;
  string   DirectConnectLicenseServers;
  uint32   PolicySourceDirectConnectLicenseServers;
  uint32   PolicySourceConfiguredLicenseServers;
  uint32   DisableForcibleLogoff;
  uint32   PolicySourceDisableForcibleLogoff;
  uint32   FallbackPrintDriverType;
  uint32   PolicySourceFallbackPrintDriverType;
  uint32   SessionBrokerDrainMode;
  uint32   LimitedUserSessions;
  uint32   EnableDFSS;
  uint32   PolicySourceEnableDFSS;
  uint32   EnableRemoteDesktopMSI;
  uint32   PolicySourceEnableRemoteDesktopMSI;
  uint32   EnableAutomaticReconnection;
  uint32   PolicySourceEnableAutomaticReconnection;
  uint32   UseRDEasyPrintDriver;
  uint32   PolicySourceUseRDEasyPrintDriver;
  uint32   RedirectSmartCards;
  uint32   PolicySourceRedirectSmartCards;
  uint32   EnableDiskFSS;
  uint32   EnableNetworkFSS;
  uint32   NetworkFSSUserSessionWeight;
  uint32   NetworkFSSLocalSystemWeight;
  uint32   NetworkFSSCatchAllWeight;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TerminalServiceSetting** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TerminalServiceSetting** tem esses métodos.



| Método                                                                                                                | Descrição                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddDirectConnectLicenseServer**](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | Configura um novo servidor de licença na empresa.<br/>                                                                                                                  |
| [**AddLSToSpecifiedLicenseServerList**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | Adiciona o servidor de licença fornecido ao final da lista de servidores de licença especificados.<br/>                                                                                  |
| [**CanAccessLicenseServer**](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | Determina se o servidor de Host da Sessão RD tem permissão para solicitar Serviços de Área de Trabalho Remota licenças de acesso para cliente (RDS CALs) de um servidor de licença Área de Trabalho Remota.<br/> |
| [**ChangeMode**](win32-terminalservicesetting-changemode.md)                                                         | Define o tipo de licenciamento do servidor de licença Área de Trabalho Remota.<br/>                                                                                                       |
| [**CreateWinstation**](createwinstation-win32-terminalservicesetting.md)                                             | Cria uma nova pilha de ouvinte com base na combinação exclusiva de nome do ouvinte e NIC.<br/>                                                                              |
| [**DeleteDirectConnectLicenseServer**](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | Exclui o servidor de licença especificado da empresa.<br/>                                                                                                           |
| [**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | Remove todos os servidores de licença da lista de servidores de licença especificados.<br/>                                                                                             |
| [**FindLicenseServers**](findlicenseservers-win32-terminalservicesetting.md)                                         | Enumera todos os servidores de licença Área de Trabalho Remota e o método de descoberta.<br/>                                                                                   |
| [**GetDomain**](getdomain-win32-terminalservicesetting.md)                                                           | Recupera o nome do domínio do qual o servidor de Host da Sessão RD é membro.<br/>                                                                                    |
| [**GetGracePeriodDays**](getgraceperioddays-win32-terminalservicesetting.md)                                         | Recupera o número de dias restantes no período de carência de Licenciamento RD para um servidor Host da Sessão RD.<br/>                                                     |
| [**GetRegisteredLicenseServerList**](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | Obtém a lista de servidores de licença registrados.<br/>                                                                                                                        |
| [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Recupera a lista de servidores de licença especificados.<br/>                                                                                                                    |
| [**GetTSLanaIds**](gettslanaids-win32-terminalservicesetting.md)                                                     | Obtém as IDs e descrições de Serviços de Área de Trabalho Remota adaptadores de rede.<br/>                                                                                          |
| [**GetTStoLSConnectivityStatus**](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | Determina o status de conectividade entre Serviços de Área de Trabalho Remota e um servidor de licença.<br/>                                                                            |
| [**GetWinstationDriverNames**](getwinstationdrivernames-win32-terminalservicesetting.md)                             | Recupera uma lista de nomes de driver WinStation.<br/>                                                                                                                        |
| [**PingLicenseServer**](pinglicenseserver-win32-terminalservicesetting.md)                                           | Executa ping no servidor de licença para determinar se ele é um servidor de licença válido.<br/>                                                                                         |
| [**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | Remove o servidor de licença fornecido da lista de servidores de licença especificados.<br/>                                                                                        |
| [**SetAllowTSConnections**](win32-terminalservicesetting-setallowtsconnections.md)                                   | Define a propriedade **AllowTSConnections** .<br/>                                                                                                                           |
| [**SetDisableForcibleLogoff**](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | Define a propriedade **DisableForcibleLogoff** .<br/>                                                                                                                        |
| [**SetFallbackPrintDriverType**](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | Define a propriedade **FallbackPrintDriverType** .<br/>                                                                                                                      |
| [**SetHomeDirectory**](win32-terminalservicesetting-sethomedirectory.md)                                             | Define a propriedade **HomeDirectory** .<br/>                                                                                                                                |
| [**SetPolicyPropertyName**](win32-terminalservicesetting-setpolicypropertyname.md)                                   | Define uma das seguintes propriedades: **DeleteTempFolders** ou **UseTempFolders**.<br/>                                                                                  |
| [**SetPrimaryLicenseServer**](setprimarylicenseserver-win32-terminalservicesetting.md)                               | Define o servidor de licença fornecido como a primeira entrada na lista de servidores de licença especificados.<br/>                                                                          |
| [**SetProfilePath**](win32-terminalservicesetting-setprofilepath.md)                                                 | Define a propriedade **ProfilePath** .<br/>                                                                                                                                  |
| [**SetSingleSession**](win32-terminalservicesetting-setsinglesession.md)                                             | Define a propriedade **SingleSession** .<br/>                                                                                                                                |
| [**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Atualiza a lista de servidores de licença especificados, substituindo quaisquer servidores de licença especificados existentes.<br/>                                                                    |
| [**SetTimeZoneRedirection**](win32-terminalservicesetting-settimezoneredirection.md)                                 | Define a propriedade **TimeZoneRedirection** .<br/>                                                                                                                          |
| [**UpdateDirectConnectLicenseServer**](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | Atualiza a lista de servidores de licença de descoberta.<br/>                                                                                                                      |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TerminalServiceSetting** tem essas propriedades.

<dl> <dt>

**ActiveDesktop**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se o Active Desktop é permitido em cada sessão de usuário.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (0)


</dt> <dd>

O Active Desktop não é permitido em cada sessão de usuário.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (1)


</dt> <dd>

O Active Desktop é permitido em cada sessão de usuário.

</dd> </dl>

</dd> <dt>

**AllowTSConnections**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se novas conexões de Serviços de Área de Trabalho Remota são permitidas.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Não são permitidas novas conexões.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

Novas conexões são permitidas.

</dd> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrição (cadeia de caracteres de uma linha) do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DeleteTempFolders**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se os diretórios temporários são excluídos na saída.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

A exclusão de diretórios temporários está desabilitada.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

A exclusão de diretórios temporários está habilitada.

</dd> </dl>

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **PRETERIDO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Essa propriedade não está disponível.

**Windows Server 2008:** Enumera a lista de servidores de licença.

</dd> <dt>

**DisableForcibleLogoff**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Determina se um administrador que está conectado ao console pode ser desconectado à força.

<dt>

0
</dt> <dd>

O administrador pode ser desconectado à força.

</dd> <dt>

1
</dt> <dd>

O administrador não pode ser desconectado à força.

</dd> </dl>

</dd> <dt>

**EnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica se os clientes de conexão Área de Trabalho Remota podem se reconectar automaticamente às sessões em um servidor Host da Sessão RD se o link de rede for temporariamente perdido.

<dt>

0 (0x0)
</dt> <dd>

A reconexão automática está desabilitada.

</dd> <dt>

1 (0x1)
</dt> <dd>

A reconexão automática está habilitada.

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Essa propriedade não está disponível.

</dd> <dt>

**EnableDFSS**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica se o DFSS (agendamento dinâmico de compartilhamento justo) está habilitado ou desabilitado. Esse pode ser um dos valores a seguir.

**Windows Server 2008:** Essa propriedade não está disponível antes Windows Server 2008 R2.

<dt>

0
</dt> <dd>

O DFSS está desabilitado.

</dd> <dt>

1
</dt> <dd>

O DFSS está habilitado.

</dd> </dl>

</dd> <dt>

**EnableDiskFSS**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica se o agendamento de compartilhamento justo de disco está habilitado.

<dt>

0 (0x0)
</dt> <dd>

O agendamento de compartilhamento justo de disco está desabilitado.

</dd> <dt>

1 (0x1)
</dt> <dd>

O agendamento de compartilhamento justo de disco está habilitado.

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Essa propriedade não está disponível.

</dd> <dt>

**EnableNetworkFSS**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica se o agendamento de compartilhamento justo de rede está habilitado.

<dt>

0 (0x0)
</dt> <dd>

O agendamento de compartilhamento justo de rede está desabilitado.

</dd> <dt>

1 (0x1)
</dt> <dd>

O agendamento de compartilhamento justo de rede está habilitado.

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Essa propriedade não está disponível.

</dd> <dt>

**EnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica se a Área de Trabalho Remota MSI está habilitada ou desabilitada.

<dt>

0 (0x0)
</dt> <dd>

Desabilitado

</dd> <dt>

1 (0x1)
</dt> <dd>

habilitado

</dd> </dl>

**Windows Server 2008:** Essa propriedade não está disponível antes Windows Server 2008 R2.

</dd> <dt>

**FallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica para qual driver de impressora fazer fallback.

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Nenhum dirvers=0** de fallback (0)


</dt> <dd>

Nenhum drivers de fallback.

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Melhor suposição=1** (1)


</dt> <dd>

Melhor suposição.

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Melhor suposição: se nenhuma combinação for encontrada, fallback para PCL=2** (2)


</dt> <dd>

Melhor suposição. Se nenhuma combinação for encontrada, fallback para Hewlett-Packard PCL (Printer Control Language).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Melhor suposição: se nenhuma combinação for encontrada, fallback para PS=3** (3)


</dt> <dd>

Melhor suposição. Se nenhuma corresponder for encontrada, fallback para Postscript (PS).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Melhor suposição: se nenhuma combinação for encontrada, mostre os drivers PCL e PS=4** (4)


</dt> <dd>

Melhor suposição. Se nenhuma combinação for encontrada, mostre os drivers PS e PCL.

</dd> </dl>

</dd> <dt>

**GetCapabilitiesID**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

ID de funcionalidades para o provedor.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O diretório raiz do computador.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

A data em que o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LicensingDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do modo de licenciamento.

</dd> <dt>

**Licenciamento**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do modo de licenciamento.

</dd> <dt>

**Licenciamento**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de licenciamento para o modo de servidor especificado.

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Terminal Server pessoais** (0)


</dt> <dd>

Servidor de Host da Sessão RD pessoal.

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Área de trabalho remota para administração** (1)


</dt> <dd>

Área de Trabalho Remota para administração.

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Por dispositivo** (2)


</dt> <dd>

Por dispositivo. Válido para servidores de aplicativos.

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuário** (3)


</dt> <dd>

Por Usuário. Válido para servidores de aplicativos.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (4)


</dt> <dd>

Não configurado.

</dd> </dl>

</dd> <dt>

**LimitedUserSessions**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o recurso para limitar o número de sessões ativas e inativas permitidas em um Host da Sessão RD Server está habilitado. Por exemplo, talvez você queira definir **LimitedUserSessions** para garantir a conformidade de licença para um determinado aplicativo que está instalado no servidor de host da Sessão RD. Ou, talvez você queira limitar o número máximo de sessões em um servidor de Host da Sessão RD em um farm com balanceamento de carga para que o servidor não seja sobrecarregado se outro servidor no farm falhar.

> [!Note]
>
> A sessão usada para se conectar ao servidor para fins administrativos não é afetada pelo **LimitedUserSessions**.
>
> Em um farm de servidores Host da Sessão RD, se um usuário exceder o limite de sessão, a sessão será direcionada para outro servidor pelo balanceamento de carga do agente de conexão RD. Se o servidor for um servidor autônomo, o usuário não poderá se conectar.
>
> Devido à sessão usada para se conectar ao servidor para fins administrativos e o tempo de imposição do número de sessões durante o ciclo de logon, é recomendável que você defina **LimitedUserSessions** com um valor ligeiramente menor que o limite físico para o número de sessões em um servidor.
>
> A propriedade **LimitedUserSessions** só será válida se o serviço de função host da Sessão RD estiver instalado.

 

<dt>

0
</dt> <dd>

O recurso está desabilitado.

</dd> <dt>

1 ou superior
</dt> <dd>

Um valor de um ou mais representa o número máximo de sessões (ativas e inativas) que são permitidas no servidor de Host da Sessão RD.

</dd> </dl>

</dd> <dt>

**Logons**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se novas sessões são permitidas. Essa configuração não afeta as configurações existentes.

<dt>

0
</dt> <dd>

Novas sessões são permitidas.

</dd> <dt>

1
</dt> <dd>

Não são permitidas novas sessões.

</dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**NetworkFSSCatchAllWeight**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica o peso de compartilhamento justa de rede padrão para todo o tráfego de rede. Os valores válidos são de 1 a 9.

**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.

</dd> <dt>

**NetworkFSSLocalSystemWeight**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica o peso de compartilhamento justa de rede padrão para processos de sistema local. Os valores válidos são de 1 a 9.

**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.

</dd> <dt>

**NetworkFSSUserSessionWeight**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica o peso de compartilhamento justa de rede padrão para uma sessão de usuário. Os valores válidos são de 1 a 9.

**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.

</dd> <dt>

**PolicySourceAllowTSConnections**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **AllowTSConnections** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceConfiguredLicenseServers**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se os servidores de licença retornados pelo método [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) são configurados pelo servidor ou pela política de grupo.

**Windows Server 2008:** Esta propriedade não está disponível.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceDeleteTempFolders**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **DeleteTempFolders** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceDirectConnectLicenseServers**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **PRETERIDO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Essa propriedade não está disponível.

**Windows Server 2008:** Indica se a **propriedade DirectConnectLicenseServers** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceDisableForcibleLogoff**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não há suporte a esta propriedade.

**Windows Server 2008:** Determina se a **propriedade DisableForcibleLogoff** está configurada pelo servidor ou pela política de grupo.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de Grupo.

</dd> </dl>

</dd> <dt>

**PolicySourceEnableAutomaticReconnection**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade EnableAutomaticReconnection** está configurada pela política de servidor ou grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Essa propriedade não está disponível.

</dd> <dt>

**PolicySourceEnableDFSSS**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade EnableDFSS** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

**Windows Server 2008:** Essa propriedade não está disponível antes Windows Server 2008 R2.

</dd> <dt>

**PolicySourceEnableRemoteDesktopMSI**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade EnableRemoteDesktopMSI** está configurada pela política de servidor ou grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

**Windows Server 2008:** Essa propriedade não está disponível antes Windows Server 2008 R2.

</dd> <dt>

**PolicySourceFallbackPrintDriverType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade FallbackPrintDriverType** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceHomeDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade HomeDirectory** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceLicensingType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **LicensingType** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceProfilePath**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **ProfilePath** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceRedirectSmartCards**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade RedirectSmartCards** está configurada pela política de servidor ou grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

**Windows Server 2008 R2 e Windows Server 2008:** Essa propriedade não está disponível.

</dd> <dt>

**PolicySourceSingleSession**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **SingleSession** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceTimeZoneRedirection**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **TimeZoneRedirection** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PolicySourceUseRDEasyPrintDriver**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **UseRDEasyPrintDriver** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.

</dd> <dt>

**PolicySourceUseTempFolders**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **UseTempFolders** está configurada pelo servidor ou pela política de grupo.

<dt>

0 (0x0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**PossibleLicensingTypes**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**bitvalues**](/windows/desktop/WmiSdk/standard-qualifiers) ("pessoal Terminal Server", "área de trabalho remota para administração", "por dispositivo", "por usuário", "não configurado")
</dt> </dl>

Um bitmask que especifica os tipos de licenciamento que estão disponíveis. Isso pode ser uma combinação de um ou mais dos valores a seguir.

<dt>

1 (0x1)
</dt> <dd>

Há suporte para licenças do Personal Host da Sessão RD Server.

</dd> <dt>

2 (0x2)
</dt> <dd>

Há suporte para Área de Trabalho Remota licenças.

</dd> <dt>

4 (0x4)
</dt> <dd>

Há suporte para licenças por dispositivo.

</dd> <dt>

8 (0x8)
</dt> <dd>

Há suporte para licenças por usuário.

</dd> </dl>

</dd> <dt>

**Profilepath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do perfil do computador.

</dd> <dt>

**RedirectSmartCards**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se o redirecionamento de dispositivos de cartão inteligente é permitido em uma sessão remota.

<dt>

0 (0x0)
</dt> <dd>

O redirecionamento de dispositivo de cartão inteligente não é permitido.

</dd> <dt>

1 (0x1)
</dt> <dd>

O redirecionamento de dispositivo de cartão inteligente é permitido.

</dd> </dl>

**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome do servidor de Host da Sessão RD cujas propriedades são de interesse.

</dd> <dt>

**SessionBrokerDrainMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O modo de logon do usuário do agente de conexão RD.

<dt>

0
</dt> <dd>

Permitir todas as conexões.

</dd> <dt>

1
</dt> <dd>

Permitir reconexões, mas evitar novos logons até que o servidor seja reiniciado.

</dd> <dt>

2
</dt> <dd>

Permitir reconexões, mas impedir novos logons.

</dd> </dl>

</dd> <dt>

**SingleSession**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se uma ou mais sessões de Serviços de Área de Trabalho Remota são permitidas por usuário.

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)


</dt> <dd>

Mais de uma sessão é permitida por usuário.

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**Verdadeiro** (1)


</dt> <dd>

Somente uma sessão é permitida por usuário.

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Status atual do objeto. Vários status de operação e não operacional podem ser definidos. Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço". O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Erro")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconhecido")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Iniciando")


</dt> <dd></dd> <dt>



 ("Parando")


</dt> <dd></dd> <dt>



 ("Serviço")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalServerMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O modo operacional do servidor Host da Sessão RD do serviço Serviços de Área de Trabalho Remota. Esse modo controla as políticas de licenciamento que são aplicáveis, bem como se os recursos de compatibilidade de aplicativos estão habilitados.

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)


</dt> <dd>

O servidor Opera como um servidor de aplicativos.

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)


</dt> <dd>

A sessão é administrada remotamente.

</dd> </dl>

</dd> <dt>

**TimeZoneRedirection**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o computador cliente pode redirecionar suas configurações de fuso horário para a sessão de Serviços de Área de Trabalho Remota.

<dt>

0
</dt> <dd>

O redirecionamento está desabilitado.

</dd> <dt>

1
</dt> <dd>

O redirecionamento está habilitado.

</dd> </dl>

</dd> <dt>

**UseRDEasyPrintDriver**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se o driver de impressora Easy Print de Área de Trabalho Remota é usado primeiro para instalar todas as impressoras de cliente.

<dt>

0
</dt> <dd>

O Host da Sessão RD Server tenta encontrar um driver de impressora adequado para instalar a impressora do cliente. Se o servidor de Host da Sessão RD não tiver um driver de impressora que corresponda à impressora cliente, o servidor tentará usar o driver Easy Print de Área de Trabalho Remota para instalar a impressora cliente.

</dd> <dt>

1
</dt> <dd>

O Host da Sessão RD Server primeiro tenta usar o driver de impressora Easy Print de Área de Trabalho Remota para instalar todas as impressoras do cliente. Se por algum motivo o driver de impressora Easy Print de Área de Trabalho Remota não puder ser usado, um driver de impressora no servidor Host da Sessão RD que corresponda à impressora cliente será usado.

</dd> </dl>

**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.

</dd> <dt>

**UserPermission**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Especifica se cada sessão de usuário tem segurança rígida ou reduzida.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

A segurança é rígida.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

A segurança é relaxada.

</dd> </dl>

</dd> <dt>

**UseTempFolders**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se os diretórios temporários são criados e excluídos por sessão.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Os diretórios temporários não são criados e excluídos para cada sessão. Uma é criada para a primeira sessão e nunca é excluída.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)


</dt> <dd>

Os diretórios temporários são criados e excluídos para cada sessão.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

**Win32 \_ TerminalServiceSetting** está associado ao [**Win32 \_ TerminalService**](win32-terminalservice.md) como a propriedade **Setting** da Associação [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) é associado ao [**\_ terminal do Win32**](win32-terminal.md) como a propriedade de **configuração** da Associação [**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md) .

Para se conectar ao \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**. para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "pktPrivacy", com um valor de seis.

o exemplo a seguir Visual Basic scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração de CIM \_**](cim-setting.md)
</dt> <dt>

[**Terminal do Win32 \_**](win32-terminal.md)
</dt> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dt>

[**\_TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md)
</dt> <dt>

[**\_TerminalTerminalSetting Win32**](win32-terminalterminalsetting.md)
</dt> <dt>

[**Configuração de CIM \_**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

