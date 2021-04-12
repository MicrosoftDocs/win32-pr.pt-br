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
ms.openlocfilehash: bc03f02028a331a3688152a1ce8c57ada7269d07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295871"
---
# <a name="win32_terminalservicesetting-class"></a><span data-ttu-id="f6500-105">\_Classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="f6500-105">Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f6500-106">A classe WMI **\_ TerminalServiceSetting do Win32** representa a configuração de um servidor de host da sessão da área de trabalho remota (host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="f6500-106">The **Win32\_TerminalServiceSetting** WMI class represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="f6500-107">As configurações incluem recursos como Host da Sessão RD modo de servidor, licenciamento, Active Desktop, permissões, exclusão de pastas temporárias e diretórios temporários para sessões.</span><span class="sxs-lookup"><span data-stu-id="f6500-107">Settings include capabilities such as RD Session Host server mode, licensing, Active Desktop, permissions, deletion of temporary folders, and temporary directories for sessions.</span></span>

<span data-ttu-id="f6500-108">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="f6500-108">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="f6500-109">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="f6500-109">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6500-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6500-110">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="f6500-111">Membros</span><span class="sxs-lookup"><span data-stu-id="f6500-111">Members</span></span>

<span data-ttu-id="f6500-112">A classe **Win32 \_ TerminalServiceSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f6500-112">The **Win32\_TerminalServiceSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="f6500-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f6500-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="f6500-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f6500-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f6500-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="f6500-115">Methods</span></span>

<span data-ttu-id="f6500-116">A classe **Win32 \_ TerminalServiceSetting** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f6500-116">The **Win32\_TerminalServiceSetting** class has these methods.</span></span>



