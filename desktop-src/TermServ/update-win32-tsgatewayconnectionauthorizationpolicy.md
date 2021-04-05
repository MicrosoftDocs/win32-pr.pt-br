---
title: Método Update da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Atualiza a política de autorização de conexão do Área de Trabalho Remota atual (RD \ 160; CAP).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de atualização
- Método Update Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Serviços de Área de Trabalho Remota de classe Win32_TSGatewayConnectionAuthorizationPolicy, método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b982030170e954342dc5ff99754dcb89afd0e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009442"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="4ebff-106">Método Update da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="4ebff-106">Update method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="4ebff-107">Atualiza a RD CAP (política de autorização de conexão) do Área de Trabalho Remota atual.</span><span class="sxs-lookup"><span data-stu-id="4ebff-107">Updates the current Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebff-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ebff-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a><span data-ttu-id="4ebff-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ebff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ebff-110">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-111">Nome do RD CAP.</span><span class="sxs-lookup"><span data-stu-id="4ebff-111">Name of the RD CAP.</span></span> <span data-ttu-id="4ebff-112">O nome deve ter 64 caracteres ou menos, exclusivo (o caso é ignorado) e não pode conter os seguintes caracteres reservados:</span><span class="sxs-lookup"><span data-stu-id="4ebff-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="4ebff-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="4ebff-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="4ebff-114">\*\[Guia\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-114">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-115">*Usergroupnames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-115">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-116">Lista de nomes de grupos de usuários separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="4ebff-116">List of semicolon-separated user group names.</span></span> <span data-ttu-id="4ebff-117">Os nomes são do formato *domínio \\ userGroupName*.</span><span class="sxs-lookup"><span data-stu-id="4ebff-117">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="4ebff-118">Se o usuário pertencer a qualquer um desses grupos de usuários, o usuário terá permissão para acessar o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="4ebff-118">If the user belongs to any one of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-119">*ComputerGroupNames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-120">Lista de nomes de grupos de computadores separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="4ebff-120">List of semicolon-separated machine group names.</span></span> <span data-ttu-id="4ebff-121">Esse valor pode estar vazio.</span><span class="sxs-lookup"><span data-stu-id="4ebff-121">This value can be empty.</span></span> <span data-ttu-id="4ebff-122">Os nomes são do formato *domínio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="4ebff-122">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="4ebff-123">Se um valor for especificado, o computador cliente deverá pertencer a um desses grupos de computadores para que o usuário acesse o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="4ebff-123">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-124">*Cartão inteligente* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-124">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-125">Especifica se os cartões inteligentes podem ser usados para autenticar com o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="4ebff-125">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-126">*Senha* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-126">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-127">Especifica se as senhas podem ser usadas para autenticar com o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="4ebff-127">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-128">*Segurança segura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-128">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-129">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4ebff-129">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-130">*Habilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-130">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-131">Especifica se este RD CAP está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4ebff-131">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-132">*DeviceRedirectionType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-132">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-133">Especifica quais tipos de dispositivo serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="4ebff-133">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="4ebff-134">0</span><span class="sxs-lookup"><span data-stu-id="4ebff-134">0</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-135">Todos os dispositivos serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="4ebff-135">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-136">1</span><span class="sxs-lookup"><span data-stu-id="4ebff-136">1</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-137">Nenhum dispositivo será redirecionado.</span><span class="sxs-lookup"><span data-stu-id="4ebff-137">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-138">2</span><span class="sxs-lookup"><span data-stu-id="4ebff-138">2</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-139">Os dispositivos especificados não serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="4ebff-139">Specified devices will not be redirected.</span></span> <span data-ttu-id="4ebff-140">Os parâmetros *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* e *PlugAndPlayDevicesDisabled* controlam quais dispositivos não serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="4ebff-140">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4ebff-141">*DiskDrivesDisabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-141">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-142">Especifica se o redirecionamento de unidade de disco será desabilitado se o parâmetro *DeviceRedirectionType* for "2".</span><span class="sxs-lookup"><span data-stu-id="4ebff-142">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-143">*PrintersDisabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-143">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-144">Especifica se o redirecionamento de impressora deve ser desabilitado se o parâmetro *DeviceRedirectionType* for "2".</span><span class="sxs-lookup"><span data-stu-id="4ebff-144">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-145">*SerialPortsDisabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-145">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-146">Especifica se o redirecionamento de porta serial deve ser desabilitado se o parâmetro *DeviceRedirectionType* for "2".</span><span class="sxs-lookup"><span data-stu-id="4ebff-146">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-147">*ClipboardDisabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-147">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-148">Especifica se o redirecionamento da área de transferência deve ser desabilitado se o parâmetro *DeviceRedirectionType* for "2".</span><span class="sxs-lookup"><span data-stu-id="4ebff-148">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-149">*PlugAndPlayDevicesDisabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-149">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-150">Especifica se é para desabilitar o redirecionamento de dispositivos Plug and Play se o parâmetro *DeviceRedirectionType* for "2".</span><span class="sxs-lookup"><span data-stu-id="4ebff-150">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-151">*IdleTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-151">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-152">Valor de tempo limite de ociosidade em minutos</span><span class="sxs-lookup"><span data-stu-id="4ebff-152">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-153">*SessionTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-153">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-154">Valor de tempo limite da sessão em minutos</span><span class="sxs-lookup"><span data-stu-id="4ebff-154">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-155">*SessionTimeoutAction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-155">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-156">Ação de tempo limite da sessão em minutos</span><span class="sxs-lookup"><span data-stu-id="4ebff-156">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-157">*AllowOnlySDRServers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-157">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-158">Se as conexões são permitidas apenas para servidores TS SDR</span><span class="sxs-lookup"><span data-stu-id="4ebff-158">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="4ebff-159">*CookieAuthentication* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebff-159">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebff-160">Indica se a autenticação de cookie pode ser usada para se conectar ao servidor Gateway TS</span><span class="sxs-lookup"><span data-stu-id="4ebff-160">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ebff-161">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ebff-161">Return value</span></span>

<span data-ttu-id="4ebff-162">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="4ebff-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4ebff-163">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="4ebff-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4ebff-164">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4ebff-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ebff-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ebff-165">Remarks</span></span>

<span data-ttu-id="4ebff-166">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="4ebff-166">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4ebff-167">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4ebff-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4ebff-168">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4ebff-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4ebff-169">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="4ebff-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4ebff-170">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4ebff-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ebff-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ebff-171">Requirements</span></span>



| <span data-ttu-id="4ebff-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ebff-172">Requirement</span></span> | <span data-ttu-id="4ebff-173">Valor</span><span class="sxs-lookup"><span data-stu-id="4ebff-173">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ebff-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ebff-174">Minimum supported client</span></span><br/> | <span data-ttu-id="4ebff-175">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4ebff-175">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4ebff-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ebff-176">Minimum supported server</span></span><br/> | <span data-ttu-id="4ebff-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ebff-177">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4ebff-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ebff-178">Namespace</span></span><br/>                | <span data-ttu-id="4ebff-179">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="4ebff-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4ebff-180">MOF</span><span class="sxs-lookup"><span data-stu-id="4ebff-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ebff-181"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ebff-181"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ebff-182">DLL</span><span class="sxs-lookup"><span data-stu-id="4ebff-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ebff-183"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ebff-183"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4ebff-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ebff-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ebff-185">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="4ebff-185">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

