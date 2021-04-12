---
title: Método GetTStoLSConnectivityStatus da classe Win32_TerminalServiceSetting
description: Determina o status de conectividade entre Serviços de Área de Trabalho Remota e um servidor de licença.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetTStoLSConnectivityStatus
- Método GetTStoLSConnectivityStatus Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método GetTStoLSConnectivityStatus
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455390"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="31127-106">Método GetTStoLSConnectivityStatus da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="31127-106">GetTStoLSConnectivityStatus method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="31127-107">Determina o status de conectividade entre Serviços de Área de Trabalho Remota e um servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="31127-107">Determines the connectivity status between Remote Desktop Services and a license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="31127-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31127-108">Syntax</span></span>


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a><span data-ttu-id="31127-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31127-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31127-110">*Nome do Server* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31127-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31127-111">O nome do servidor de licença para verificar o status de conectividade.</span><span class="sxs-lookup"><span data-stu-id="31127-111">The name of the license server to check the connectivity status of.</span></span>

</dd> <dt>

<span data-ttu-id="31127-112">*TStoLSConnectivityStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31127-112">*TStoLSConnectivityStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31127-113">Um valor que indica o status de conectividade do servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="31127-113">A value that indicates the connectivity status of the license server.</span></span> <span data-ttu-id="31127-114">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="31127-114">This can be one of the following values.</span></span>

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span data-ttu-id="31127-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**Ls \_ CONECTADO \_ desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="31127-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS\_CONNECTABLE\_UNKNOWN** (0)</span></span>


</dt> <dd>

<span data-ttu-id="31127-116">Não é possível determinar o status de conectividade.</span><span class="sxs-lookup"><span data-stu-id="31127-116">The connectivity status cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span data-ttu-id="31127-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**Ls \_ \_ \_ WS08R2 válido conectável** (1)</span><span class="sxs-lookup"><span data-stu-id="31127-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS\_CONNECTABLE\_VALID\_WS08R2** (1)</span></span>


</dt> <dd>

<span data-ttu-id="31127-118">Serviços de Área de Trabalho Remota pode se conectar ao servidor de licença do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="31127-118">Remote Desktop Services can connect to the Windows Server 2008 R2 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span data-ttu-id="31127-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**Ls \_ \_ \_ WS08 válido conectável** (2)</span><span class="sxs-lookup"><span data-stu-id="31127-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS\_CONNECTABLE\_VALID\_WS08** (2)</span></span>


</dt> <dd>

<span data-ttu-id="31127-120">Serviços de Área de Trabalho Remota pode se conectar ao servidor de licença do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="31127-120">Remote Desktop Services can connect to the Windows Server 2008 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span data-ttu-id="31127-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**Ls \_ Incompatibilidade \_ de \_ RTM \_ beta connectável** (3)</span><span class="sxs-lookup"><span data-stu-id="31127-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS\_CONNECTABLE\_BETA\_RTM\_MISMATCH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="31127-122">Serviços de Área de Trabalho Remota pode se conectar ao servidor de licença, mas um dos servidores está executando uma versão beta do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="31127-122">Remote Desktop Services can connect to the license server, but one of the servers is running a beta version of the operating system.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span data-ttu-id="31127-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**Ls \_ \_ \_ Versão inferior conectável** (4)</span><span class="sxs-lookup"><span data-stu-id="31127-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS\_CONNECTABLE\_LOWER\_VERSION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="31127-124">Serviços de Área de Trabalho Remota pode se conectar ao servidor de licença, mas há uma incompatibilidade entre o servidor de licença e o servidor host Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="31127-124">Remote Desktop Services can connect to the license server, but there is an incompatibility between the license server and the Remote Desktop Services host server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span data-ttu-id="31127-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**Ls \_ CONNECTável \_ não está \_ em \_ TSCGROUP** (5)</span><span class="sxs-lookup"><span data-stu-id="31127-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS\_CONNECTABLE\_NOT\_IN\_TSCGROUP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="31127-126">A política de grupo de segurança está habilitada no servidor de licença, mas Serviços de Área de Trabalho Remota não faz parte da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="31127-126">Security group policy is enabled in license server, but Remote Desktop Services is not a part of the group policy.</span></span>

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span data-ttu-id="31127-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**Ls \_ Não \_ conectável** (6)</span><span class="sxs-lookup"><span data-stu-id="31127-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS\_NOT\_CONNECTABLE** (6)</span></span>


