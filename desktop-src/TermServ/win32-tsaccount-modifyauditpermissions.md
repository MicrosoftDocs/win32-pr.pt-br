---
title: Método ModifyAuditPermissions da classe Win32_TSAccount
description: Prepara para definir um conjunto mais granular de permissões de auditoria para a conta especificada.
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ModifyAuditPermissions
- Método ModifyAuditPermissions Serviços de Área de Trabalho Remota, classe Win32_TSAccount
- Classe Win32_TSAccount Serviços de Área de Trabalho Remota, método ModifyAuditPermissions
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyAuditPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f19337cc6110a15b206fc437fb6ec594ded60640
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824728"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="951a2-106">Método ModifyAuditPermissions da classe Win32 \_ TSAccount</span><span class="sxs-lookup"><span data-stu-id="951a2-106">ModifyAuditPermissions method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="951a2-107">O método **ModifyAuditPermissions** se prepara para definir um conjunto mais granular de permissões de auditoria para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="951a2-107">The **ModifyAuditPermissions** method prepares to set a more granular set of audit permissions to the specified account.</span></span>

## <a name="syntax"></a><span data-ttu-id="951a2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="951a2-108">Syntax</span></span>


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a><span data-ttu-id="951a2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="951a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="951a2-110">*PermissionMask* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="951a2-110">*PermissionMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951a2-111">O conjunto de [permissões de host da sessão da área de trabalho remota](terminal-services-permissions.md) a ser associado à conta especificada.</span><span class="sxs-lookup"><span data-stu-id="951a2-111">The set of [Remote Desktop Session Host Permissions](terminal-services-permissions.md) to associate with the specified account.</span></span> <span data-ttu-id="951a2-112">O valor desse parâmetro é um bitmap, e qualquer um ou todos os valores a seguir podem ser selecionados.</span><span class="sxs-lookup"><span data-stu-id="951a2-112">The value of this parameter is a bitmap, and any or all of the following values may be selected.</span></span>

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span data-ttu-id="951a2-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION \_ CONSULTA** (0)</span><span class="sxs-lookup"><span data-stu-id="951a2-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION\_QUERY** (0)</span></span>


</dt> <dd>

<span data-ttu-id="951a2-114">Permissão para consultar informações sobre uma sessão.</span><span class="sxs-lookup"><span data-stu-id="951a2-114">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="951a2-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ DEFINIR** (1)</span><span class="sxs-lookup"><span data-stu-id="951a2-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (1)</span></span>


</dt> <dd>

<span data-ttu-id="951a2-116">Permissão para modificar os parâmetros de conexão.</span><span class="sxs-lookup"><span data-stu-id="951a2-116">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="951a2-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ REDEFINIR** (6)</span><span class="sxs-lookup"><span data-stu-id="951a2-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (6)</span></span>


</dt> <dd>

<span data-ttu-id="951a2-118">Permissão para redefinir ou encerrar uma sessão ou conexão.</span><span class="sxs-lookup"><span data-stu-id="951a2-118">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="951a2-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ \| Direitos padrão \_ virtuais \_ necessários** (3)</span><span class="sxs-lookup"><span data-stu-id="951a2-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="951a2-120">Permissão para usar canais virtuais.</span><span class="sxs-lookup"><span data-stu-id="951a2-120">Permission to use virtual channels.</span></span> <span data-ttu-id="951a2-121">Os canais virtuais fornecem acesso de um programa de servidor a dispositivos cliente.</span><span class="sxs-lookup"><span data-stu-id="951a2-121">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="951a2-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ SOMBRA** (4)</span><span class="sxs-lookup"><span data-stu-id="951a2-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (4)</span></span>


</dt> <dd>

<span data-ttu-id="951a2-123">Permissão para sombrear ou controlar remotamente a sessão de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="951a2-123">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="951a2-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ LOGON** (5)</span><span class="sxs-lookup"><span data-stu-id="951a2-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (5)</span></span>


</dt> <dd>

<span data-ttu-id="951a2-125">Permissão para fazer logon em uma sessão no servidor.</span><span class="sxs-lookup"><span data-stu-id="951a2-125">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="951a2-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ LOGOFF** (2)</span><span class="sxs-lookup"><span data-stu-id="951a2-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (2)</span></span>


</dt> <dd>

<span data-ttu-id="951a2-127">Permissão para fazer logoff de um usuário de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="951a2-127">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="951a2-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MSG** (7)</span><span class="sxs-lookup"><span data-stu-id="951a2-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (7)</span></span>


</dt> <dd>

<span data-ttu-id="951a2-129">Permissão para enviar uma mensagem para a sessão de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="951a2-129">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="951a2-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ CONECTAR** (8)</span><span class="sxs-lookup"><span data-stu-id="951a2-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (8)</span></span>


</dt> <dd>

<span data-ttu-id="951a2-131">Permissão para se conectar a outra sessão.</span><span class="sxs-lookup"><span data-stu-id="951a2-131">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="951a2-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ Desconectar** (9)</span><span class="sxs-lookup"><span data-stu-id="951a2-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (9)</span></span>


</dt> <dd>

<span data-ttu-id="951a2-133">Permissão para desconectar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="951a2-133">Permission to disconnect a session.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="951a2-134">*Êxito* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="951a2-134">*Success* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951a2-135">Especifica se o conjunto de permissões especificado pelo valor do parâmetro *PermissionMask* é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="951a2-135">Specifies if the permission set specified by the value of the *PermissionMask* parameter is allowed or denied.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="951a2-136"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="951a2-136"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="951a2-137">O conjunto de permissões especificado é permitido.</span><span class="sxs-lookup"><span data-stu-id="951a2-137">The specified permission set is allowed.</span></span>

</dd> <dt>

<span id="0"></span>

<span data-ttu-id="951a2-138"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="951a2-138"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="951a2-139">O conjunto de permissões especificado foi negado.</span><span class="sxs-lookup"><span data-stu-id="951a2-139">The specified permission set is denied.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="951a2-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="951a2-140">Return value</span></span>

<span data-ttu-id="951a2-141">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="951a2-141">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="951a2-142">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="951a2-142">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="951a2-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="951a2-143">Remarks</span></span>

<span data-ttu-id="951a2-144">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="951a2-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="951a2-145">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="951a2-145">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="951a2-146">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="951a2-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="951a2-147">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="951a2-147">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="951a2-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="951a2-148">Requirements</span></span>



| <span data-ttu-id="951a2-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="951a2-149">Requirement</span></span> | <span data-ttu-id="951a2-150">Valor</span><span class="sxs-lookup"><span data-stu-id="951a2-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="951a2-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="951a2-151">Minimum supported client</span></span><br/> | <span data-ttu-id="951a2-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="951a2-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="951a2-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="951a2-153">Minimum supported server</span></span><br/> | <span data-ttu-id="951a2-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="951a2-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="951a2-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="951a2-155">Namespace</span></span><br/>                | <span data-ttu-id="951a2-156">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="951a2-156">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="951a2-157">MOF</span><span class="sxs-lookup"><span data-stu-id="951a2-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="951a2-158"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="951a2-158"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="951a2-159">DLL</span><span class="sxs-lookup"><span data-stu-id="951a2-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="951a2-160"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="951a2-160"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="951a2-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="951a2-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="951a2-162">**\_TSAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="951a2-162">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

