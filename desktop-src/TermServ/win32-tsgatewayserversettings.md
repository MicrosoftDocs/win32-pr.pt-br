---
title: Classe Win32_TSGatewayServerSettings
description: Fornece métodos e propriedades para exibir e definir configurações de servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayServerSettings classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0fb9b93f75c47760da8778e4aef8bed7f4e022
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455845"
---
# <a name="win32_tsgatewayserversettings-class"></a><span data-ttu-id="42fac-105">\_Classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="42fac-105">Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="42fac-106">Fornece métodos e propriedades para exibir e definir configurações de servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="42fac-106">Provides methods and properties to view and configure Remote Desktop Gateway (RD Gateway) server settings.</span></span> <span data-ttu-id="42fac-107">Um administrador pode usar essa classe para configurar um conjunto de protocolos, o conjunto de eventos que será gravado no log de eventos e o número máximo de conexões por meio do gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="42fac-107">An administrator can use this class to configure a set of protocols, the set of events that will be written to the event log, and the maximum number of connections through RD Gateway.</span></span>

## <a name="syntax"></a><span data-ttu-id="42fac-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42fac-108">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a><span data-ttu-id="42fac-109">Membros</span><span class="sxs-lookup"><span data-stu-id="42fac-109">Members</span></span>

<span data-ttu-id="42fac-110">A classe **Win32 \_ TSGatewayServerSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="42fac-110">The **Win32\_TSGatewayServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="42fac-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="42fac-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="42fac-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="42fac-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="42fac-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="42fac-113">Methods</span></span>

<span data-ttu-id="42fac-114">A classe **Win32 \_ TSGatewayServerSettings** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="42fac-114">The **Win32\_TSGatewayServerSettings** class has these methods.</span></span>