</dt> <dd>

<span data-ttu-id="31127-128">Serviços de Área de Trabalho Remota não pode se conectar ao servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="31127-128">Remote Desktop Services cannot connect to the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span data-ttu-id="31127-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**Ls \_ \_ \_ Validade de conexão desconhecida** (7)</span><span class="sxs-lookup"><span data-stu-id="31127-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS\_CONNECTABLE\_UNKNOWN\_VALIDITY** (7)</span></span>


</dt> <dd>

<span data-ttu-id="31127-130">O servidor de licenças pode ser conectado ao, mas a validade da conexão não pode ser determinada.</span><span class="sxs-lookup"><span data-stu-id="31127-130">The license server can be connected to, but the validity of the connection cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span data-ttu-id="31127-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**Ls \_ CONNECTável \_ , mas \_ acesso \_ negado** (8)</span><span class="sxs-lookup"><span data-stu-id="31127-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS\_CONNECTABLE\_BUT\_ACCESS\_DENIED** (8)</span></span>


</dt> <dd>

<span data-ttu-id="31127-132">Serviços de Área de Trabalho Remota pode se conectar ao servidor de licença, mas a conta de usuário não tem privilégios de administrador no servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="31127-132">Remote Desktop Services can connect to the license server, but the user account does not have administrator privileges on the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span data-ttu-id="31127-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**Ls \_ \_ \_ \_ VDI WS08R2 válido e conectável** (9)</span><span class="sxs-lookup"><span data-stu-id="31127-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS\_CONNECTABLE\_VALID\_WS08R2\_VDI** (9)</span></span>


</dt> <dd>

<span data-ttu-id="31127-134">Serviços de Área de Trabalho Remota pode se conectar ao servidor do Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI).</span><span class="sxs-lookup"><span data-stu-id="31127-134">Remote Desktop Services can connect to the Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI) server.</span></span>

<span data-ttu-id="31127-135">**Windows Server 2008 R2:** Não há suporte para esse valor antes do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="31127-135">**Windows Server 2008 R2:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span data-ttu-id="31127-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**Ls \_ \_ \_ Não \_ há suporte para o recurso conectável** (10)</span><span class="sxs-lookup"><span data-stu-id="31127-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS\_CONNECTABLE\_FEATURE\_NOT\_SUPPORTED** (10)</span></span>


</dt> <dd>

<span data-ttu-id="31127-137">Não há suporte para o recurso.</span><span class="sxs-lookup"><span data-stu-id="31127-137">The feature is not supported.</span></span>

<span data-ttu-id="31127-138">**Windows server 2008 R2 e Windows server 2008 R2 com SP1:** Não há suporte para esse valor antes do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="31127-138">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span data-ttu-id="31127-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**Ls \_ \_ \_ Ls válido conectável** (11)</span><span class="sxs-lookup"><span data-stu-id="31127-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS\_CONNECTABLE\_VALID\_LS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="31127-140">O servidor de licença é válido.</span><span class="sxs-lookup"><span data-stu-id="31127-140">The license server is valid.</span></span>

<span data-ttu-id="31127-141">**Windows server 2008 R2 e Windows server 2008 R2 com SP1:** Não há suporte para esse valor antes do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="31127-141">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31127-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31127-142">Return value</span></span>

<span data-ttu-id="31127-143">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="31127-143">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="31127-144">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="31127-144">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="31127-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31127-145">Requirements</span></span>



| <span data-ttu-id="31127-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="31127-146">Requirement</span></span> | <span data-ttu-id="31127-147">Valor</span><span class="sxs-lookup"><span data-stu-id="31127-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31127-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31127-148">Minimum supported client</span></span><br/> | <span data-ttu-id="31127-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="31127-149">None supported</span></span><br/>                                                               |
| <span data-ttu-id="31127-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31127-150">Minimum supported server</span></span><br/> | <span data-ttu-id="31127-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31127-151">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="31127-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="31127-152">Namespace</span></span><br/>                | <span data-ttu-id="31127-153">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="31127-153">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="31127-154">MOF</span><span class="sxs-lookup"><span data-stu-id="31127-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31127-155"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31127-155"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="31127-156">DLL</span><span class="sxs-lookup"><span data-stu-id="31127-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31127-157"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31127-157"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31127-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="31127-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31127-159">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="31127-159">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





