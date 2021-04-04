---
title: Método CanAccessLicenseServer da classe Win32_TerminalServiceSetting
description: O CanAccessLicenseServer não está mais disponível.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CanAccessLicenseServer
- Método CanAccessLicenseServer Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método CanAccessLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085310"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="151a1-106">Método CanAccessLicenseServer da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="151a1-106">CanAccessLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="151a1-107">\[O **CanAccessLicenseServer** não está mais disponível para uso a partir do Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="151a1-107">\[**CanAccessLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="151a1-108">\* \* Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="151a1-108">\*\*Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="151a1-109">Determina se o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) tem permissão para solicitar Serviços de Área de Trabalho Remota CALs (licenças de acesso para cliente) de um servidor de licença Área de Trabalho Remota com base no seguinte:</span><span class="sxs-lookup"><span data-stu-id="151a1-109">Determines whether the Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server based on the following:</span></span>

-   <span data-ttu-id="151a1-110">A configuração da política de grupo "grupo de segurança do servidor de licenças" no servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="151a1-110">The "license server security group" group policy setting on the Remote Desktop license server.</span></span>
-   <span data-ttu-id="151a1-111">Associação no grupo local computadores Terminal Server no servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="151a1-111">Membership in the Terminal Server Computers local group on the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="151a1-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="151a1-112">Syntax</span></span>


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="151a1-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="151a1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="151a1-114">*Nome do Server* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="151a1-114">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="151a1-115">O nome do servidor de licença de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="151a1-115">The name of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="151a1-116">*AccessAllowed* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="151a1-116">*AccessAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="151a1-117">Se o servidor de Host da Sessão RD tem permissão para solicitar RDS CALs do servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="151a1-117">Whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

<dt>

<span data-ttu-id="151a1-118">0</span><span class="sxs-lookup"><span data-stu-id="151a1-118">0</span></span>
</dt> <dd>

<span data-ttu-id="151a1-119">A solicitação é permitida.</span><span class="sxs-lookup"><span data-stu-id="151a1-119">The request is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="151a1-120">1</span><span class="sxs-lookup"><span data-stu-id="151a1-120">1</span></span>
</dt> <dd>

<span data-ttu-id="151a1-121">A solicitação não é permitida.</span><span class="sxs-lookup"><span data-stu-id="151a1-121">The request is not allowed.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="151a1-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="151a1-122">Return value</span></span>

<span data-ttu-id="151a1-123">Retornará **S \_ OK** se o servidor de host da Sessão RD tiver acesso ao servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="151a1-123">Returns **S\_OK** if the RD Session Host server has access to the license server.</span></span> <span data-ttu-id="151a1-124">Retornará **S \_ false** se o servidor de host da Sessão RD não tiver acesso ao servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="151a1-124">Returns **S\_FALSE** if the RD Session Host server does not have access to the license server.</span></span>

## <a name="remarks"></a><span data-ttu-id="151a1-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="151a1-125">Remarks</span></span>

<span data-ttu-id="151a1-126">A configuração de política "grupo de segurança de servidor de licenças" permite que você especifique os servidores de Host da Sessão RD que têm permissão para contatar o servidor de licença para obter RDS CALs.</span><span class="sxs-lookup"><span data-stu-id="151a1-126">The "license server security group" policy setting allows you to specify the RD Session Host servers that are permitted to contact the license server to obtain RDS CALs.</span></span> <span data-ttu-id="151a1-127">Se a configuração de política estiver habilitada no servidor de licença, o servidor de licença responderá apenas às solicitações de RDS CAL de Host da Sessão RD servidores cujas contas de computador são membros do grupo local de computadores Terminal Server no servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="151a1-127">If the policy setting is enabled on the license server, the license server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="151a1-128">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="151a1-128">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="151a1-129">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="151a1-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="151a1-130">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="151a1-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="151a1-131">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="151a1-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="151a1-132">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="151a1-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="151a1-133">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="151a1-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="151a1-134">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="151a1-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="151a1-135">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="151a1-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="151a1-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="151a1-136">Requirements</span></span>



| <span data-ttu-id="151a1-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="151a1-137">Requirement</span></span> | <span data-ttu-id="151a1-138">Valor</span><span class="sxs-lookup"><span data-stu-id="151a1-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="151a1-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="151a1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="151a1-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="151a1-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="151a1-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="151a1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="151a1-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="151a1-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="151a1-143">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="151a1-143">End of client support</span></span><br/>    | <span data-ttu-id="151a1-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="151a1-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="151a1-145">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="151a1-145">End of server support</span></span><br/>    | <span data-ttu-id="151a1-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="151a1-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="151a1-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="151a1-147">Namespace</span></span><br/>                | <span data-ttu-id="151a1-148">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="151a1-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="151a1-149">MOF</span><span class="sxs-lookup"><span data-stu-id="151a1-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="151a1-150"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="151a1-150"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="151a1-151">DLL</span><span class="sxs-lookup"><span data-stu-id="151a1-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="151a1-152"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="151a1-152"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="151a1-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="151a1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="151a1-154">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="151a1-154">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

