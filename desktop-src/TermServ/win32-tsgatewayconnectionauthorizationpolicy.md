---
title: Classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Descreve um Área de Trabalho Remota a política de autorização de conexão (RD \ 160; CAP). RD \ 160; As CAPs são usadas para determinar se um usuário tem permissão para se conectar ao servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayConnectionAuthorizationPolicy classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27384ec3a5f17c3e41fe0ceccf0ee1f7f9d08044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824352"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="90a16-106">\_Classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="90a16-106">Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="90a16-107">Descreve um Área de Trabalho Remota RD CAP (política de autorização de conexão).</span><span class="sxs-lookup"><span data-stu-id="90a16-107">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="90a16-108">As RD CAPs são usadas para determinar se um usuário tem permissão para se conectar ao servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="90a16-108">RD CAPs are used to determine whether a user is allowed to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a16-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90a16-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a><span data-ttu-id="90a16-110">Membros</span><span class="sxs-lookup"><span data-stu-id="90a16-110">Members</span></span>

<span data-ttu-id="90a16-111">A classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="90a16-111">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="90a16-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="90a16-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="90a16-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="90a16-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="90a16-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="90a16-114">Methods</span></span>

<span data-ttu-id="90a16-115">A classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="90a16-115">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="90a16-116">Método</span><span class="sxs-lookup"><span data-stu-id="90a16-116">Method</span></span>                                                                                                                | <span data-ttu-id="90a16-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="90a16-117">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90a16-118">**AddComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="90a16-118">**AddComputerGroupNames**</span></span>](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="90a16-119">Adiciona os nomes de grupo de computadores especificados à propriedade **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="90a16-119">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span><br/>                                                                                      |
| [<span data-ttu-id="90a16-120">**AddUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="90a16-120">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="90a16-121">Adiciona os nomes de grupos de usuários especificados à propriedade **Usergroupnames** .</span><span class="sxs-lookup"><span data-stu-id="90a16-121">Adds the specified user group names to the **UserGroupNames** property.</span></span><br/>                                                                                              |
| [<span data-ttu-id="90a16-122">**Criar**</span><span class="sxs-lookup"><span data-stu-id="90a16-122">**Create**</span></span>](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="90a16-123">Cria um RD CAP.</span><span class="sxs-lookup"><span data-stu-id="90a16-123">Creates an RD CAP.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="90a16-124">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="90a16-124">**Delete**</span></span>](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="90a16-125">Exclui o RD CAP atual.</span><span class="sxs-lookup"><span data-stu-id="90a16-125">Deletes the current RD CAP.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="90a16-126">**DisableClipboard**</span><span class="sxs-lookup"><span data-stu-id="90a16-126">**DisableClipboard**</span></span>](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | <span data-ttu-id="90a16-127">Define a propriedade **ClipboardDisabled** .</span><span class="sxs-lookup"><span data-stu-id="90a16-127">Sets the **ClipboardDisabled** property.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="90a16-128">**DisableDiskDrives**</span><span class="sxs-lookup"><span data-stu-id="90a16-128">**DisableDiskDrives**</span></span>](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="90a16-129">Define a propriedade **DiskDrivesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="90a16-129">Sets the **DiskDrivesDisabled** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="90a16-130">**DisablePlugAndPlayDevices**</span><span class="sxs-lookup"><span data-stu-id="90a16-130">**DisablePlugAndPlayDevices**</span></span>](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | <span data-ttu-id="90a16-131">Define a propriedade **PlugAndPlayDevicesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="90a16-131">Sets the **PlugAndPlayDevicesDisabled** property.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="90a16-132">**DisablePrinters**</span><span class="sxs-lookup"><span data-stu-id="90a16-132">**DisablePrinters**</span></span>](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | <span data-ttu-id="90a16-133">Define a propriedade **PrintersDisabled** .</span><span class="sxs-lookup"><span data-stu-id="90a16-133">Sets the **PrintersDisabled** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="90a16-134">**DisableSerialPorts**</span><span class="sxs-lookup"><span data-stu-id="90a16-134">**DisableSerialPorts**</span></span>](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="90a16-135">Define a propriedade **SerialPortsDisabled** .</span><span class="sxs-lookup"><span data-stu-id="90a16-135">Sets the **SerialPortsDisabled** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="90a16-136">**EnableAllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="90a16-136">**EnableAllowOnlySDRServers**</span></span>](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | <span data-ttu-id="90a16-137">Usado para alternar a propriedade **AllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="90a16-137">Used to toggle the **AllowOnlySDRServers** property</span></span><br/> <span data-ttu-id="90a16-138">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="90a16-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                  |
| [<span data-ttu-id="90a16-139">**MoveDown**</span><span class="sxs-lookup"><span data-stu-id="90a16-139">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | <span data-ttu-id="90a16-140">Move a RD CAP atual uma posição para baixo na lista.</span><span class="sxs-lookup"><span data-stu-id="90a16-140">Moves the current RD CAP one position down in the list.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="90a16-141">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="90a16-141">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="90a16-142">Move a RD CAP atual uma posição para cima na lista.</span><span class="sxs-lookup"><span data-stu-id="90a16-142">Moves the current RD CAP one position up in the list.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="90a16-143">**RemoveComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="90a16-143">**RemoveComputerGroupNames**</span></span>](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="90a16-144">Remove os nomes de grupos de computadores especificados da propriedade **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="90a16-144">Removes the specified computer group names from the **ComputerGroupNames** property.</span></span><br/>                                                                                 |
| [<span data-ttu-id="90a16-145">**RemoveUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="90a16-145">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | <span data-ttu-id="90a16-146">Remove os nomes de grupo de usuários especificados da propriedade **Usergroupnames** .</span><span class="sxs-lookup"><span data-stu-id="90a16-146">Removes specified user group names from the **UserGroupNames** property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="90a16-147">**SetComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="90a16-147">**SetComputerGroupNames**</span></span>](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="90a16-148">Define a propriedade **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="90a16-148">Sets the **ComputerGroupNames** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="90a16-149">**SetCookieAuthenticationAllowed**</span><span class="sxs-lookup"><span data-stu-id="90a16-149">**SetCookieAuthenticationAllowed**</span></span>](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | <span data-ttu-id="90a16-150">Define a propriedade **CookieAuthenticationAllowed** .</span><span class="sxs-lookup"><span data-stu-id="90a16-150">Sets the **CookieAuthenticationAllowed** property.</span></span><br/> <span data-ttu-id="90a16-151">**Windows Server 2008:** Este método não está disponível.</span><span class="sxs-lookup"><span data-stu-id="90a16-151">**Windows Server 2008:** This method is not available.</span></span><br/>                                                 |
| [<span data-ttu-id="90a16-152">**SetDeviceRedirectionType**</span><span class="sxs-lookup"><span data-stu-id="90a16-152">**SetDeviceRedirectionType**</span></span>](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="90a16-153">Define a propriedade **DeviceRedirectionType** .</span><span class="sxs-lookup"><span data-stu-id="90a16-153">Sets the **DeviceRedirectionType** property.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="90a16-154">**Sethabilitado**</span><span class="sxs-lookup"><span data-stu-id="90a16-154">**SetEnabled**</span></span>](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | <span data-ttu-id="90a16-155">Habilita ou desabilita a RD CAP atual.</span><span class="sxs-lookup"><span data-stu-id="90a16-155">Enables or disables the current RD CAP.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="90a16-156">**SetIdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="90a16-156">**SetIdleTimeout**</span></span>](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | <span data-ttu-id="90a16-157">Define a propriedade **IdleTimeout** .</span><span class="sxs-lookup"><span data-stu-id="90a16-157">Sets the **IdleTimeout** property.</span></span><br/> <span data-ttu-id="90a16-158">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="90a16-158">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                   |
| [<span data-ttu-id="90a16-159">**SetName**</span><span class="sxs-lookup"><span data-stu-id="90a16-159">**SetName**</span></span>](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | <span data-ttu-id="90a16-160">Define um novo nome para este RD CAP.</span><span class="sxs-lookup"><span data-stu-id="90a16-160">Sets a new name for this RD CAP.</span></span> <span data-ttu-id="90a16-161">Esse método garante que os nomes serão exclusivos.</span><span class="sxs-lookup"><span data-stu-id="90a16-161">This method ensures that names will be unique.</span></span><br/>                                                                                      |
| [<span data-ttu-id="90a16-162">**SetPasswordAllowed**</span><span class="sxs-lookup"><span data-stu-id="90a16-162">**SetPasswordAllowed**</span></span>](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="90a16-163">Define a propriedade **PasswordAllowed** .</span><span class="sxs-lookup"><span data-stu-id="90a16-163">Sets the **PasswordAllowed** property.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="90a16-164">**SetSecureIdAllowed**</span><span class="sxs-lookup"><span data-stu-id="90a16-164">**SetSecureIdAllowed**</span></span>](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="90a16-165">Define a propriedade **SecureIdAllowed** .</span><span class="sxs-lookup"><span data-stu-id="90a16-165">Sets the **SecureIdAllowed** property.</span></span><br/> <span data-ttu-id="90a16-166">**Windows Server 2008:** Esse método é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="90a16-166">**Windows Server 2008:** This method is reserved for future use.</span></span><br/>                                                   |
| [<span data-ttu-id="90a16-167">**SetSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="90a16-167">**SetSessionTimeout**</span></span>](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="90a16-168">Define as propriedades **SessionTimeout** e **SessionTimeoutAction** .</span><span class="sxs-lookup"><span data-stu-id="90a16-168">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span><br/> <span data-ttu-id="90a16-169">**Windows Server 2008:** Esse método não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="90a16-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/> |
| [<span data-ttu-id="90a16-170">**SetSmartcardAllowed**</span><span class="sxs-lookup"><span data-stu-id="90a16-170">**SetSmartcardAllowed**</span></span>](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | <span data-ttu-id="90a16-171">Define a propriedade **SmartcardAllowed** .</span><span class="sxs-lookup"><span data-stu-id="90a16-171">Sets the **SmartcardAllowed** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="90a16-172">**SetUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="90a16-172">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="90a16-173">Define a propriedade **Usergroupnames** .</span><span class="sxs-lookup"><span data-stu-id="90a16-173">Sets the **UserGroupNames** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="90a16-174">**Cumulativo**</span><span class="sxs-lookup"><span data-stu-id="90a16-174">**Update**</span></span>](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="90a16-175">Atualiza o RD CAP atual.</span><span class="sxs-lookup"><span data-stu-id="90a16-175">Updates the current RD CAP.</span></span><br/>                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="90a16-176">Propriedades</span><span class="sxs-lookup"><span data-stu-id="90a16-176">Properties</span></span>

<span data-ttu-id="90a16-177">A classe **Win32 \_ TSGatewayConnectionAuthorizationPolicy** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="90a16-177">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90a16-178">**AllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="90a16-178">**AllowOnlySDRServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-179">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-181">Indica se as conexões são permitidas apenas para proteger servidores RDS do redirecionamento de dispositivo (SDR).</span><span class="sxs-lookup"><span data-stu-id="90a16-181">Indicates whether connections allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="90a16-182">Essa propriedade pode ser definida usando o método [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) .</span><span class="sxs-lookup"><span data-stu-id="90a16-182">This property can be set using the [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) method.</span></span>

<span data-ttu-id="90a16-183">**Windows Server 2008:** Essa propriedade não está disponível antes do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="90a16-183">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-184">**ClipboardDisabled**</span><span class="sxs-lookup"><span data-stu-id="90a16-184">**ClipboardDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-185">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-187">Indica se o redirecionamento da área de transferência será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="90a16-187">Indicates if clipboard redirection will be disabled.</span></span> <span data-ttu-id="90a16-188">Essa propriedade terá efeito somente se a propriedade **DeviceRedirectionType** tiver um valor de "2".</span><span class="sxs-lookup"><span data-stu-id="90a16-188">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="90a16-189">**ComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="90a16-189">**ComputerGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90a16-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-192">Lista de nomes de grupos de computadores separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="90a16-192">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="90a16-193">Esse valor pode estar vazio.</span><span class="sxs-lookup"><span data-stu-id="90a16-193">This value can be empty.</span></span> <span data-ttu-id="90a16-194">Os nomes são do formato *domínio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="90a16-194">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="90a16-195">Se um valor for especificado, o computador cliente deverá pertencer a um desses grupos de computadores para que o usuário acesse o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="90a16-195">If a value is specified, then the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-196">**CookieAuthenticationAllowed**</span><span class="sxs-lookup"><span data-stu-id="90a16-196">**CookieAuthenticationAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-197">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-199">Indica se a autenticação de cookie pode ser usada para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="90a16-199">Indicates if cookie authentication can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="90a16-200">Essa propriedade pode ser definida usando o método [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="90a16-200">This property can be set by using the [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="90a16-201">**Windows Server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="90a16-201">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-202">**DeviceRedirectionType**</span><span class="sxs-lookup"><span data-stu-id="90a16-202">**DeviceRedirectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-203">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90a16-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-205">Especifica quais dispositivos serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="90a16-205">Specifies which devices will be redirected.</span></span>

<dt>

<span data-ttu-id="90a16-206">0</span><span class="sxs-lookup"><span data-stu-id="90a16-206">0</span></span>
</dt> <dd>

<span data-ttu-id="90a16-207">Todos os dispositivos serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="90a16-207">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-208">1</span><span class="sxs-lookup"><span data-stu-id="90a16-208">1</span></span>
</dt> <dd>

<span data-ttu-id="90a16-209">Nenhum dispositivo será redirecionado.</span><span class="sxs-lookup"><span data-stu-id="90a16-209">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-210">2</span><span class="sxs-lookup"><span data-stu-id="90a16-210">2</span></span>
</dt> <dd>

<span data-ttu-id="90a16-211">Os dispositivos especificados não serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="90a16-211">Specified devices will not be redirected.</span></span> <span data-ttu-id="90a16-212">As propriedades **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** e **PlugAndPlayDevicesDisabled** controlam quais dispositivos não serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="90a16-212">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="90a16-213">**DiskDrivesDisabled**</span><span class="sxs-lookup"><span data-stu-id="90a16-213">**DiskDrivesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-214">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-216">Indica se o redirecionamento de unidade de disco será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="90a16-216">Indicates if disk drive redirection will be disabled.</span></span> <span data-ttu-id="90a16-217">Essa propriedade terá efeito somente se a propriedade **DeviceRedirectionType** tiver um valor de "2".</span><span class="sxs-lookup"><span data-stu-id="90a16-217">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="90a16-218">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="90a16-218">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-219">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-221">Indica se este RD CAP será usado para avaliar um usuário para autorização.</span><span class="sxs-lookup"><span data-stu-id="90a16-221">Indicates whether this RD CAP will be used to evaluate a user for authorization.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-222">**HasNapAttributes**</span><span class="sxs-lookup"><span data-stu-id="90a16-222">**HasNapAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-223">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-225">Indica se o RD CAP usa atributos NAP (proteção de acesso à rede).</span><span class="sxs-lookup"><span data-stu-id="90a16-225">Indicates if the RD CAP uses Network Access Protection (NAP) attributes.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-226">**IdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="90a16-226">**IdleTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-227">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90a16-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-229">O valor de tempo limite de ociosidade, em minutos.</span><span class="sxs-lookup"><span data-stu-id="90a16-229">The idle timeout value, in minutes.</span></span> <span data-ttu-id="90a16-230">Um valor de 0 significa que não há nenhum tempo limite.</span><span class="sxs-lookup"><span data-stu-id="90a16-230">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="90a16-231">Essa propriedade pode ser definida usando o método [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="90a16-231">This property can be set by using the [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="90a16-232">**Windows Server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="90a16-232">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-233">**Nome**</span><span class="sxs-lookup"><span data-stu-id="90a16-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90a16-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90a16-236">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90a16-236">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="90a16-237">Nome do RD CAP.</span><span class="sxs-lookup"><span data-stu-id="90a16-237">Name of the RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-238">**Ordem**</span><span class="sxs-lookup"><span data-stu-id="90a16-238">**Order**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-239">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90a16-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-241">Ordem de avaliação do RD CAP.</span><span class="sxs-lookup"><span data-stu-id="90a16-241">Evaluation order of the RD CAP.</span></span> <span data-ttu-id="90a16-242">A primeira RD CAP avaliada tem um valor de "1".</span><span class="sxs-lookup"><span data-stu-id="90a16-242">The first RD CAP evaluated has a value of "1".</span></span> <span data-ttu-id="90a16-243">A propriedade **Order** pode ser alterada quando os [**métodos Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**moveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)ou [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) são chamados.</span><span class="sxs-lookup"><span data-stu-id="90a16-243">The **Order** property can be changed when the [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md), or [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-244">**PasswordAllowed**</span><span class="sxs-lookup"><span data-stu-id="90a16-244">**PasswordAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-245">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-247">Indica se uma senha pode ser usada para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="90a16-247">Indicates if a password can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="90a16-248">Essa propriedade pode ser alterada usando o método [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="90a16-248">This property can be changed by using the [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-249">**PlugAndPlayDevicesDisabled**</span><span class="sxs-lookup"><span data-stu-id="90a16-249">**PlugAndPlayDevicesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-250">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-252">Indica se o redirecionamento de dispositivos Plug and Play será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="90a16-252">Indicates if redirection of Plug and Play devices will be disabled.</span></span> <span data-ttu-id="90a16-253">Essa propriedade terá efeito somente se a propriedade **DeviceRedirectionType** tiver um valor de "2".</span><span class="sxs-lookup"><span data-stu-id="90a16-253">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="90a16-254">**PrintersDisabled**</span><span class="sxs-lookup"><span data-stu-id="90a16-254">**PrintersDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-255">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-257">Indica se o redirecionamento de impressora será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="90a16-257">Indicates if printer redirection will be disabled.</span></span> <span data-ttu-id="90a16-258">Essa propriedade terá efeito somente se a propriedade **DeviceRedirectionType** tiver um valor de "2".</span><span class="sxs-lookup"><span data-stu-id="90a16-258">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="90a16-259">**SecureIdAllowed**</span><span class="sxs-lookup"><span data-stu-id="90a16-259">**SecureIdAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-260">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-260">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-262">Indica se um identificador seguro pode ser usado para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="90a16-262">Indicates if a secure identifier can be used to connect to the RD Gateway server.</span></span>

<span data-ttu-id="90a16-263">**Windows Server 2008:** Essa propriedade não é usada.</span><span class="sxs-lookup"><span data-stu-id="90a16-263">**Windows Server 2008:** This property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-264">**SerialPortsDisabled**</span><span class="sxs-lookup"><span data-stu-id="90a16-264">**SerialPortsDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-265">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-267">Indica se o redirecionamento de porta serial será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="90a16-267">Indicates if serial port redirection will be disabled.</span></span> <span data-ttu-id="90a16-268">Essa propriedade terá efeito somente se a propriedade **DeviceRedirectionType** tiver um valor de "2".</span><span class="sxs-lookup"><span data-stu-id="90a16-268">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="90a16-269">**SessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="90a16-269">**SessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-270">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90a16-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-272">O valor de tempo limite da sessão, em minutos.</span><span class="sxs-lookup"><span data-stu-id="90a16-272">The session timeout value, in minutes.</span></span> <span data-ttu-id="90a16-273">Um valor de 0 significa que não há nenhum tempo limite.</span><span class="sxs-lookup"><span data-stu-id="90a16-273">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="90a16-274">Essa propriedade pode ser definida usando o método [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="90a16-274">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="90a16-275">**Windows Server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="90a16-275">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-276">**SessionTimeoutAction**</span><span class="sxs-lookup"><span data-stu-id="90a16-276">**SessionTimeoutAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-277">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90a16-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-279">Especifica a ação a ser executada no caso de um tempo limite de sessão.</span><span class="sxs-lookup"><span data-stu-id="90a16-279">Specifies the action to be taken in the case of a session timeout.</span></span> <span data-ttu-id="90a16-280">Essa propriedade pode ser definida usando o método [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="90a16-280">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="90a16-281">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="90a16-281">This can be one of the following values.</span></span>

<span data-ttu-id="90a16-282">**Windows Server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="90a16-282">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="90a16-283">0</span><span class="sxs-lookup"><span data-stu-id="90a16-283">0</span></span>
</dt> <dd>

<span data-ttu-id="90a16-284">Desconecte a sessão.</span><span class="sxs-lookup"><span data-stu-id="90a16-284">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-285">1</span><span class="sxs-lookup"><span data-stu-id="90a16-285">1</span></span>
</dt> <dd>

<span data-ttu-id="90a16-286">Tentativa de autorizar a sessão novamente.</span><span class="sxs-lookup"><span data-stu-id="90a16-286">Attempt to re-authorize the session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="90a16-287">**SmartcardAllowed**</span><span class="sxs-lookup"><span data-stu-id="90a16-287">**SmartcardAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-288">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90a16-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-290">Indica se um cartão inteligente pode ser usado para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="90a16-290">Indicates if a smart card can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="90a16-291">Essa propriedade pode ser alterada usando o método [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="90a16-291">This property can be changed by using the [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="90a16-292">**Usergroupnames**</span><span class="sxs-lookup"><span data-stu-id="90a16-292">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90a16-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90a16-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90a16-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90a16-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90a16-295">Lista de nomes de grupos de usuários separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="90a16-295">List of semicolon-separated user group names.</span></span> <span data-ttu-id="90a16-296">Os nomes são do formato *domínio \\ userGroupName*.</span><span class="sxs-lookup"><span data-stu-id="90a16-296">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="90a16-297">Se o usuário pertencer a qualquer um desses grupos de usuários, o usuário terá permissão para acessar o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="90a16-297">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90a16-298">Comentários</span><span class="sxs-lookup"><span data-stu-id="90a16-298">Remarks</span></span>

<span data-ttu-id="90a16-299">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="90a16-299">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="90a16-300">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="90a16-300">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="90a16-301">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="90a16-301">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="90a16-302">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="90a16-302">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="90a16-303">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="90a16-303">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="90a16-304">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90a16-304">Requirements</span></span>



| <span data-ttu-id="90a16-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="90a16-305">Requirement</span></span> | <span data-ttu-id="90a16-306">Valor</span><span class="sxs-lookup"><span data-stu-id="90a16-306">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="90a16-307">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90a16-307">Minimum supported client</span></span><br/> | <span data-ttu-id="90a16-308">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="90a16-308">None supported</span></span><br/>                                                                |
| <span data-ttu-id="90a16-309">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90a16-309">Minimum supported server</span></span><br/> | <span data-ttu-id="90a16-310">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90a16-310">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="90a16-311">Namespace</span><span class="sxs-lookup"><span data-stu-id="90a16-311">Namespace</span></span><br/>                | <span data-ttu-id="90a16-312">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="90a16-312">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="90a16-313">MOF</span><span class="sxs-lookup"><span data-stu-id="90a16-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90a16-314"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90a16-314"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="90a16-315">DLL</span><span class="sxs-lookup"><span data-stu-id="90a16-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90a16-316"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90a16-316"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="90a16-317">Confira também</span><span class="sxs-lookup"><span data-stu-id="90a16-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a16-318">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="90a16-318">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="90a16-319">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="90a16-319">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="90a16-320">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="90a16-320">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="90a16-321">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="90a16-321">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="90a16-322">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="90a16-322">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="90a16-323">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="90a16-323">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