| <span data-ttu-id="f6500-117">Método</span><span class="sxs-lookup"><span data-stu-id="f6500-117">Method</span></span>                                                                                                                | <span data-ttu-id="f6500-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6500-118">Description</span></span>                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6500-119">**AddDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="f6500-119">**AddDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | <span data-ttu-id="f6500-120">Configura um novo servidor de licença na empresa.</span><span class="sxs-lookup"><span data-stu-id="f6500-120">Configures a new license server in the enterprise.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="f6500-121">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="f6500-121">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | <span data-ttu-id="f6500-122">Adiciona o servidor de licença fornecido ao final da lista de servidores de licença especificados.</span><span class="sxs-lookup"><span data-stu-id="f6500-122">Adds the given license server to the end of the list of specified license servers.</span></span><br/>                                                                                  |
| [<span data-ttu-id="f6500-123">**CanAccessLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="f6500-123">**CanAccessLicenseServer**</span></span>](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | <span data-ttu-id="f6500-124">Determina se o servidor de Host da Sessão RD tem permissão para solicitar Serviços de Área de Trabalho Remota licenças de acesso para cliente (RDS CALs) de um servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="f6500-124">Determines whether the RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="f6500-125">**ChangeMode**</span><span class="sxs-lookup"><span data-stu-id="f6500-125">**ChangeMode**</span></span>](win32-terminalservicesetting-changemode.md)                                                         | <span data-ttu-id="f6500-126">Define o tipo de licenciamento do servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="f6500-126">Sets the licensing type of the Remote Desktop license server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="f6500-127">**CreateWinstation**</span><span class="sxs-lookup"><span data-stu-id="f6500-127">**CreateWinstation**</span></span>](createwinstation-win32-terminalservicesetting.md)                                             | <span data-ttu-id="f6500-128">Cria uma nova pilha de ouvinte com base na combinação exclusiva de nome do ouvinte e NIC.</span><span class="sxs-lookup"><span data-stu-id="f6500-128">Creates a new listener stack based on the unique combination of listener name and NIC.</span></span><br/>                                                                              |
| [<span data-ttu-id="f6500-129">**DeleteDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="f6500-129">**DeleteDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | <span data-ttu-id="f6500-130">Exclui o servidor de licença especificado da empresa.</span><span class="sxs-lookup"><span data-stu-id="f6500-130">Deletes the specified license server from the enterprise.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="f6500-131">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="f6500-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | <span data-ttu-id="f6500-132">Remove todos os servidores de licença da lista de servidores de licença especificados.</span><span class="sxs-lookup"><span data-stu-id="f6500-132">Removes all license servers from the list of specified license servers.</span></span><br/>                                                                                             |
| [<span data-ttu-id="f6500-133">**FindLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="f6500-133">**FindLicenseServers**</span></span>](findlicenseservers-win32-terminalservicesetting.md)                                         | <span data-ttu-id="f6500-134">Enumera todos os servidores de licença Área de Trabalho Remota e o método de descoberta.</span><span class="sxs-lookup"><span data-stu-id="f6500-134">Enumerates all of the Remote Desktop license servers and the method of discovery.</span></span><br/>                                                                                   |
| [<span data-ttu-id="f6500-135">**GetDomain**</span><span class="sxs-lookup"><span data-stu-id="f6500-135">**GetDomain**</span></span>](getdomain-win32-terminalservicesetting.md)                                                           | <span data-ttu-id="f6500-136">Recupera o nome do domínio do qual o servidor de Host da Sessão RD é membro.</span><span class="sxs-lookup"><span data-stu-id="f6500-136">Retrieves the name of the domain that the RD Session Host server is a member of.</span></span><br/>                                                                                    |
| [<span data-ttu-id="f6500-137">**GetGracePeriodDays**</span><span class="sxs-lookup"><span data-stu-id="f6500-137">**GetGracePeriodDays**</span></span>](getgraceperioddays-win32-terminalservicesetting.md)                                         | <span data-ttu-id="f6500-138">Recupera o número de dias restantes no período de carência de Licenciamento RD para um servidor Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="f6500-138">Retrieves the number of days that are remaining in the RD Licensing grace period for an RD Session Host server.</span></span><br/>                                                     |
| [<span data-ttu-id="f6500-139">**GetRegisteredLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="f6500-139">**GetRegisteredLicenseServerList**</span></span>](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | <span data-ttu-id="f6500-140">Obtém a lista de servidores de licença registrados.</span><span class="sxs-lookup"><span data-stu-id="f6500-140">Gets the list of registered license servers.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="f6500-141">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="f6500-141">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="f6500-142">Recupera a lista de servidores de licença especificados.</span><span class="sxs-lookup"><span data-stu-id="f6500-142">Retrieves the list of specified license servers.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="f6500-143">**GetTSLanaIds**</span><span class="sxs-lookup"><span data-stu-id="f6500-143">**GetTSLanaIds**</span></span>](gettslanaids-win32-terminalservicesetting.md)                                                     | <span data-ttu-id="f6500-144">Obtém as IDs e descrições de Serviços de Área de Trabalho Remota adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="f6500-144">Gets the IDs and descriptions of Remote Desktop Services network adapters.</span></span><br/>                                                                                          |
| [<span data-ttu-id="f6500-145">**GetTStoLSConnectivityStatus**</span><span class="sxs-lookup"><span data-stu-id="f6500-145">**GetTStoLSConnectivityStatus**</span></span>](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | <span data-ttu-id="f6500-146">Determina o status de conectividade entre Serviços de Área de Trabalho Remota e um servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="f6500-146">Determines the connectivity status between Remote Desktop Services and a license server.</span></span><br/>                                                                            |
| [<span data-ttu-id="f6500-147">**GetWinstationDriverNames**</span><span class="sxs-lookup"><span data-stu-id="f6500-147">**GetWinstationDriverNames**</span></span>](getwinstationdrivernames-win32-terminalservicesetting.md)                             | <span data-ttu-id="f6500-148">Recupera uma lista de nomes de driver WinStation.</span><span class="sxs-lookup"><span data-stu-id="f6500-148">Retrieves a list of Winstation driver names.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="f6500-149">**PingLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="f6500-149">**PingLicenseServer**</span></span>](pinglicenseserver-win32-terminalservicesetting.md)                                           | <span data-ttu-id="f6500-150">Executa ping no servidor de licença para determinar se ele é um servidor de licença válido.</span><span class="sxs-lookup"><span data-stu-id="f6500-150">Pings the license server to determine whether it is a valid license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="f6500-151">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="f6500-151">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | <span data-ttu-id="f6500-152">Remove o servidor de licença fornecido da lista de servidores de licença especificados.</span><span class="sxs-lookup"><span data-stu-id="f6500-152">Removes the given license server from the list of specified license servers.</span></span><br/>                                                                                        |
| [<span data-ttu-id="f6500-153">**SetAllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="f6500-153">**SetAllowTSConnections**</span></span>](win32-terminalservicesetting-setallowtsconnections.md)                                   | <span data-ttu-id="f6500-154">Define a propriedade **AllowTSConnections** .</span><span class="sxs-lookup"><span data-stu-id="f6500-154">Sets the **AllowTSConnections** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="f6500-155">**SetDisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="f6500-155">**SetDisableForcibleLogoff**</span></span>](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | <span data-ttu-id="f6500-156">Define a propriedade **DisableForcibleLogoff** .</span><span class="sxs-lookup"><span data-stu-id="f6500-156">Sets the **DisableForcibleLogoff** property.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="f6500-157">**SetFallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="f6500-157">**SetFallbackPrintDriverType**</span></span>](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | <span data-ttu-id="f6500-158">Define a propriedade **FallbackPrintDriverType** .</span><span class="sxs-lookup"><span data-stu-id="f6500-158">Sets the **FallbackPrintDriverType** property.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="f6500-159">**SetHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="f6500-159">**SetHomeDirectory**</span></span>](win32-terminalservicesetting-sethomedirectory.md)                                             | <span data-ttu-id="f6500-160">Define a propriedade **HomeDirectory** .</span><span class="sxs-lookup"><span data-stu-id="f6500-160">Sets the **HomeDirectory** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="f6500-161">**SetPolicyPropertyName**</span><span class="sxs-lookup"><span data-stu-id="f6500-161">**SetPolicyPropertyName**</span></span>](win32-terminalservicesetting-setpolicypropertyname.md)                                   | <span data-ttu-id="f6500-162">Define uma das seguintes propriedades: **DeleteTempFolders** ou **UseTempFolders**.</span><span class="sxs-lookup"><span data-stu-id="f6500-162">Sets one of the following properties: **DeleteTempFolders** or **UseTempFolders**.</span></span><br/>                                                                                  |
| [<span data-ttu-id="f6500-163">**SetPrimaryLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="f6500-163">**SetPrimaryLicenseServer**</span></span>](setprimarylicenseserver-win32-terminalservicesetting.md)                               | <span data-ttu-id="f6500-164">Define o servidor de licença fornecido como a primeira entrada na lista de servidores de licença especificados.</span><span class="sxs-lookup"><span data-stu-id="f6500-164">Sets the given license server as the first entry in the list of specified license servers.</span></span><br/>                                                                          |
| [<span data-ttu-id="f6500-165">**SetProfilePath**</span><span class="sxs-lookup"><span data-stu-id="f6500-165">**SetProfilePath**</span></span>](win32-terminalservicesetting-setprofilepath.md)                                                 | <span data-ttu-id="f6500-166">Define a propriedade **ProfilePath** .</span><span class="sxs-lookup"><span data-stu-id="f6500-166">Sets the **ProfilePath** property.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="f6500-167">**SetSingleSession**</span><span class="sxs-lookup"><span data-stu-id="f6500-167">**SetSingleSession**</span></span>](win32-terminalservicesetting-setsinglesession.md)                                             | <span data-ttu-id="f6500-168">Define a propriedade **SingleSession** .</span><span class="sxs-lookup"><span data-stu-id="f6500-168">Sets the **SingleSession** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="f6500-169">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="f6500-169">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="f6500-170">Atualiza a lista de servidores de licença especificados, substituindo quaisquer servidores de licença especificados existentes.</span><span class="sxs-lookup"><span data-stu-id="f6500-170">Updates the list of specified license servers, replacing any existing specified license servers.</span></span><br/>                                                                    |
| [<span data-ttu-id="f6500-171">**SetTimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="f6500-171">**SetTimeZoneRedirection**</span></span>](win32-terminalservicesetting-settimezoneredirection.md)                                 | <span data-ttu-id="f6500-172">Define a propriedade **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="f6500-172">Sets the **TimeZoneRedirection** property.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="f6500-173">**UpdateDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="f6500-173">**UpdateDirectConnectLicenseServer**</span></span>](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | <span data-ttu-id="f6500-174">Atualiza a lista de servidores de licença de descoberta.</span><span class="sxs-lookup"><span data-stu-id="f6500-174">Updates the list of discovery license servers.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="f6500-175">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f6500-175">Properties</span></span>

<span data-ttu-id="f6500-176">A classe **Win32 \_ TerminalServiceSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f6500-176">The **Win32\_TerminalServiceSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6500-177">**ActiveDesktop**</span><span class="sxs-lookup"><span data-stu-id="f6500-177">**ActiveDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-178">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-179">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-180">Especifica se o Active Desktop é permitido em cada sessão de usuário.</span><span class="sxs-lookup"><span data-stu-id="f6500-180">Specifies whether Active Desktop is allowed in each user session.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="f6500-181"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (0)</span><span class="sxs-lookup"><span data-stu-id="f6500-181"><span id="TRUE"></span><span id="true"></span>**TRUE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-182">O Active Desktop não é permitido em cada sessão de usuário.</span><span class="sxs-lookup"><span data-stu-id="f6500-182">Active Desktop is not allowed in each user session.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="f6500-183"><span id="FALSE"></span><span id="false"></span>**False** (1)</span><span class="sxs-lookup"><span data-stu-id="f6500-183"><span id="FALSE"></span><span id="false"></span>**FALSE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-184">O Active Desktop é permitido em cada sessão de usuário.</span><span class="sxs-lookup"><span data-stu-id="f6500-184">Active Desktop is allowed in each user session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-185">**AllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="f6500-185">**AllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-186">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-188">Especifica se novas conexões de Serviços de Área de Trabalho Remota são permitidas.</span><span class="sxs-lookup"><span data-stu-id="f6500-188">Specifies whether new Remote Desktop Services connections are allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="f6500-189"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="f6500-189"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-190">Não são permitidas novas conexões.</span><span class="sxs-lookup"><span data-stu-id="f6500-190">New connections are not allowed.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="f6500-191"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="f6500-191"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-192">Novas conexões são permitidas.</span><span class="sxs-lookup"><span data-stu-id="f6500-192">New connections are allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-193">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="f6500-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f6500-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6500-196">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f6500-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f6500-197">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="f6500-197">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f6500-198">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f6500-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6500-199">**DeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="f6500-199">**DeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-200">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-202">Especifica se os diretórios temporários são excluídos ao sair.</span><span class="sxs-lookup"><span data-stu-id="f6500-202">Specifies whether temporary directories are deleted on exit.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="f6500-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="f6500-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-204">A exclusão de diretórios temporários está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f6500-204">Deletion of temporary directories is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="f6500-205"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="f6500-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-206">A exclusão de diretórios temporários está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f6500-206">Deletion of temporary directories is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-207">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f6500-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f6500-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-210">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="f6500-210">Description of the object.</span></span>

<span data-ttu-id="f6500-211">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f6500-211">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6500-212">**DirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="f6500-212">**DirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f6500-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6500-215">Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f6500-215">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f6500-216">Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-216">This property is not available.</span></span>

<span data-ttu-id="f6500-217">**Windows Server 2008:** Enumera a lista de servidores de licença.</span><span class="sxs-lookup"><span data-stu-id="f6500-217">**Windows Server 2008:** Enumerates the list of license servers.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-218">**DisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="f6500-218">**DisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-219">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-219">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-221">Determina se um administrador que está conectado ao console pode ser forçado a desconectar.</span><span class="sxs-lookup"><span data-stu-id="f6500-221">Determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span data-ttu-id="f6500-222">0</span><span class="sxs-lookup"><span data-stu-id="f6500-222">0</span></span>
</dt> <dd>

<span data-ttu-id="f6500-223">O administrador pode ser forçado a desconectar.</span><span class="sxs-lookup"><span data-stu-id="f6500-223">Administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-224">1</span><span class="sxs-lookup"><span data-stu-id="f6500-224">1</span></span>
</dt> <dd>

<span data-ttu-id="f6500-225">Não é possível efetuar logoff forçado do administrador.</span><span class="sxs-lookup"><span data-stu-id="f6500-225">Administrator cannot be forcibly logged off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-226">**EnableAutomaticReconnection**</span><span class="sxs-lookup"><span data-stu-id="f6500-226">**EnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-227">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-228">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-229">Especifica se os clientes de conexão Área de Trabalho Remota devem ser permitidos para se reconectarem automaticamente a sessões em um servidor Host da Sessão RD se o link de rede for perdido temporariamente.</span><span class="sxs-lookup"><span data-stu-id="f6500-229">Specifies whether to allow Remote Desktop connection clients to automatically reconnect to sessions on an RD Session Host server if the network link is temporarily lost.</span></span>

<dt>

<span data-ttu-id="f6500-230">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-230">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-231">A reconexão automática está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f6500-231">Automatic reconnection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-232">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-232">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-233">A reconexão automática está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f6500-233">Automatic reconnection is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="f6500-234">**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-234">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-235">**EnableDFSS**</span><span class="sxs-lookup"><span data-stu-id="f6500-235">**EnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-236">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-237">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-238">Indica se o agendamento de Fair-share dinâmico (DFSS) está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-238">Indicates whether dynamic fair-share scheduling (DFSS) is enabled or disabled.</span></span> <span data-ttu-id="f6500-239">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6500-239">This can be one of the following values.</span></span>

<span data-ttu-id="f6500-240">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f6500-240">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="f6500-241">0</span><span class="sxs-lookup"><span data-stu-id="f6500-241">0</span></span>
</dt> <dd>

<span data-ttu-id="f6500-242">DFSS está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-242">DFSS is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-243">1</span><span class="sxs-lookup"><span data-stu-id="f6500-243">1</span></span>
</dt> <dd>

<span data-ttu-id="f6500-244">DFSS está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-244">DFSS is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-245">**EnableDiskFSS**</span><span class="sxs-lookup"><span data-stu-id="f6500-245">**EnableDiskFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-246">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-247">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-247">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-248">Especifica se o agendamento de compartilhamento justa de disco está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-248">Specifies if disk fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="f6500-249">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-249">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-250">O agendamento do fair share do disco está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-250">Disk fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-251">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-251">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-252">O agendamento do fair share de disco está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-252">Disk fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="f6500-253">**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-253">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-254">**EnableNetworkFSS**</span><span class="sxs-lookup"><span data-stu-id="f6500-254">**EnableNetworkFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-255">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-256">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-256">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-257">Especifica se o agendamento de compartilhamento justa de rede está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-257">Specifies if network fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="f6500-258">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-258">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-259">O agendamento do fair share de rede está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-259">Network fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-260">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-260">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-261">O agendamento do fair share de rede está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-261">Network fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="f6500-262">**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-262">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-263">**EnableRemoteDesktopMSI**</span><span class="sxs-lookup"><span data-stu-id="f6500-263">**EnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-264">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-265">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-266">Indica se a Área de Trabalho Remota MSI está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f6500-266">Indicates whether the Remote Desktop MSI is enabled or disabled.</span></span>

<dt>

<span data-ttu-id="f6500-267">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-267">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-268">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="f6500-268">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="f6500-269">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-269">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-270">habilitado</span><span class="sxs-lookup"><span data-stu-id="f6500-270">Enabled</span></span>

</dd> </dl>

<span data-ttu-id="f6500-271">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f6500-271">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-272">**FallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="f6500-272">**FallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-273">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-275">Especifica para qual driver de impressora fazer fallback.</span><span class="sxs-lookup"><span data-stu-id="f6500-275">Specifies which printer driver to fallback to.</span></span>

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span data-ttu-id="f6500-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Sem dirvers de fallback = 0** (0)</span><span class="sxs-lookup"><span data-stu-id="f6500-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**No fallback dirvers=0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-277">Nenhum driver de fallback.</span><span class="sxs-lookup"><span data-stu-id="f6500-277">No fallback drivers.</span></span>

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span data-ttu-id="f6500-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Melhor estimativa = 1** (1)</span><span class="sxs-lookup"><span data-stu-id="f6500-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Best guess=1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-279">Melhor estimativa.</span><span class="sxs-lookup"><span data-stu-id="f6500-279">Best guess.</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span data-ttu-id="f6500-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Melhor estimativa, se nenhuma correspondência for encontrada para fallback para PCL = 2** (2)</span><span class="sxs-lookup"><span data-stu-id="f6500-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Best guess, if no match is found fallback to PCL=2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-281">Melhor estimativa.</span><span class="sxs-lookup"><span data-stu-id="f6500-281">Best guess.</span></span> <span data-ttu-id="f6500-282">Se nenhuma correspondência for encontrada, fallback para Hewlett-Packard PCL (linguagem de controle de impressora).</span><span class="sxs-lookup"><span data-stu-id="f6500-282">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span data-ttu-id="f6500-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Melhor estimativa, se nenhuma correspondência for encontrada para o PS = 3** (3)</span><span class="sxs-lookup"><span data-stu-id="f6500-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Best guess, if no match is found fallback to PS=3** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-284">Melhor estimativa.</span><span class="sxs-lookup"><span data-stu-id="f6500-284">Best guess.</span></span> <span data-ttu-id="f6500-285">Se nenhuma correspondência for encontrada, fallback para o PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="f6500-285">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span data-ttu-id="f6500-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Melhor estimativa, se nenhuma correspondência for encontrada, mostrar drivers PCL e PS = 4** (4)</span><span class="sxs-lookup"><span data-stu-id="f6500-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Best guess, if no match is found show both PCL and PS drivers=4** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-287">Melhor estimativa.</span><span class="sxs-lookup"><span data-stu-id="f6500-287">Best guess.</span></span> <span data-ttu-id="f6500-288">Se nenhuma correspondência for encontrada, mostre os drivers PS e PCL.</span><span class="sxs-lookup"><span data-stu-id="f6500-288">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-289">**Getcapabilitiesid**</span><span class="sxs-lookup"><span data-stu-id="f6500-289">**GetCapabilitiesID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-290">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-292">ID de recursos para o provedor.</span><span class="sxs-lookup"><span data-stu-id="f6500-292">Capabilities ID for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-293">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="f6500-293">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-294">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f6500-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-296">O diretório raiz do computador.</span><span class="sxs-lookup"><span data-stu-id="f6500-296">The root directory for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f6500-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-298">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f6500-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6500-300">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="f6500-300">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f6500-301">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="f6500-301">The date the object was installed.</span></span> <span data-ttu-id="f6500-302">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="f6500-302">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f6500-303">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f6500-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6500-304">**LicensingDescription**</span><span class="sxs-lookup"><span data-stu-id="f6500-304">**LicensingDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-305">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f6500-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-307">Uma breve descrição do modo de licenciamento.</span><span class="sxs-lookup"><span data-stu-id="f6500-307">A brief description of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-308">**Licenciamento**</span><span class="sxs-lookup"><span data-stu-id="f6500-308">**LicensingName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f6500-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-311">O nome do modo de licenciamento.</span><span class="sxs-lookup"><span data-stu-id="f6500-311">The name of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-312">**Licenciamento**</span><span class="sxs-lookup"><span data-stu-id="f6500-312">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-313">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-315">O tipo de licenciamento para o modo de servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="f6500-315">The licensing type for the specified server mode.</span></span>

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span data-ttu-id="f6500-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Terminal Server pessoais** (0)</span><span class="sxs-lookup"><span data-stu-id="f6500-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Personal Terminal Server** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-317">Servidor de Host da Sessão RD pessoal.</span><span class="sxs-lookup"><span data-stu-id="f6500-317">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span data-ttu-id="f6500-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Área de trabalho remota para administração** (1)</span><span class="sxs-lookup"><span data-stu-id="f6500-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Remote Desktop for Administration** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-319">Área de Trabalho Remota para administração.</span><span class="sxs-lookup"><span data-stu-id="f6500-319">Remote Desktop for Administration.</span></span>

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="f6500-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Por dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="f6500-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Per Device** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-321">Por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6500-321">Per Device.</span></span> <span data-ttu-id="f6500-322">Válido para servidores de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f6500-322">Valid for application servers.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="f6500-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuário** (3)</span><span class="sxs-lookup"><span data-stu-id="f6500-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-324">Por Usuário.</span><span class="sxs-lookup"><span data-stu-id="f6500-324">Per User.</span></span> <span data-ttu-id="f6500-325">Válido para servidores de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f6500-325">Valid for application servers.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f6500-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (4)</span><span class="sxs-lookup"><span data-stu-id="f6500-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-327">Não configurado.</span><span class="sxs-lookup"><span data-stu-id="f6500-327">Not Configured.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-328">**LimitedUserSessions**</span><span class="sxs-lookup"><span data-stu-id="f6500-328">**LimitedUserSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-329">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-330">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-330">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-331">Indica se o recurso para limitar o número de sessões ativas e inativas permitidas em um Host da Sessão RD Server está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-331">Indicates whether the feature to limit the number of both active and inactive sessions that are allowed on an RD Session Host server is enabled.</span></span> <span data-ttu-id="f6500-332">Por exemplo, talvez você queira definir **LimitedUserSessions** para garantir a conformidade de licença para um determinado aplicativo que está instalado no servidor de host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="f6500-332">For example, you may want to set **LimitedUserSessions** to guarantee license compliance for a particular application that is installed on the RD Session Host server.</span></span> <span data-ttu-id="f6500-333">Ou, talvez você queira limitar o número máximo de sessões em um servidor de Host da Sessão RD em um farm com balanceamento de carga para que o servidor não seja sobrecarregado se outro servidor no farm falhar.</span><span class="sxs-lookup"><span data-stu-id="f6500-333">Or, you may want to limit the maximum number of sessions on an RD Session Host server in a load-balanced farm so that the server will not be overloaded if another server in the farm fails.</span></span>

> [!Note]
>
> <span data-ttu-id="f6500-334">A sessão usada para se conectar ao servidor para fins administrativos não é afetada pelo **LimitedUserSessions**.</span><span class="sxs-lookup"><span data-stu-id="f6500-334">The session that is used to connect to the server for administrative purposes is not affected by **LimitedUserSessions**.</span></span>
>
> <span data-ttu-id="f6500-335">Em um farm de servidores Host da Sessão RD, se um usuário exceder o limite de sessão, a sessão será direcionada para outro servidor pelo balanceamento de carga do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="f6500-335">In an RD Session Host server farm, if a user exceeds the session limit, the session will be directed to another server by RD Connection Broker load balancing.</span></span> <span data-ttu-id="f6500-336">Se o servidor for um servidor autônomo, o usuário não poderá se conectar.</span><span class="sxs-lookup"><span data-stu-id="f6500-336">If the server is a stand-alone server, the user will not be able to connect.</span></span>
>
> <span data-ttu-id="f6500-337">Devido à sessão usada para se conectar ao servidor para fins administrativos e o tempo de imposição do número de sessões durante o ciclo de logon, é recomendável que você defina **LimitedUserSessions** com um valor ligeiramente menor que o limite físico para o número de sessões em um servidor.</span><span class="sxs-lookup"><span data-stu-id="f6500-337">Because of the session that is used to connect to the server for administrative purposes, and the timing of the enforcement of the number of sessions during the logon cycle, it is recommended that you set **LimitedUserSessions** to a value that is slightly lower that the physical limit for the number of sessions on a server.</span></span>
>
> <span data-ttu-id="f6500-338">A propriedade **LimitedUserSessions** só será válida se o serviço de função host da Sessão RD estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="f6500-338">The **LimitedUserSessions** property is only valid if the RD Session Host role service is installed.</span></span>

 

<dt>

<span data-ttu-id="f6500-339">0</span><span class="sxs-lookup"><span data-stu-id="f6500-339">0</span></span>
</dt> <dd>

<span data-ttu-id="f6500-340">O recurso está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-340">The feature is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-341">1 ou superior</span><span class="sxs-lookup"><span data-stu-id="f6500-341">1 or greater</span></span>
</dt> <dd>

<span data-ttu-id="f6500-342">Um valor de um ou mais representa o número máximo de sessões (ativas e inativas) que são permitidas no servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="f6500-342">A value of one or greater represents the maximum number of sessions (both active and inactive) that are allowed on the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-343">**Logons**</span><span class="sxs-lookup"><span data-stu-id="f6500-343">**Logons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-344">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f6500-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-345">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-345">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-346">Especifica se novas sessões são permitidas.</span><span class="sxs-lookup"><span data-stu-id="f6500-346">Specifies whether new sessions are allowed.</span></span> <span data-ttu-id="f6500-347">Essa configuração não afeta as configurações existentes.</span><span class="sxs-lookup"><span data-stu-id="f6500-347">This setting does not affect existing settings.</span></span>

<dt>

<span data-ttu-id="f6500-348">0</span><span class="sxs-lookup"><span data-stu-id="f6500-348">0</span></span>
</dt> <dd>

<span data-ttu-id="f6500-349">Novas sessões são permitidas.</span><span class="sxs-lookup"><span data-stu-id="f6500-349">New sessions are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-350">1</span><span class="sxs-lookup"><span data-stu-id="f6500-350">1</span></span>
</dt> <dd>

<span data-ttu-id="f6500-351">Não são permitidas novas sessões.</span><span class="sxs-lookup"><span data-stu-id="f6500-351">New sessions are not allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-352">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f6500-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f6500-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-355">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="f6500-355">The name of the object.</span></span>

<span data-ttu-id="f6500-356">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f6500-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6500-357">**NetworkFSSCatchAllWeight**</span><span class="sxs-lookup"><span data-stu-id="f6500-357">**NetworkFSSCatchAllWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-358">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-359">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-359">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-360">Especifica o peso de compartilhamento justa de rede padrão para todo o tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="f6500-360">Specifies the default network fair share weight for catch-all network traffic.</span></span> <span data-ttu-id="f6500-361">Os valores válidos são de 1 a 9.</span><span class="sxs-lookup"><span data-stu-id="f6500-361">Valid values are 1 to 9.</span></span>

<span data-ttu-id="f6500-362">**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-362">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-363">**NetworkFSSLocalSystemWeight**</span><span class="sxs-lookup"><span data-stu-id="f6500-363">**NetworkFSSLocalSystemWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-364">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-365">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-365">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-366">Especifica o peso de compartilhamento justa de rede padrão para processos de sistema local.</span><span class="sxs-lookup"><span data-stu-id="f6500-366">Specifies the default network fair share weight for a local system processes.</span></span> <span data-ttu-id="f6500-367">Os valores válidos são de 1 a 9.</span><span class="sxs-lookup"><span data-stu-id="f6500-367">Valid values are 1 to 9.</span></span>

<span data-ttu-id="f6500-368">**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-368">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-369">**NetworkFSSUserSessionWeight**</span><span class="sxs-lookup"><span data-stu-id="f6500-369">**NetworkFSSUserSessionWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-370">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-371">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-371">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-372">Especifica o peso de compartilhamento justa de rede padrão para uma sessão de usuário.</span><span class="sxs-lookup"><span data-stu-id="f6500-372">Specifies the default network fair share weight for a user session.</span></span> <span data-ttu-id="f6500-373">Os valores válidos são de 1 a 9.</span><span class="sxs-lookup"><span data-stu-id="f6500-373">Valid values are 1 to 9.</span></span>

<span data-ttu-id="f6500-374">**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-374">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-375">**PolicySourceAllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="f6500-375">**PolicySourceAllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-376">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-378">Indica se a propriedade **AllowTSConnections** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-378">Indicates whether the **AllowTSConnections** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-379">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-379">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-380">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-380">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-381">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-381">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-382">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-382">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-383">**PolicySourceConfiguredLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="f6500-383">**PolicySourceConfiguredLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-384">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-384">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-386">Indica se os servidores de licença retornados pelo método [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) são configurados pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-386">Indicates whether the license servers returned by the [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) method are configured by the server or by group policy.</span></span>

<span data-ttu-id="f6500-387">**Windows Server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-387">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="f6500-388">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-388">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-389">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-389">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-390">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-390">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-391">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-391">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-392">**PolicySourceDeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="f6500-392">**PolicySourceDeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-393">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-395">Indica se a propriedade **DeleteTempFolders** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-395">Indicates whether the **DeleteTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-396">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-396">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-397">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-397">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-398">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-398">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-399">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-399">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-400">**PolicySourceDirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="f6500-400">**PolicySourceDirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-401">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-401">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6500-403">Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f6500-403">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f6500-404">Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-404">This property is not available.</span></span>

<span data-ttu-id="f6500-405">**Windows Server 2008:** Indica se a propriedade **DirectConnectLicenseServers** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-405">**Windows Server 2008:** Indicates whether the **DirectConnectLicenseServers** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-406">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-406">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-407">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-407">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-408">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-408">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-409">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-409">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-410">**PolicySourceDisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="f6500-410">**PolicySourceDisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-411">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-412">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-413">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="f6500-413">This property is not supported.</span></span>

<span data-ttu-id="f6500-414">**Windows Server 2008:** Determina se a propriedade **DisableForcibleLogoff** é configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-414">**Windows Server 2008:** Determines whether the **DisableForcibleLogoff** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-415">0</span><span class="sxs-lookup"><span data-stu-id="f6500-415">0</span></span>
</dt> <dd>

<span data-ttu-id="f6500-416">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-416">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-417">1</span><span class="sxs-lookup"><span data-stu-id="f6500-417">1</span></span>
</dt> <dd>

<span data-ttu-id="f6500-418">Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-418">Group Policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-419">**PolicySourceEnableAutomaticReconnection**</span><span class="sxs-lookup"><span data-stu-id="f6500-419">**PolicySourceEnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-420">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-422">Indica se a propriedade **EnableAutomaticReconnection** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-422">Indicates whether the **EnableAutomaticReconnection** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="f6500-423">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-424">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-426">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-426">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="f6500-427">**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-427">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-428">**PolicySourceEnableDFSS**</span><span class="sxs-lookup"><span data-stu-id="f6500-428">**PolicySourceEnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-429">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-431">Indica se a propriedade **EnableDFSS** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-431">Indicates whether the **EnableDFSS** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-432">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-432">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-433">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-433">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-434">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-434">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-435">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-435">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="f6500-436">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f6500-436">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-437">**PolicySourceEnableRemoteDesktopMSI**</span><span class="sxs-lookup"><span data-stu-id="f6500-437">**PolicySourceEnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-438">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-439">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-440">Indica se a propriedade **EnableRemoteDesktopMSI** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-440">Indicates whether the **EnableRemoteDesktopMSI** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="f6500-441">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-441">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-442">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-442">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-443">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-443">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-444">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-444">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="f6500-445">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f6500-445">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-446">**PolicySourceFallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="f6500-446">**PolicySourceFallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-447">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-447">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-448">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-449">Indica se a propriedade **FallbackPrintDriverType** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-449">Indicates whether the **FallbackPrintDriverType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-450">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-450">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-451">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-451">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-452">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-452">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-453">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-453">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-454">**PolicySourceHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="f6500-454">**PolicySourceHomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-455">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-455">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-456">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-457">Indica se a propriedade **HomeDirectory** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-457">Indicates whether the **HomeDirectory** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-458">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-458">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-459">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-459">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-460">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-460">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-461">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-461">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-462">**PolicySourceLicensingType**</span><span class="sxs-lookup"><span data-stu-id="f6500-462">**PolicySourceLicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-463">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-464">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-465">Indica se a propriedade **licensingtype** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-465">Indicates whether the **LicensingType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-466">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-466">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-467">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-467">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-468">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-468">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-469">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-469">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-470">**PolicySourceProfilePath**</span><span class="sxs-lookup"><span data-stu-id="f6500-470">**PolicySourceProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-471">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-473">Indica se a propriedade **ProfilePath** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-473">Indicates whether the **ProfilePath** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-474">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-474">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-475">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-475">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-476">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-476">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-477">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-477">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-478">**PolicySourceRedirectSmartCards**</span><span class="sxs-lookup"><span data-stu-id="f6500-478">**PolicySourceRedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-479">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-479">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-480">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-481">Indica se a propriedade **RedirectSmartCards** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-481">Indicates whether the **RedirectSmartCards** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="f6500-482">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-482">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-483">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-483">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-484">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-484">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-485">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-485">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="f6500-486">**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-486">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-487">**PolicySourceSingleSession**</span><span class="sxs-lookup"><span data-stu-id="f6500-487">**PolicySourceSingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-488">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-489">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-490">Indica se a propriedade **SingleSession** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-490">Indicates whether the property **SingleSession** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-491">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-491">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-492">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-492">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-493">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-493">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-494">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-494">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-495">**PolicySourceTimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="f6500-495">**PolicySourceTimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-496">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-497">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-498">Indica se a propriedade **TimeZoneRedirection** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-498">Indicates whether the property **TimeZoneRedirection** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-499">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-499">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-500">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-500">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-501">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-501">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-502">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-502">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-503">**PolicySourceUseRDEasyPrintDriver**</span><span class="sxs-lookup"><span data-stu-id="f6500-503">**PolicySourceUseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-504">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-505">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-506">Indica se a propriedade **UseRDEasyPrintDriver** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-506">Indicates whether the **UseRDEasyPrintDriver** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="f6500-507">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-507">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-508">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-508">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-509">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-509">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-510">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-510">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="f6500-511">**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-511">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-512">**PolicySourceUseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="f6500-512">**PolicySourceUseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-513">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-514">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-515">Indica se a propriedade **UseTempFolders** está configurada pelo servidor ou pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="f6500-515">Indicates whether the **UseTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="f6500-516">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-516">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-517">Servidor</span><span class="sxs-lookup"><span data-stu-id="f6500-517">Server</span></span>

</dd> <dt>

<span data-ttu-id="f6500-518">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-518">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-519">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="f6500-519">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-520">**PossibleLicensingTypes**</span><span class="sxs-lookup"><span data-stu-id="f6500-520">**PossibleLicensingTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-521">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-522">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6500-523">Qualificadores: [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**bitvalues**](/windows/desktop/WmiSdk/standard-qualifiers) ("pessoal Terminal Server", "área de trabalho remota para administração", "por dispositivo", "por usuário", "não configurado")</span><span class="sxs-lookup"><span data-stu-id="f6500-523">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Personal Terminal Server", "Remote Desktop for Administration", "Per Device", "Per User", "Not Configured")</span></span>
</dt> </dl>

<span data-ttu-id="f6500-524">Um bitmask que especifica os tipos de licenciamento que estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f6500-524">A bitmask that specifies the licensing types that are available.</span></span> <span data-ttu-id="f6500-525">Isso pode ser uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6500-525">This can be a combination of one or more of the following values.</span></span>

<dt>

<span data-ttu-id="f6500-526">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-526">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-527">Há suporte para licenças do Personal Host da Sessão RD Server.</span><span class="sxs-lookup"><span data-stu-id="f6500-527">Personal RD Session Host server licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-528">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="f6500-528">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-529">Há suporte para Área de Trabalho Remota licenças.</span><span class="sxs-lookup"><span data-stu-id="f6500-529">Remote Desktop licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-530">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="f6500-530">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-531">Há suporte para licenças por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6500-531">Per device licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-532">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="f6500-532">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-533">Há suporte para licenças por usuário.</span><span class="sxs-lookup"><span data-stu-id="f6500-533">Per user licenses are supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-534">**Profilepath**</span><span class="sxs-lookup"><span data-stu-id="f6500-534">**ProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-535">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f6500-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-536">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-537">Caminho do perfil do computador.</span><span class="sxs-lookup"><span data-stu-id="f6500-537">Profile path for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-538">**RedirectSmartCards**</span><span class="sxs-lookup"><span data-stu-id="f6500-538">**RedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-539">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-540">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-540">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-541">Especifica se o redirecionamento de dispositivos de cartão inteligente é permitido em uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="f6500-541">Specifies if redirection of smart card devices is allowed in a remote session.</span></span>

<dt>

<span data-ttu-id="f6500-542">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f6500-542">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-543">O redirecionamento de dispositivo de cartão inteligente não é permitido.</span><span class="sxs-lookup"><span data-stu-id="f6500-543">Smart card device redirection is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-544">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f6500-544">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f6500-545">O redirecionamento de dispositivo de cartão inteligente é permitido.</span><span class="sxs-lookup"><span data-stu-id="f6500-545">Smart card device redirection is allowed.</span></span>

</dd> </dl>

<span data-ttu-id="f6500-546">**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-546">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-547">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="f6500-547">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-548">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f6500-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-549">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6500-550">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6500-550">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f6500-551">Nome do servidor de Host da Sessão RD cujas propriedades são de interesse.</span><span class="sxs-lookup"><span data-stu-id="f6500-551">Name of the RD Session Host server whose properties are of interest.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-552">**SessionBrokerDrainMode**</span><span class="sxs-lookup"><span data-stu-id="f6500-552">**SessionBrokerDrainMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-553">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-553">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-554">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-555">O modo de logon do usuário do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="f6500-555">The RD Connection Broker user logon mode.</span></span>

<dt>

<span data-ttu-id="f6500-556">0</span><span class="sxs-lookup"><span data-stu-id="f6500-556">0</span></span>
</dt> <dd>

<span data-ttu-id="f6500-557">Permitir todas as conexões.</span><span class="sxs-lookup"><span data-stu-id="f6500-557">Allow all connections.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-558">1</span><span class="sxs-lookup"><span data-stu-id="f6500-558">1</span></span>
</dt> <dd>

<span data-ttu-id="f6500-559">Permitir reconexões, mas evitar novos logons até que o servidor seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="f6500-559">Allow reconnections, but prevent new logons until the server is restarted.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-560">2</span><span class="sxs-lookup"><span data-stu-id="f6500-560">2</span></span>
</dt> <dd>

<span data-ttu-id="f6500-561">Permitir reconexões, mas impedir novos logons.</span><span class="sxs-lookup"><span data-stu-id="f6500-561">Allow reconnections, but prevent new logons.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-562">**SingleSession**</span><span class="sxs-lookup"><span data-stu-id="f6500-562">**SingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-563">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-564">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-565">Especifica se uma ou mais sessões de Serviços de Área de Trabalho Remota são permitidas por usuário.</span><span class="sxs-lookup"><span data-stu-id="f6500-565">Specifies whether one or more Remote Desktop Services sessions are allowed per user.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="f6500-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="f6500-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-567">Mais de uma sessão é permitida por usuário.</span><span class="sxs-lookup"><span data-stu-id="f6500-567">More than one session is allowed per user.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="f6500-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="f6500-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-569">Somente uma sessão é permitida por usuário.</span><span class="sxs-lookup"><span data-stu-id="f6500-569">Only one session is allowed per user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-570">**Status**</span><span class="sxs-lookup"><span data-stu-id="f6500-570">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-571">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f6500-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-572">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6500-573">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f6500-573">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f6500-574">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f6500-574">Current status of the object.</span></span> <span data-ttu-id="f6500-575">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="f6500-575">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f6500-576">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="f6500-576">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f6500-577">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="f6500-577">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f6500-578">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="f6500-578">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f6500-579">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="f6500-579">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f6500-580">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f6500-580">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f6500-581">("OK")</span><span class="sxs-lookup"><span data-stu-id="f6500-581">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f6500-582">("Erro")</span><span class="sxs-lookup"><span data-stu-id="f6500-582">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f6500-583">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="f6500-583">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f6500-584">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="f6500-584">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f6500-585">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f6500-585">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f6500-586">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="f6500-586">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f6500-587">("Parando")</span><span class="sxs-lookup"><span data-stu-id="f6500-587">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f6500-588">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="f6500-588">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-589">**TerminalServerMode**</span><span class="sxs-lookup"><span data-stu-id="f6500-589">**TerminalServerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-590">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-591">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-592">O modo operacional do servidor Host da Sessão RD do serviço Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="f6500-592">The RD Session Host server operating mode of the Remote Desktop Services service.</span></span> <span data-ttu-id="f6500-593">Esse modo controla as políticas de licenciamento que são aplicáveis, bem como se os recursos de compatibilidade de aplicativos estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="f6500-593">This mode controls the licensing policies that are applicable as well as whether application-compatibility features are enabled.</span></span>

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span data-ttu-id="f6500-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)</span><span class="sxs-lookup"><span data-stu-id="f6500-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-595">O servidor Opera como um servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f6500-595">The server operates as an application server.</span></span>

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span data-ttu-id="f6500-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span><span class="sxs-lookup"><span data-stu-id="f6500-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-597">A sessão é administrada remotamente.</span><span class="sxs-lookup"><span data-stu-id="f6500-597">The session is administered remotely.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-598">**TimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="f6500-598">**TimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-599">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-599">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-600">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-600">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-601">Especifica se o computador cliente pode redirecionar suas configurações de fuso horário para a sessão de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="f6500-601">Specifies whether the client computer can redirect its time zone settings to the Remote Desktop Services session.</span></span>

<dt>

<span data-ttu-id="f6500-602">0</span><span class="sxs-lookup"><span data-stu-id="f6500-602">0</span></span>
</dt> <dd>

<span data-ttu-id="f6500-603">O redirecionamento está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-603">Redirection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-604">1</span><span class="sxs-lookup"><span data-stu-id="f6500-604">1</span></span>
</dt> <dd>

<span data-ttu-id="f6500-605">O redirecionamento está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f6500-605">Redirection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-606">**UseRDEasyPrintDriver**</span><span class="sxs-lookup"><span data-stu-id="f6500-606">**UseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-607">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-607">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-608">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-608">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-609">Especifica se o driver de impressora Easy Print de Área de Trabalho Remota é usado primeiro para instalar todas as impressoras de cliente.</span><span class="sxs-lookup"><span data-stu-id="f6500-609">Specifies whether the Remote Desktop Easy Print printer driver is used first to install all client printers.</span></span>

<dt>

<span data-ttu-id="f6500-610">0</span><span class="sxs-lookup"><span data-stu-id="f6500-610">0</span></span>
</dt> <dd>

<span data-ttu-id="f6500-611">O Host da Sessão RD Server tenta encontrar um driver de impressora adequado para instalar a impressora do cliente.</span><span class="sxs-lookup"><span data-stu-id="f6500-611">The RD Session Host server tries to find a suitable printer driver to install the client printer.</span></span> <span data-ttu-id="f6500-612">Se o servidor de Host da Sessão RD não tiver um driver de impressora que corresponda à impressora cliente, o servidor tentará usar o driver Easy Print de Área de Trabalho Remota para instalar a impressora cliente.</span><span class="sxs-lookup"><span data-stu-id="f6500-612">If the RD Session Host server does not have a printer driver that matches the client printer, the server tries to use the Remote Desktop Easy Print driver to install the client printer.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-613">1</span><span class="sxs-lookup"><span data-stu-id="f6500-613">1</span></span>
</dt> <dd>

<span data-ttu-id="f6500-614">O Host da Sessão RD Server primeiro tenta usar o driver de impressora Easy Print de Área de Trabalho Remota para instalar todas as impressoras do cliente.</span><span class="sxs-lookup"><span data-stu-id="f6500-614">The RD Session Host server first tries to use the Remote Desktop Easy Print printer driver to install all client printers.</span></span> <span data-ttu-id="f6500-615">Se por algum motivo o driver de impressora Easy Print de Área de Trabalho Remota não puder ser usado, um driver de impressora no servidor Host da Sessão RD que corresponda à impressora cliente será usado.</span><span class="sxs-lookup"><span data-stu-id="f6500-615">If for any reason the Remote Desktop Easy Print printer driver cannot be used, a printer driver on the RD Session Host server that matches the client printer is used.</span></span>

</dd> </dl>

<span data-ttu-id="f6500-616">**Windows server 2008 R2 e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6500-616">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="f6500-617">**UserPermission**</span><span class="sxs-lookup"><span data-stu-id="f6500-617">**UserPermission**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-618">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-618">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-619">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f6500-619">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f6500-620">Especifica se cada sessão de usuário tem segurança rígida ou reduzida.</span><span class="sxs-lookup"><span data-stu-id="f6500-620">Specifies if each user session has tight or relaxed security.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="f6500-621"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="f6500-621"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-622">A segurança é rígida.</span><span class="sxs-lookup"><span data-stu-id="f6500-622">Security is tight.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="f6500-623"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="f6500-623"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-624">A segurança é relaxada.</span><span class="sxs-lookup"><span data-stu-id="f6500-624">Security is relaxed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6500-625">**UseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="f6500-625">**UseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6500-626">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6500-626">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6500-627">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f6500-627">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6500-628">Especifica se os diretórios temporários são criados e excluídos por sessão.</span><span class="sxs-lookup"><span data-stu-id="f6500-628">Specifies whether temporary directories are created and deleted on a per-session basis.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="f6500-629"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="f6500-629"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-630">Os diretórios temporários não são criados e excluídos para cada sessão.</span><span class="sxs-lookup"><span data-stu-id="f6500-630">Temporary directories are not created and deleted for each session.</span></span> <span data-ttu-id="f6500-631">Uma é criada para a primeira sessão e nunca é excluída.</span><span class="sxs-lookup"><span data-stu-id="f6500-631">One is created for the first session and never deleted.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="f6500-632"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="f6500-632"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6500-633">Os diretórios temporários são criados e excluídos para cada sessão.</span><span class="sxs-lookup"><span data-stu-id="f6500-633">Temporary directories are created and deleted for each session.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6500-634">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6500-634">Remarks</span></span>

<span data-ttu-id="f6500-635">**Win32 \_ TerminalServiceSetting** está associado ao [**Win32 \_ TerminalService**](win32-terminalservice.md) como a propriedade **Setting** da Associação [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="f6500-635">**Win32\_TerminalServiceSetting** is associated to [**Win32\_TerminalService**](win32-terminalservice.md) as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="f6500-636">[**Win32 \_ TerminalSetting**](win32-terminalsetting.md) é associado ao [**\_ terminal do Win32**](win32-terminal.md) como a propriedade de **configuração** da Associação [**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="f6500-636">[**Win32\_TerminalSetting**](win32-terminalsetting.md) is associated to [**Win32\_Terminal**](win32-terminal.md) as the **Setting** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="f6500-637">Para se conectar ao \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="f6500-637">To connect to the Root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="f6500-638">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="f6500-638">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="f6500-639">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de seis.</span><span class="sxs-lookup"><span data-stu-id="f6500-639">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="f6500-640">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="f6500-640">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="f6500-641">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f6500-641">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f6500-642">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f6500-642">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f6500-643">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f6500-643">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f6500-644">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f6500-644">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6500-645">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6500-645">Requirements</span></span>



| <span data-ttu-id="f6500-646">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6500-646">Requirement</span></span> | <span data-ttu-id="f6500-647">Valor</span><span class="sxs-lookup"><span data-stu-id="f6500-647">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6500-648">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6500-648">Minimum supported client</span></span><br/> | <span data-ttu-id="f6500-649">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f6500-649">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f6500-650">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6500-650">Minimum supported server</span></span><br/> | <span data-ttu-id="f6500-651">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6500-651">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6500-652">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6500-652">Namespace</span></span><br/>                | <span data-ttu-id="f6500-653">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f6500-653">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f6500-654">MOF</span><span class="sxs-lookup"><span data-stu-id="f6500-654">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6500-655"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6500-655"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6500-656">DLL</span><span class="sxs-lookup"><span data-stu-id="f6500-656">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6500-657"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6500-657"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6500-658">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6500-658">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6500-659">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f6500-659">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="f6500-660">**Terminal do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f6500-660">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="f6500-661">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="f6500-661">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="f6500-662">**\_TerminalServiceToSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f6500-662">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="f6500-663">**\_TerminalTerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f6500-663">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dt>

[<span data-ttu-id="f6500-664">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f6500-664">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

