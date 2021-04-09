---
title: Método Create da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Cria uma política de autorização de conexão Área de Trabalho Remota (RD \ 160; CAP) usando os valores especificados. A nova RD \ 160; A CAP será inserida na parte superior da área de trabalho remota \ 160; Ordem de avaliação de CAP, com um valor de propriedade de ordem de \ 0034; 1 \ 0034;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Criar Serviços de Área de Trabalho Remota do método
- Criar método Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método Create
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc027c2f7fc90318bd1af6fd1254077a860a5d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009033"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="ad9b2-107">Método Create da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="ad9b2-107">Create method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="ad9b2-108">Cria uma Área de Trabalho Remota política de autorização de conexão (RD CAP) usando os valores especificados.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-108">Creates a Remote Desktop connection authorization policy (RD CAP) by using the specified values.</span></span> <span data-ttu-id="ad9b2-109">O novo RD CAP será inserido na parte superior da ordem de avaliação de RD CAP, com um valor de propriedade de **ordem** de "1".</span><span class="sxs-lookup"><span data-stu-id="ad9b2-109">The new RD CAP will be inserted at the top of the RD CAP evaluation order, with an **Order** property value of "1".</span></span>

## <a name="syntax"></a><span data-ttu-id="ad9b2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad9b2-110">Syntax</span></span>


```mof
uint32 Create(
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



## <a name="parameters"></a><span data-ttu-id="ad9b2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad9b2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad9b2-112">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-113">Nome do RD CAP.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-113">Name of the RD CAP.</span></span> <span data-ttu-id="ad9b2-114">O nome deve ter 64 caracteres ou menos, exclusivo (o caso é ignorado) e não pode conter os seguintes caracteres reservados:</span><span class="sxs-lookup"><span data-stu-id="ad9b2-114">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="ad9b2-115"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="ad9b2-115"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="ad9b2-116">\*\[Guia\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-116">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-117">*Usergroupnames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-117">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-118">Lista de nomes de grupos de usuários, separados por ponto e vírgula, para o novo RD CAP.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-118">List of user group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-119">*ComputerGroupNames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-120">Lista de nomes de grupos de computadores, separados por ponto e vírgula, para o novo RD CAP.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-120">List of computer group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-121">*Cartão inteligente* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-121">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-122">Especifica se os cartões inteligentes podem ser usados para autenticar com o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-122">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-123">*Senha* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-123">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-124">Especifica se as senhas podem ser usadas para autenticar com o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-124">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-125">*Segurança segura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-125">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-126">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-126">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-127">*Habilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-128">Especifica se este RD CAP está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-128">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-129">*DeviceRedirectionType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-129">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-130">Especifica quais tipos de dispositivo serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-130">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="ad9b2-131">0</span><span class="sxs-lookup"><span data-stu-id="ad9b2-131">0</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-132">Todos os dispositivos serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-132">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-133">1</span><span class="sxs-lookup"><span data-stu-id="ad9b2-133">1</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-134">Nenhum dispositivo será redirecionado.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-134">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-135">2</span><span class="sxs-lookup"><span data-stu-id="ad9b2-135">2</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-136">Os dispositivos especificados não serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-136">Specified devices will not be redirected.</span></span> <span data-ttu-id="ad9b2-137">Os parâmetros *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* e *PlugAndPlayDevicesDisabled* controlam quais dispositivos não serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-137">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ad9b2-138">*DiskDrivesDisabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-138">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-139">Especifica se o redirecionamento de unidade de disco será desabilitado se o parâmetro *DeviceRedirectionType* for "2".</span><span class="sxs-lookup"><span data-stu-id="ad9b2-139">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-140">*PrintersDisabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-140">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-141">Especifica se o redirecionamento de impressora deve ser desabilitado se o parâmetro *DeviceRedirectionType* for "2".</span><span class="sxs-lookup"><span data-stu-id="ad9b2-141">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-142">*SerialPortsDisabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-142">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-143">Especifica se o redirecionamento de porta serial deve ser desabilitado se o parâmetro *DeviceRedirectionType* for "2".</span><span class="sxs-lookup"><span data-stu-id="ad9b2-143">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-144">*ClipboardDisabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-144">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-145">Especifica se o redirecionamento da área de transferência deve ser desabilitado se o parâmetro *DeviceRedirectionType* for "2".</span><span class="sxs-lookup"><span data-stu-id="ad9b2-145">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-146">*PlugAndPlayDevicesDisabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-146">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-147">Especifica se é para desabilitar o redirecionamento de dispositivos Plug and Play se o parâmetro *DeviceRedirectionType* for "2".</span><span class="sxs-lookup"><span data-stu-id="ad9b2-147">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-148">*IdleTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-148">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-149">Valor de tempo limite de ociosidade em minutos</span><span class="sxs-lookup"><span data-stu-id="ad9b2-149">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-150">*SessionTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-150">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-151">Valor de tempo limite da sessão em minutos</span><span class="sxs-lookup"><span data-stu-id="ad9b2-151">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-152">*SessionTimeoutAction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-152">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-153">Ação de tempo limite da sessão em minutos</span><span class="sxs-lookup"><span data-stu-id="ad9b2-153">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-154">*AllowOnlySDRServers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-154">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-155">Se as conexões são permitidas apenas para servidores TS SDR</span><span class="sxs-lookup"><span data-stu-id="ad9b2-155">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="ad9b2-156">*CookieAuthentication* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad9b2-156">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9b2-157">Indica se a autenticação de cookie pode ser usada para se conectar ao servidor Gateway TS</span><span class="sxs-lookup"><span data-stu-id="ad9b2-157">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad9b2-158">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad9b2-158">Return value</span></span>

<span data-ttu-id="ad9b2-159">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-159">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ad9b2-160">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-160">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ad9b2-161">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ad9b2-161">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad9b2-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad9b2-162">Remarks</span></span>

<span data-ttu-id="ad9b2-163">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-163">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ad9b2-164">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ad9b2-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ad9b2-165">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ad9b2-166">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="ad9b2-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ad9b2-167">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ad9b2-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad9b2-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad9b2-168">Requirements</span></span>



| <span data-ttu-id="ad9b2-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad9b2-169">Requirement</span></span> | <span data-ttu-id="ad9b2-170">Valor</span><span class="sxs-lookup"><span data-stu-id="ad9b2-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9b2-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad9b2-171">Minimum supported client</span></span><br/> | <span data-ttu-id="ad9b2-172">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ad9b2-172">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ad9b2-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad9b2-173">Minimum supported server</span></span><br/> | <span data-ttu-id="ad9b2-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad9b2-174">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ad9b2-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad9b2-175">Namespace</span></span><br/>                | <span data-ttu-id="ad9b2-176">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="ad9b2-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ad9b2-177">MOF</span><span class="sxs-lookup"><span data-stu-id="ad9b2-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad9b2-178"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad9b2-178"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad9b2-179">DLL</span><span class="sxs-lookup"><span data-stu-id="ad9b2-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad9b2-180"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad9b2-180"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ad9b2-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad9b2-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9b2-182">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="ad9b2-182">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

