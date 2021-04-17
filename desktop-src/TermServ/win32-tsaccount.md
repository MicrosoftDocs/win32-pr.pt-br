---
title: Classe Win32_TSAccount
description: Permite a exclusão de uma conta que existe no terminal do Win32 \_ e a modificação de permissões existentes.
ms.assetid: fd4d8a0f-685b-4619-84f1-faefbabd04ba
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSAccount Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSAccount classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSAccount
- Win32_TSAccount.Caption
- Win32_TSAccount.Description
- Win32_TSAccount.InstallDate
- Win32_TSAccount.Name
- Win32_TSAccount.Status
- Win32_TSAccount.TerminalName
- Win32_TSAccount.AccountName
- Win32_TSAccount.AuditFail
- Win32_TSAccount.AuditSuccess
- Win32_TSAccount.PermissionsAllowed
- Win32_TSAccount.PermissionsDenied
- Win32_TSAccount.SID
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fed32943cf89728081e2443dfffe2e3762298d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782872"
---
# <a name="win32_tsaccount-class"></a><span data-ttu-id="e056e-105">\_Classe Win32 TSAccount</span><span class="sxs-lookup"><span data-stu-id="e056e-105">Win32\_TSAccount class</span></span>

<span data-ttu-id="e056e-106">A classe WMI **\_ TSAccount do Win32** permite a exclusão de uma conta que existe [**no \_ terminal do Win32**](win32-terminal.md) e a modificação de permissões existentes.</span><span class="sxs-lookup"><span data-stu-id="e056e-106">The **Win32\_TSAccount** WMI class allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