| <span data-ttu-id="42fac-115">Método</span><span class="sxs-lookup"><span data-stu-id="42fac-115">Method</span></span>                                                                                                                                             | <span data-ttu-id="42fac-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="42fac-116">Description</span></span>                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42fac-117">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="42fac-117">**Configure**</span></span>](configure-win32-tsgatewayserversettings.md)                                                                                       | <span data-ttu-id="42fac-118">Define as configurações de IIS e RPC exigidas pelo serviço de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="42fac-118">Configures the IIS and RPC settings required by the RD Gateway service.</span></span><br/> <span data-ttu-id="42fac-119">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-119">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                               |
| [<span data-ttu-id="42fac-120">**EnableCentralCAP**</span><span class="sxs-lookup"><span data-stu-id="42fac-120">**EnableCentralCAP**</span></span>](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="42fac-121">Habilita ou desabilita a propriedade **CentralCAPEnabled** , que controla se os servidores de política de autorização de conexão central Área de Trabalho Remota (RD CAP) são usados para controlar as políticas de autorização de conexão para este servidor.</span><span class="sxs-lookup"><span data-stu-id="42fac-121">Enables or disables the **CentralCAPEnabled** property, which controls whether central Remote Desktop connection authorization policy (RD CAP) servers are used for controlling connection authorization policies for this server.</span></span><br/>                    |
| [<span data-ttu-id="42fac-122">**EnableLogEvent**</span><span class="sxs-lookup"><span data-stu-id="42fac-122">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="42fac-123">Habilita ou desabilita o registro em log do tipo de evento especificado.</span><span class="sxs-lookup"><span data-stu-id="42fac-123">Enables or disables logging of the specified event type.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="42fac-124">**EnableOnlyConsentCapableClients**</span><span class="sxs-lookup"><span data-stu-id="42fac-124">**EnableOnlyConsentCapableClients**</span></span>](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | <span data-ttu-id="42fac-125">Define a propriedade **OnlyConsentCapableClients** .</span><span class="sxs-lookup"><span data-stu-id="42fac-125">Sets the **OnlyConsentCapableClients** property.</span></span><br/> <span data-ttu-id="42fac-126">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-126">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="42fac-127">**EnableRequestSOH**</span><span class="sxs-lookup"><span data-stu-id="42fac-127">**EnableRequestSOH**</span></span>](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | <span data-ttu-id="42fac-128">Este método não tem suporte a partir do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="42fac-128">This method is not supported starting with Windows Server 2016.</span></span><br/> <span data-ttu-id="42fac-129">**Windows server 2012 R2, Windows server 2012, Windows server 2008 R2 e Windows server 2008:** Habilita ou desabilita solicitações para uma SoH (declaração de integridade).</span><span class="sxs-lookup"><span data-stu-id="42fac-129">**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:** Enables or disables requests for a Statement of Health (SoH).</span></span><br/> <br/> |
| [<span data-ttu-id="42fac-130">**EnableTransport**</span><span class="sxs-lookup"><span data-stu-id="42fac-130">**EnableTransport**</span></span>](enabletransport-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="42fac-131">Habilita ou desabilita o transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="42fac-131">Enables or disables the specified transport.</span></span><br/> <span data-ttu-id="42fac-132">**Windows server 2008 R2 e Windows server 2008:** Este método não está disponível antes do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="42fac-132">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="42fac-133">**EnumAuthenticationPlugins**</span><span class="sxs-lookup"><span data-stu-id="42fac-133">**EnumAuthenticationPlugins**</span></span>](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | <span data-ttu-id="42fac-134">Enumera todos os plug-ins de autenticação registrados.</span><span class="sxs-lookup"><span data-stu-id="42fac-134">Enumerates all registered authentication plug-ins.</span></span><br/> <span data-ttu-id="42fac-135">**Windows Server 2008:** Este método não está disponível.</span><span class="sxs-lookup"><span data-stu-id="42fac-135">**Windows Server 2008:** This method is not available.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="42fac-136">**EnumAuthorizationPlugins**</span><span class="sxs-lookup"><span data-stu-id="42fac-136">**EnumAuthorizationPlugins**</span></span>](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="42fac-137">Enumera todos os plug-ins de autorização registrados.</span><span class="sxs-lookup"><span data-stu-id="42fac-137">Enumerates all registered authorization plug-ins.</span></span><br/> <span data-ttu-id="42fac-138">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="42fac-139">**GetIPAndPort**</span><span class="sxs-lookup"><span data-stu-id="42fac-139">**GetIPAndPort**</span></span>](getipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="42fac-140">Obtém o endereço IP de escuta e o número da porta para o transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="42fac-140">Obtains the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="42fac-141">**Windows server 2008 R2 e Windows server 2008:** Este método não está disponível antes do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="42fac-141">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                 |
| [<span data-ttu-id="42fac-142">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="42fac-142">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="42fac-143">Retorna o nome do evento de log para o índice de evento de log especificado.</span><span class="sxs-lookup"><span data-stu-id="42fac-143">Returns the log event name for the specified log event index.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="42fac-144">**Getprotocolname**</span><span class="sxs-lookup"><span data-stu-id="42fac-144">**GetProtocolName**</span></span>](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="42fac-145">Retorna o nome do protocolo para o índice de protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="42fac-145">Returns the protocol name for the specified protocol index.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="42fac-146">**IsLogEventEnabled**</span><span class="sxs-lookup"><span data-stu-id="42fac-146">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="42fac-147">Indica se o tipo de log de eventos especificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="42fac-147">Indicates whether the specified event log type is enabled.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="42fac-148">**IsTransportEnabled**</span><span class="sxs-lookup"><span data-stu-id="42fac-148">**IsTransportEnabled**</span></span>](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="42fac-149">Determina se o transporte especificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="42fac-149">Determines whether the specified transport is enabled.</span></span><br/> <span data-ttu-id="42fac-150">**Windows server 2008 R2 e Windows server 2008:** Este método não está disponível antes do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="42fac-150">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                        |
| [<span data-ttu-id="42fac-151">**QueryCertContext**</span><span class="sxs-lookup"><span data-stu-id="42fac-151">**QueryCertContext**</span></span>](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | <span data-ttu-id="42fac-152">Indica se o certificado especificado está instalado.</span><span class="sxs-lookup"><span data-stu-id="42fac-152">Indicates whether the specified certificate is installed.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="42fac-153">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="42fac-153">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | <span data-ttu-id="42fac-154">Recicla os pools de aplicativos RPC no IIS.</span><span class="sxs-lookup"><span data-stu-id="42fac-154">Recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="42fac-155">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-155">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="42fac-156">**RefreshCertContext**</span><span class="sxs-lookup"><span data-stu-id="42fac-156">**RefreshCertContext**</span></span>](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | <span data-ttu-id="42fac-157">Atualiza o certificado que é usado pelo servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="42fac-157">Refreshes the certificate that is used by the RD Gateway server.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="42fac-158">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="42fac-158">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | <span data-ttu-id="42fac-159">Define o plug-in de autenticação atual para o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="42fac-159">Sets the current authentication plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="42fac-160">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-160">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="42fac-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="42fac-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span></span>](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | <span data-ttu-id="42fac-162">Define o plug-in de autenticação atual para o servidor de gateway de área de trabalho remota e recicla os pools de aplicativos RPC no IIS.</span><span class="sxs-lookup"><span data-stu-id="42fac-162">Sets the current authentication plug-in for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="42fac-163">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-163">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                      |
| [<span data-ttu-id="42fac-164">**SetAuthorizationPlugin**</span><span class="sxs-lookup"><span data-stu-id="42fac-164">**SetAuthorizationPlugin**</span></span>](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | <span data-ttu-id="42fac-165">Define o plug-in de autorização atual para o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="42fac-165">Sets the current authorization plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="42fac-166">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-166">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                     |
| [<span data-ttu-id="42fac-167">**SetCertificate**</span><span class="sxs-lookup"><span data-stu-id="42fac-167">**SetCertificate**</span></span>](setcertificate-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="42fac-168">Define o hash de certificado para associação HTTPS na porta 443 no IIS.</span><span class="sxs-lookup"><span data-stu-id="42fac-168">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span><br/> <span data-ttu-id="42fac-169">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                       |
| [<span data-ttu-id="42fac-170">**SetCertificateACL**</span><span class="sxs-lookup"><span data-stu-id="42fac-170">**SetCertificateACL**</span></span>](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="42fac-171">Define as listas de controle de acesso (ACLs) do certificado para este servidor.</span><span class="sxs-lookup"><span data-stu-id="42fac-171">Sets the certificate access control lists (ACLs) for this server.</span></span><br/>                                                                                                                                                                                     |
| [<span data-ttu-id="42fac-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="42fac-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span></span>](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | <span data-ttu-id="42fac-173">Define os plug-ins de autenticação e autorização atuais para o servidor de gateway de área de trabalho remota e recicla os pools de aplicativos RPC no IIS.</span><span class="sxs-lookup"><span data-stu-id="42fac-173">Sets the current authentication and authorization plug-ins for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="42fac-174">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-174">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                   |
| [<span data-ttu-id="42fac-175">**SetEnforceChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="42fac-175">**SetEnforceChannelBinding**</span></span>](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="42fac-176">Define a propriedade **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="42fac-176">Sets the **EnforceChannelBinding** property.</span></span><br/> <span data-ttu-id="42fac-177">**Windows server 2008 R2 e Windows server 2008:** Este método não está disponível antes do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="42fac-177">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="42fac-178">**SetIPAndPort**</span><span class="sxs-lookup"><span data-stu-id="42fac-178">**SetIPAndPort**</span></span>](setipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="42fac-179">Define o endereço IP de escuta e o número da porta para o transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="42fac-179">Sets the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="42fac-180">**Windows server 2008 R2 e Windows server 2008:** Este método não está disponível antes do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="42fac-180">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                    |
| [<span data-ttu-id="42fac-181">**SetMaxConnections**</span><span class="sxs-lookup"><span data-stu-id="42fac-181">**SetMaxConnections**</span></span>](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="42fac-182">Define o número máximo de conexões permitidas por meio do gateway RD.</span><span class="sxs-lookup"><span data-stu-id="42fac-182">Sets the maximum number of allowed connections through RD Gateway.</span></span> <span data-ttu-id="42fac-183">Esse método altera as propriedades **MaxConnections** e **UnlimitedConnections** .</span><span class="sxs-lookup"><span data-stu-id="42fac-183">This method changes the **MaxConnections** and **UnlimitedConnections** properties.</span></span><br/>                                                                                                |
| [<span data-ttu-id="42fac-184">**SetSslBridging**</span><span class="sxs-lookup"><span data-stu-id="42fac-184">**SetSslBridging**</span></span>](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="42fac-185">Define o tipo de ponte SSL a ser usado pelo servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="42fac-185">Sets the type of SSL bridging to be used by the RD Gateway server.</span></span><br/> <span data-ttu-id="42fac-186">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-186">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="42fac-187">**TSGRemoveAdminMsg**</span><span class="sxs-lookup"><span data-stu-id="42fac-187">**TSGRemoveAdminMsg**</span></span>](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="42fac-188">Remove a mensagem administrativa para o servidor de gateway.</span><span class="sxs-lookup"><span data-stu-id="42fac-188">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="42fac-189">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-189">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="42fac-190">**TSGRemoveConsentMsg**</span><span class="sxs-lookup"><span data-stu-id="42fac-190">**TSGRemoveConsentMsg**</span></span>](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | <span data-ttu-id="42fac-191">Remove a mensagem administrativa para o servidor de gateway.</span><span class="sxs-lookup"><span data-stu-id="42fac-191">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="42fac-192">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-192">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="42fac-193">**TSGStoreAdminMsg**</span><span class="sxs-lookup"><span data-stu-id="42fac-193">**TSGStoreAdminMsg**</span></span>](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="42fac-194">Atualiza a mensagem administrativa para o servidor de gateway.</span><span class="sxs-lookup"><span data-stu-id="42fac-194">Updates the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="42fac-195">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-195">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="42fac-196">**TSGStoreConsentMsg**</span><span class="sxs-lookup"><span data-stu-id="42fac-196">**TSGStoreConsentMsg**</span></span>](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="42fac-197">Atualiza a mensagem de consentimento para o servidor de gateway.</span><span class="sxs-lookup"><span data-stu-id="42fac-197">Updates the consent message for the gateway server.</span></span><br/> <span data-ttu-id="42fac-198">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-198">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="42fac-199">Propriedades</span><span class="sxs-lookup"><span data-stu-id="42fac-199">Properties</span></span>

<span data-ttu-id="42fac-200">A classe **Win32 \_ TSGatewayServerSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="42fac-200">The **Win32\_TSGatewayServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42fac-201">**adminMessageEndTime**</span><span class="sxs-lookup"><span data-stu-id="42fac-201">**adminMessageEndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42fac-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-204">A hora de término da mensagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="42fac-204">The administrative message end time.</span></span>

<span data-ttu-id="42fac-205">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-205">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-206">**adminMessageStartTime**</span><span class="sxs-lookup"><span data-stu-id="42fac-206">**adminMessageStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42fac-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-209">A hora de início da mensagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="42fac-209">The administrative message start time.</span></span>

<span data-ttu-id="42fac-210">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-210">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-211">**adminMessageText**</span><span class="sxs-lookup"><span data-stu-id="42fac-211">**adminMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-212">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42fac-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-214">O texto da mensagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="42fac-214">The administrative message text.</span></span>

<span data-ttu-id="42fac-215">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-215">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-216">**AuthenticationPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="42fac-216">**AuthenticationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42fac-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-219">O CLSID do plug-in de autenticação atual.</span><span class="sxs-lookup"><span data-stu-id="42fac-219">The CLSID of the current authentication plug-in.</span></span>

<span data-ttu-id="42fac-220">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-220">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-221">**AuthenticationPluginDescription**</span><span class="sxs-lookup"><span data-stu-id="42fac-221">**AuthenticationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42fac-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-224">A descrição do plug-in de autenticação atual.</span><span class="sxs-lookup"><span data-stu-id="42fac-224">The description of the current authentication plug-in.</span></span>

<span data-ttu-id="42fac-225">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-225">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-226">**AuthenticationPluginName**</span><span class="sxs-lookup"><span data-stu-id="42fac-226">**AuthenticationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42fac-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-229">O nome do plug-in de autenticação atual.</span><span class="sxs-lookup"><span data-stu-id="42fac-229">The name of the current authentication plug-in.</span></span>

<span data-ttu-id="42fac-230">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-230">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-231">**AuthorizationPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="42fac-231">**AuthorizationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42fac-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-234">O CLSID do plug-in de autorização atual.</span><span class="sxs-lookup"><span data-stu-id="42fac-234">The CLSID of the current authorization plug-in.</span></span>

<span data-ttu-id="42fac-235">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-235">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-236">**AuthorizationPluginDescription**</span><span class="sxs-lookup"><span data-stu-id="42fac-236">**AuthorizationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42fac-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-239">A descrição do plug-in de autorização atual.</span><span class="sxs-lookup"><span data-stu-id="42fac-239">The description of the current authorization plug-in.</span></span>

<span data-ttu-id="42fac-240">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-240">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-241">**AuthorizationPluginName**</span><span class="sxs-lookup"><span data-stu-id="42fac-241">**AuthorizationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42fac-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-244">O nome do plug-in de autorização atual.</span><span class="sxs-lookup"><span data-stu-id="42fac-244">The name of the current authorization plug-in.</span></span>

<span data-ttu-id="42fac-245">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-245">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-246">**CentralCAPEnabled**</span><span class="sxs-lookup"><span data-stu-id="42fac-246">**CentralCAPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-247">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42fac-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-249">Especifica se os servidores de RD CAP central são usados para controlar esse servidor.</span><span class="sxs-lookup"><span data-stu-id="42fac-249">Specifies whether central RD CAP servers are used for controlling this server.</span></span> <span data-ttu-id="42fac-250">Essa propriedade pode ser alterada chamando o método [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="42fac-250">This property can be changed by calling the [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-251">**CertHash**</span><span class="sxs-lookup"><span data-stu-id="42fac-251">**CertHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-252">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="42fac-252">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="42fac-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-254">Especifica o hash de certificado para associação HTTPS na porta 443 no IIS.</span><span class="sxs-lookup"><span data-stu-id="42fac-254">Specifies the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

<span data-ttu-id="42fac-255">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-255">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-256">**consentMessageText**</span><span class="sxs-lookup"><span data-stu-id="42fac-256">**consentMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42fac-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-259">O texto da mensagem de consentimento.</span><span class="sxs-lookup"><span data-stu-id="42fac-259">The consent message text.</span></span>

<span data-ttu-id="42fac-260">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-260">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-261">**EnforceChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="42fac-261">**EnforceChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-262">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42fac-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-264">Indica se a associação de canal é imposta para o transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="42fac-264">Indicates if channel binding is enforced for the HTTP transport.</span></span> <span data-ttu-id="42fac-265">Esse valor de propriedade pode ser alterado usando o método [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="42fac-265">This property value can be changed by using the [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) method.</span></span>

<span data-ttu-id="42fac-266">**Windows server 2008 R2 e Windows server 2008:** Essa propriedade não está disponível antes do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="42fac-266">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available before Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-267">**IsConfigured**</span><span class="sxs-lookup"><span data-stu-id="42fac-267">**IsConfigured**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-268">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42fac-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-270">Especifica se as configurações de IIS e RPC exigidas pelo serviço de gateway de área de trabalho remota estão configuradas.</span><span class="sxs-lookup"><span data-stu-id="42fac-270">Specifies if IIS and RPC settings required by the RD Gateway service are configured.</span></span>

<span data-ttu-id="42fac-271">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-271">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-272">**MaxConnections**</span><span class="sxs-lookup"><span data-stu-id="42fac-272">**MaxConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-273">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42fac-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42fac-275">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42fac-275">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="42fac-276">Retorna o número máximo de conexões permitidas por meio do gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="42fac-276">Returns the maximum number of connections that are allowed through RD Gateway.</span></span> <span data-ttu-id="42fac-277">Essa propriedade pode ser definida usando o método [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="42fac-277">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-278">**MaximumAllowedConnectionsBySku**</span><span class="sxs-lookup"><span data-stu-id="42fac-278">**MaximumAllowedConnectionsBySku**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-279">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42fac-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-281">Número máximo de conexões que a SKU (unidade de manutenção de estoque) permite.</span><span class="sxs-lookup"><span data-stu-id="42fac-281">Maximum number of connections that the stock-keeping unit (SKU) allows.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-282">**MaxLogEvents**</span><span class="sxs-lookup"><span data-stu-id="42fac-282">**MaxLogEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-283">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42fac-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-285">Retorna o número máximo de eventos de log.</span><span class="sxs-lookup"><span data-stu-id="42fac-285">Returns the maximum number of log events.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-286">**MaxProtocols**</span><span class="sxs-lookup"><span data-stu-id="42fac-286">**MaxProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-287">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42fac-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-289">Número de protocolos com suporte pelo Gateway RD.</span><span class="sxs-lookup"><span data-stu-id="42fac-289">Number of protocols supported by RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-290">**OnlyConsentCapableClients**</span><span class="sxs-lookup"><span data-stu-id="42fac-290">**OnlyConsentCapableClients**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-291">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42fac-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-293">Especifica se somente clientes capazes de autorizar mensagens de consentimento têm permissão para se conectar ao gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="42fac-293">Specifies if only clients capable of consent messages are allowed to connect to the RD Gateway.</span></span>

<span data-ttu-id="42fac-294">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-294">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="42fac-295">diferente</span><span class="sxs-lookup"><span data-stu-id="42fac-295">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="42fac-296">Somente clientes compatíveis com mensagens de consentimento podem se conectar.</span><span class="sxs-lookup"><span data-stu-id="42fac-296">Only consent message capable clients can connect.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-297">zero</span><span class="sxs-lookup"><span data-stu-id="42fac-297">zero</span></span>
</dt> <dd>

<span data-ttu-id="42fac-298">Clientes que não são compatíveis com mensagens de consentimento também podem se conectar.</span><span class="sxs-lookup"><span data-stu-id="42fac-298">Clients that are not consent message capable can also connect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="42fac-299">**RequestSOH**</span><span class="sxs-lookup"><span data-stu-id="42fac-299">**RequestSOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-300">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42fac-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-302">Não há suporte para essa propriedade a partir do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="42fac-302">This property is not supported starting with Windows Server 2016.</span></span>

<span data-ttu-id="42fac-303">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="42fac-303">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="42fac-304">Especifica se o servidor deve solicitar uma SoH (declaração de integridade) do cliente.</span><span class="sxs-lookup"><span data-stu-id="42fac-304">Specifies whether the server must request a Statement of Health (SoH) from the client.</span></span> <span data-ttu-id="42fac-305">Essa propriedade pode ser alterada usando o método [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) .</span><span class="sxs-lookup"><span data-stu-id="42fac-305">This property can be changed by using the [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-306">**SkuName**</span><span class="sxs-lookup"><span data-stu-id="42fac-306">**SkuName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42fac-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-309">O nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="42fac-309">Name of the SKU.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-310">**SslBridging**</span><span class="sxs-lookup"><span data-stu-id="42fac-310">**SslBridging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-311">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42fac-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-313">Especifica o tipo de ponte SSL a ser usado pelo servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="42fac-313">Specifies which type of SSL bridging to be used by the RD Gateway server.</span></span> <span data-ttu-id="42fac-314">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="42fac-314">This can be one of the following values.</span></span>

<span data-ttu-id="42fac-315">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="42fac-315">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="42fac-316">0</span><span class="sxs-lookup"><span data-stu-id="42fac-316">0</span></span>
</dt> <dd>

<span data-ttu-id="42fac-317">Sem ponte SSL.</span><span class="sxs-lookup"><span data-stu-id="42fac-317">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-318">1</span><span class="sxs-lookup"><span data-stu-id="42fac-318">1</span></span>
</dt> <dd>

<span data-ttu-id="42fac-319">Conexão HTTPS com HTTP.</span><span class="sxs-lookup"><span data-stu-id="42fac-319">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="42fac-320">2</span><span class="sxs-lookup"><span data-stu-id="42fac-320">2</span></span>
</dt> <dd>

<span data-ttu-id="42fac-321">Conexão HTTPS com HTTPS.</span><span class="sxs-lookup"><span data-stu-id="42fac-321">HTTPS to HTTPS bridging.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="42fac-322">**UnlimitedConnections**</span><span class="sxs-lookup"><span data-stu-id="42fac-322">**UnlimitedConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42fac-323">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="42fac-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42fac-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="42fac-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42fac-325">Indica se um número ilimitado de conexões é permitido por meio do gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="42fac-325">Indicates whether an unlimited number of connections are allowed through RD Gateway.</span></span> <span data-ttu-id="42fac-326">Essa propriedade pode ser definida usando o método [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="42fac-326">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42fac-327">Comentários</span><span class="sxs-lookup"><span data-stu-id="42fac-327">Remarks</span></span>

<span data-ttu-id="42fac-328">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="42fac-328">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="42fac-329">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="42fac-329">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="42fac-330">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="42fac-330">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="42fac-331">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="42fac-331">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="42fac-332">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="42fac-332">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="42fac-333">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42fac-333">Requirements</span></span>



| <span data-ttu-id="42fac-334">Requisito</span><span class="sxs-lookup"><span data-stu-id="42fac-334">Requirement</span></span> | <span data-ttu-id="42fac-335">Valor</span><span class="sxs-lookup"><span data-stu-id="42fac-335">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="42fac-336">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42fac-336">Minimum supported client</span></span><br/> | <span data-ttu-id="42fac-337">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="42fac-337">None supported</span></span><br/>                                                                |
| <span data-ttu-id="42fac-338">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42fac-338">Minimum supported server</span></span><br/> | <span data-ttu-id="42fac-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42fac-339">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="42fac-340">Namespace</span><span class="sxs-lookup"><span data-stu-id="42fac-340">Namespace</span></span><br/>                | <span data-ttu-id="42fac-341">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="42fac-341">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="42fac-342">MOF</span><span class="sxs-lookup"><span data-stu-id="42fac-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42fac-343"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42fac-343"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="42fac-344">DLL</span><span class="sxs-lookup"><span data-stu-id="42fac-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42fac-345"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42fac-345"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="42fac-346">Confira também</span><span class="sxs-lookup"><span data-stu-id="42fac-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42fac-347">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="42fac-347">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="42fac-348">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="42fac-348">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="42fac-349">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="42fac-349">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="42fac-350">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="42fac-350">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="42fac-351">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="42fac-351">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="42fac-352">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="42fac-352">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