<span data-ttu-id="e056e-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="e056e-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="e056e-108">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="e056e-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="e056e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e056e-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSACCOUNT_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSAccount : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   AccountName;
  uint32   AuditFail;
  uint32   AuditSuccess;
  uint32   PermissionsAllowed;
  uint32   PermissionsDenied;
  string   SID;
};
```

## <a name="members"></a><span data-ttu-id="e056e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e056e-110">Members</span></span>

<span data-ttu-id="e056e-111">A classe **Win32 \_ TSAccount** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e056e-111">The **Win32\_TSAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="e056e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e056e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e056e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e056e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e056e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="e056e-114">Methods</span></span>

<span data-ttu-id="e056e-115">A classe **Win32 \_ TSAccount** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e056e-115">The **Win32\_TSAccount** class has these methods.</span></span>



| <span data-ttu-id="e056e-116">Método</span><span class="sxs-lookup"><span data-stu-id="e056e-116">Method</span></span>                                                                   | <span data-ttu-id="e056e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e056e-117">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e056e-118">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="e056e-118">**Delete**</span></span>](win32-tsaccount-delete.md)                                 | <span data-ttu-id="e056e-119">Exclui o usuário, grupo ou conta de computador especificado.</span><span class="sxs-lookup"><span data-stu-id="e056e-119">Deletes the specified user, group, or computer account.</span></span><br/>                           |
| [<span data-ttu-id="e056e-120">**ModifyAuditPermissions**</span><span class="sxs-lookup"><span data-stu-id="e056e-120">**ModifyAuditPermissions**</span></span>](win32-tsaccount-modifyauditpermissions.md) | <span data-ttu-id="e056e-121">Altera a granularidade do conjunto de permissões de auditoria da conta especificada.</span><span class="sxs-lookup"><span data-stu-id="e056e-121">Changes the granularity of the set of audit permissions of the specified account.</span></span><br/> |
| [<span data-ttu-id="e056e-122">**ModifyPermissions**</span><span class="sxs-lookup"><span data-stu-id="e056e-122">**ModifyPermissions**</span></span>](win32-tsaccount-modifypermissions.md)           | <span data-ttu-id="e056e-123">Define um conjunto de permissões mais granular para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="e056e-123">Sets a more granular permission set to the specified account.</span></span><br/>                     |



 

### <a name="properties"></a><span data-ttu-id="e056e-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e056e-124">Properties</span></span>

<span data-ttu-id="e056e-125">A classe **Win32 \_ TSAccount** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e056e-125">The **Win32\_TSAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e056e-126">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="e056e-126">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e056e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e056e-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e056e-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e056e-130">O nome atual da conta.</span><span class="sxs-lookup"><span data-stu-id="e056e-130">The current name of the account.</span></span> <span data-ttu-id="e056e-131">O nome de domínio está incluído.</span><span class="sxs-lookup"><span data-stu-id="e056e-131">The domain name is included.</span></span>

</dd> <dt>

<span data-ttu-id="e056e-132">**AuditFail**</span><span class="sxs-lookup"><span data-stu-id="e056e-132">**AuditFail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e056e-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e056e-135">Especifica as [permissões de serviços de host da sessão da área de trabalho remota](terminal-services-permissions.md) que são auditadas para uma condição de falha.</span><span class="sxs-lookup"><span data-stu-id="e056e-135">Specifies the [Remote Desktop Session Host Services Permissions](terminal-services-permissions.md) that are audited for a failure condition.</span></span> <span data-ttu-id="e056e-136">O valor dessa propriedade é um bitmask, que pode ser definido como um ou mais valores da propriedade **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="e056e-136">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="e056e-137">**WINSTATION \_ CONSULTA = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="e056e-137">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="e056e-138">**WINSTATION \_ DEFINIR = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="e056e-138">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="e056e-139">**WINSTATION \_ LOGOFF = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="e056e-139">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="e056e-140">**WINSTATION \_ \| Direitos padrão \_ virtuais \_ obrigatórios = 0xF008** (3)</span><span class="sxs-lookup"><span data-stu-id="e056e-140">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="e056e-141">**WINSTATION \_ SOMBRA = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="e056e-141">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="e056e-142">**WINSTATION \_ LOGON = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="e056e-142">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="e056e-143">**WINSTATION \_ MSG = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="e056e-143">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="e056e-144">**WINSTATION \_ CONNECT = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="e056e-144">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="e056e-145">**WINSTATION \_ DISCONNECT = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="e056e-145">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e056e-146">**AuditSuccess**</span><span class="sxs-lookup"><span data-stu-id="e056e-146">**AuditSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-147">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e056e-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e056e-149">Especifica as Host da Sessão RD permissões específicas do servidor que são auditadas para uma condição de êxito.</span><span class="sxs-lookup"><span data-stu-id="e056e-149">Specifies the RD Session Host server-specific permissions that are audited for a success condition.</span></span> <span data-ttu-id="e056e-150">O valor dessa propriedade é um bitmask, que pode ser definido como um ou mais valores da propriedade **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="e056e-150">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="e056e-151">**WINSTATION \_ CONSULTA = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="e056e-151">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="e056e-152">**WINSTATION \_ DEFINIR = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="e056e-152">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_logoff_0x4winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_LOGOFF_0X4WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="e056e-153">**WINSTATION \_ LOGOFF = 0x4WINSTATION \_ virtual \| Standard \_ Rights \_ Required = 0xF008** (2)</span><span class="sxs-lookup"><span data-stu-id="e056e-153">**WINSTATION\_LOGOFF=0x4WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="e056e-154">**WINSTATION \_ SOMBRA = 0x10** (3)</span><span class="sxs-lookup"><span data-stu-id="e056e-154">**WINSTATION\_SHADOW=0x10** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="e056e-155">**WINSTATION \_ LOGON = 0x20** (4)</span><span class="sxs-lookup"><span data-stu-id="e056e-155">**WINSTATION\_LOGON=0x20** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="e056e-156">**WINSTATION \_ MSG = 0x80** (5)</span><span class="sxs-lookup"><span data-stu-id="e056e-156">**WINSTATION\_MSG=0x80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="e056e-157">**WINSTATION \_ CONNECT = 0x100** (6)</span><span class="sxs-lookup"><span data-stu-id="e056e-157">**WINSTATION\_CONNECT=0x100** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="e056e-158">**WINSTATION \_ DISCONNECT = 0x200** (7)</span><span class="sxs-lookup"><span data-stu-id="e056e-158">**WINSTATION\_DISCONNECT=0x200** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e056e-159">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e056e-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e056e-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e056e-162">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e056e-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e056e-163">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="e056e-163">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="e056e-164">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e056e-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e056e-165">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e056e-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e056e-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e056e-168">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e056e-168">Description of the object.</span></span>

<span data-ttu-id="e056e-169">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e056e-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e056e-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e056e-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-171">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e056e-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e056e-173">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="e056e-173">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="e056e-174">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="e056e-174">The date the object was installed.</span></span> <span data-ttu-id="e056e-175">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="e056e-175">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e056e-176">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e056e-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e056e-177">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e056e-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e056e-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e056e-180">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="e056e-180">The name of the object.</span></span>

<span data-ttu-id="e056e-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e056e-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e056e-182">**PermissionsAllowed**</span><span class="sxs-lookup"><span data-stu-id="e056e-182">**PermissionsAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-183">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e056e-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e056e-185">Especifica as [permissões de serviços de área de trabalho remota](terminal-services-permissions.md) permitidas para a conta.</span><span class="sxs-lookup"><span data-stu-id="e056e-185">Specifies the [Remote Desktop Services Permissions](terminal-services-permissions.md) allowed for the account.</span></span> <span data-ttu-id="e056e-186">O valor dessa propriedade é um bitmask, que pode ser definido como um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e056e-186">The value of this property is a bitmask, which can be set to one or more of the following values.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="e056e-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION \_ CONSULTA = 0x1** (1)</span><span class="sxs-lookup"><span data-stu-id="e056e-187"><span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>**WINSTATION\_QUERY=0x1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e056e-188">Permissão para consultar informações sobre uma sessão.</span><span class="sxs-lookup"><span data-stu-id="e056e-188">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="e056e-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ DEFINIR** (2)</span><span class="sxs-lookup"><span data-stu-id="e056e-189"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e056e-190">Permissão para modificar os parâmetros de conexão.</span><span class="sxs-lookup"><span data-stu-id="e056e-190">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="e056e-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ REDEFINIR** (64)</span><span class="sxs-lookup"><span data-stu-id="e056e-191"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (64)</span></span>


</dt> <dd>

<span data-ttu-id="e056e-192">Permissão para redefinir ou encerrar uma sessão ou conexão.</span><span class="sxs-lookup"><span data-stu-id="e056e-192">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="e056e-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ \| Direitos padrão \_ virtuais \_ necessários** (983048)</span><span class="sxs-lookup"><span data-stu-id="e056e-193"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (983048)</span></span>


</dt> <dd>

<span data-ttu-id="e056e-194">Permissão para usar canais virtuais.</span><span class="sxs-lookup"><span data-stu-id="e056e-194">Permission to use virtual channels.</span></span> <span data-ttu-id="e056e-195">Os canais virtuais fornecem acesso de um programa de servidor a dispositivos cliente.</span><span class="sxs-lookup"><span data-stu-id="e056e-195">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="e056e-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ SOMBRA** (16)</span><span class="sxs-lookup"><span data-stu-id="e056e-196"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (16)</span></span>


</dt> <dd>

<span data-ttu-id="e056e-197">Permissão para sombrear ou controlar remotamente a sessão de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="e056e-197">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="e056e-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ LOGON** (32)</span><span class="sxs-lookup"><span data-stu-id="e056e-198"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (32)</span></span>


</dt> <dd>

<span data-ttu-id="e056e-199">Permissão para fazer logon em uma sessão no servidor.</span><span class="sxs-lookup"><span data-stu-id="e056e-199">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="e056e-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ LOGOFF** (4)</span><span class="sxs-lookup"><span data-stu-id="e056e-200"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e056e-201">Permissão para fazer logoff de um usuário de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="e056e-201">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="e056e-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MSG** (128)</span><span class="sxs-lookup"><span data-stu-id="e056e-202"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (128)</span></span>


</dt> <dd>

<span data-ttu-id="e056e-203">Permissão para enviar uma mensagem para a sessão de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="e056e-203">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="e056e-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ CONECTAR** (256)</span><span class="sxs-lookup"><span data-stu-id="e056e-204"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (256)</span></span>


</dt> <dd>

<span data-ttu-id="e056e-205">Permissão para se conectar a outra sessão.</span><span class="sxs-lookup"><span data-stu-id="e056e-205">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="e056e-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ Desconectar** (512)</span><span class="sxs-lookup"><span data-stu-id="e056e-206"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (512)</span></span>


</dt> <dd>

<span data-ttu-id="e056e-207">Permissão para desconectar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="e056e-207">Permission to disconnect a session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e056e-208">**PermissionsDenied**</span><span class="sxs-lookup"><span data-stu-id="e056e-208">**PermissionsDenied**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-209">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e056e-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e056e-211">Especifica o Host da Sessão RD permissões específicas do servidor não permitidas para a conta.</span><span class="sxs-lookup"><span data-stu-id="e056e-211">Specifies the RD Session Host server-specific permissions disallowed for the account.</span></span> <span data-ttu-id="e056e-212">O valor dessa propriedade é um bitmask, que pode ser definido como um ou mais valores da propriedade **PermissionsAllowed** .</span><span class="sxs-lookup"><span data-stu-id="e056e-212">The value of this property is a bitmask, which can be set to one or more of the values of the **PermissionsAllowed** property.</span></span>

<dt>

<span id="WINSTATION_QUERY_0x1"></span><span id="winstation_query_0x1"></span><span id="WINSTATION_QUERY_0X1"></span>

<span data-ttu-id="e056e-213">**WINSTATION \_ CONSULTA = 0x1** (0)</span><span class="sxs-lookup"><span data-stu-id="e056e-213">**WINSTATION\_QUERY=0x1** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SET_0x2"></span><span id="winstation_set_0x2"></span><span id="WINSTATION_SET_0X2"></span>

<span data-ttu-id="e056e-214">**WINSTATION \_ DEFINIR = 0x2** (1)</span><span class="sxs-lookup"><span data-stu-id="e056e-214">**WINSTATION\_SET=0x2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGOFF_0x4"></span><span id="winstation_logoff_0x4"></span><span id="WINSTATION_LOGOFF_0X4"></span>

<span data-ttu-id="e056e-215">**WINSTATION \_ LOGOFF = 0x4** (2)</span><span class="sxs-lookup"><span data-stu-id="e056e-215">**WINSTATION\_LOGOFF=0x4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0xF008"></span><span id="winstation_virtual___standard_rights_required___0xf008"></span><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED___0XF008"></span>

<span data-ttu-id="e056e-216">**WINSTATION \_ \| Direitos padrão \_ virtuais \_ obrigatórios = 0xF008** (3)</span><span class="sxs-lookup"><span data-stu-id="e056e-216">**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED = 0xF008** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_SHADOW_0x10"></span><span id="winstation_shadow_0x10"></span><span id="WINSTATION_SHADOW_0X10"></span>

<span data-ttu-id="e056e-217">**WINSTATION \_ SOMBRA = 0x10** (4)</span><span class="sxs-lookup"><span data-stu-id="e056e-217">**WINSTATION\_SHADOW=0x10** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_LOGON_0x20"></span><span id="winstation_logon_0x20"></span><span id="WINSTATION_LOGON_0X20"></span>

<span data-ttu-id="e056e-218">**WINSTATION \_ LOGON = 0x20** (5)</span><span class="sxs-lookup"><span data-stu-id="e056e-218">**WINSTATION\_LOGON=0x20** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_MSG_0x80"></span><span id="winstation_msg_0x80"></span><span id="WINSTATION_MSG_0X80"></span>

<span data-ttu-id="e056e-219">**WINSTATION \_ MSG = 0x80** (6)</span><span class="sxs-lookup"><span data-stu-id="e056e-219">**WINSTATION\_MSG=0x80** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_CONNECT_0x100"></span><span id="winstation_connect_0x100"></span><span id="WINSTATION_CONNECT_0X100"></span>

<span data-ttu-id="e056e-220">**WINSTATION \_ CONNECT = 0x100** (7)</span><span class="sxs-lookup"><span data-stu-id="e056e-220">**WINSTATION\_CONNECT=0x100** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="WINSTATION_DISCONNECT_0x200"></span><span id="winstation_disconnect_0x200"></span><span id="WINSTATION_DISCONNECT_0X200"></span>

<span data-ttu-id="e056e-221">**WINSTATION \_ DISCONNECT = 0x200** (8)</span><span class="sxs-lookup"><span data-stu-id="e056e-221">**WINSTATION\_DISCONNECT=0x200** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e056e-222">**SID**</span><span class="sxs-lookup"><span data-stu-id="e056e-222">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e056e-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e056e-225">Especifica os [identificadores de segurança](/windows/desktop/SecAuthZ/security-identifiers) da conta.</span><span class="sxs-lookup"><span data-stu-id="e056e-225">Specifies the [Security Identifiers](/windows/desktop/SecAuthZ/security-identifiers) of the account.</span></span>

</dd> <dt>

<span data-ttu-id="e056e-226">**Status**</span><span class="sxs-lookup"><span data-stu-id="e056e-226">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e056e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e056e-229">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="e056e-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="e056e-230">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e056e-230">Current status of the object.</span></span> <span data-ttu-id="e056e-231">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="e056e-231">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e056e-232">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="e056e-232">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e056e-233">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="e056e-233">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e056e-234">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="e056e-234">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e056e-235">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="e056e-235">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e056e-236">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e056e-236">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="e056e-237">("OK")</span><span class="sxs-lookup"><span data-stu-id="e056e-237">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e056e-238">("Erro")</span><span class="sxs-lookup"><span data-stu-id="e056e-238">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e056e-239">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="e056e-239">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e056e-240">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e056e-240">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e056e-241">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e056e-241">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e056e-242">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="e056e-242">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e056e-243">("Parando")</span><span class="sxs-lookup"><span data-stu-id="e056e-243">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e056e-244">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="e056e-244">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e056e-245">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="e056e-245">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e056e-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e056e-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e056e-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e056e-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e056e-248">O nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="e056e-248">The name of the terminal.</span></span>

<span data-ttu-id="e056e-249">Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="e056e-249">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e056e-250">Comentários</span><span class="sxs-lookup"><span data-stu-id="e056e-250">Remarks</span></span>

<span data-ttu-id="e056e-251">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="e056e-251">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="e056e-252">Para chamadas C/C++, isso seria um nível de autenticação de **privacidade do PCT no nível do RPC \_ C \_ Authn \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="e056e-252">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="e056e-253">Para chamadas de script e de Visual Basic, isso seria um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="e056e-253">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="e056e-254">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="e056e-254">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="e056e-255">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e056e-255">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e056e-256">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e056e-256">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e056e-257">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e056e-257">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e056e-258">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e056e-258">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e056e-259">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e056e-259">Requirements</span></span>



| <span data-ttu-id="e056e-260">Requisito</span><span class="sxs-lookup"><span data-stu-id="e056e-260">Requirement</span></span> | <span data-ttu-id="e056e-261">Valor</span><span class="sxs-lookup"><span data-stu-id="e056e-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e056e-262">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e056e-262">Minimum supported client</span></span><br/> | <span data-ttu-id="e056e-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e056e-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e056e-264">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e056e-264">Minimum supported server</span></span><br/> | <span data-ttu-id="e056e-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e056e-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e056e-266">Namespace</span><span class="sxs-lookup"><span data-stu-id="e056e-266">Namespace</span></span><br/>                | <span data-ttu-id="e056e-267">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="e056e-267">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e056e-268">MOF</span><span class="sxs-lookup"><span data-stu-id="e056e-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e056e-269"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e056e-269"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e056e-270">DLL</span><span class="sxs-lookup"><span data-stu-id="e056e-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e056e-271"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e056e-271"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e056e-272">Confira também</span><span class="sxs-lookup"><span data-stu-id="e056e-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e056e-273">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="e056e-273">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

