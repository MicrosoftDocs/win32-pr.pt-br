---
description: Representa as configurações do serviço de migração de sistema virtual em um host.
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Classe Msvm_VirtualSystemMigrationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c8685e468d60983408c52a985169c61be91f632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754526"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a><span data-ttu-id="4254f-103">\_Classe Msvm VirtualSystemMigrationServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="4254f-103">Msvm\_VirtualSystemMigrationServiceSettingData class</span></span>

<span data-ttu-id="4254f-104">Representa as configurações do serviço de migração de sistema virtual em um host.</span><span class="sxs-lookup"><span data-stu-id="4254f-104">Represents the settings for the virtual system migration service on a host.</span></span> <span data-ttu-id="4254f-105">As propriedades desta classe não podem ser modificadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="4254f-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="4254f-106">O cliente deve chamar o método **Msvm \_ VirtualSystemMigrationService. ModifyServiceSettings** para modificar qualquer uma dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4254f-106">The client must call the **Msvm\_VirtualSystemMigrationService.ModifyServiceSettings** method to modify any of these properties.</span></span>

<span data-ttu-id="4254f-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4254f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4254f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4254f-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a><span data-ttu-id="4254f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4254f-109">Members</span></span>

<span data-ttu-id="4254f-110">A classe **Msvm \_ VirtualSystemMigrationServiceSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4254f-110">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4254f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4254f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4254f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4254f-112">Properties</span></span>

<span data-ttu-id="4254f-113">A classe **Msvm \_ VirtualSystemMigrationServiceSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4254f-113">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4254f-114">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="4254f-114">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4254f-115">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4254f-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4254f-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4254f-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4254f-117">Especifica o mecanismo de autenticação usado para conexões de rede de migração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="4254f-117">Specifies the authentication mechanism used for virtual system migration network connections.</span></span> <span data-ttu-id="4254f-118">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) da classe [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4254f-118">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

<span data-ttu-id="4254f-119">**CredSSP** (0)</span><span class="sxs-lookup"><span data-stu-id="4254f-119">**CredSSP** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

<span data-ttu-id="4254f-120">**Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="4254f-120">**Kerberos** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4254f-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="4254f-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4254f-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4254f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4254f-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4254f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4254f-124">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="4254f-124">A short description of the object.</span></span> <span data-ttu-id="4254f-125">Essa propriedade é herdada da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="4254f-125">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="4254f-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4254f-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4254f-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4254f-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4254f-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4254f-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4254f-129">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="4254f-129">A description of the object.</span></span> <span data-ttu-id="4254f-130">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4254f-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4254f-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4254f-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4254f-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4254f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4254f-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4254f-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4254f-134">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="4254f-134">A display name for the object.</span></span> <span data-ttu-id="4254f-135">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4254f-135">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4254f-136">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="4254f-136">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4254f-137">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4254f-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4254f-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4254f-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4254f-139">Indica se a compactação do tráfego de migração ao vivo está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="4254f-139">Indicates whether compression of live migration traffic is enabled or disabled.</span></span> <span data-ttu-id="4254f-140">Verdadeiro indica habilitado.</span><span class="sxs-lookup"><span data-stu-id="4254f-140">True indicates enabled.</span></span>

<span data-ttu-id="4254f-141">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4254f-141">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="4254f-142">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="4254f-142">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="4254f-143">**EnableSmbTransport**</span><span class="sxs-lookup"><span data-stu-id="4254f-143">**EnableSmbTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4254f-144">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4254f-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4254f-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4254f-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4254f-146">Indica se o uso de SMB como um tipo de transporte para transferir o estado da VM entre os hosts do Hyper-V durante a migração do sistema virtual está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4254f-146">Indicates whether use of SMB as a transport type for transferring VM state between the Hyper-V hosts during virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="4254f-147">**Verdadeiro** indica habilitado.</span><span class="sxs-lookup"><span data-stu-id="4254f-147">**True** indicates enabled.</span></span> <span data-ttu-id="4254f-148">Um desempenho maior será obtido se as NICs RDMA estiverem configuradas para transporte SMB durante a migração dinâmica de VM.</span><span class="sxs-lookup"><span data-stu-id="4254f-148">A higher performance is achieved if RDMA NICs are configured for SMB transport during VM live migration.</span></span> <span data-ttu-id="4254f-149">Se o valor de **EnableSmbTransport** for true, o valor de **EnableCompression** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="4254f-149">If **EnableSmbTransport** value is true, the value of **EnableCompression** is ignored.</span></span>

<span data-ttu-id="4254f-150">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4254f-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="4254f-151">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="4254f-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="4254f-152">**EnableVirtualSystemMigration**</span><span class="sxs-lookup"><span data-stu-id="4254f-152">**EnableVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4254f-153">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="4254f-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4254f-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4254f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4254f-155">Especifica se a migração do sistema virtual está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="4254f-155">Specifies whether virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="4254f-156">A migração de armazenamento está sempre habilitada.</span><span class="sxs-lookup"><span data-stu-id="4254f-156">Storage migration is always enabled.</span></span> <span data-ttu-id="4254f-157">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) da classe [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4254f-157">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4254f-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4254f-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4254f-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4254f-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4254f-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4254f-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4254f-161">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="4254f-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4254f-162">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="4254f-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4254f-163">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4254f-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4254f-164">**MaximumActiveStorageMigration**</span><span class="sxs-lookup"><span data-stu-id="4254f-164">**MaximumActiveStorageMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4254f-165">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4254f-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4254f-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4254f-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4254f-167">Especifica o número máximo de migrações de armazenamento ativas permitidas.</span><span class="sxs-lookup"><span data-stu-id="4254f-167">Specifies the maximum number of active storage migrations allowed.</span></span> <span data-ttu-id="4254f-168">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) da classe [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4254f-168">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4254f-169">**MaximumActiveVirtualSystemMigration**</span><span class="sxs-lookup"><span data-stu-id="4254f-169">**MaximumActiveVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4254f-170">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4254f-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4254f-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4254f-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4254f-172">Especifica o número máximo de migrações de sistema virtual ativas permitidas.</span><span class="sxs-lookup"><span data-stu-id="4254f-172">Specifies the maximum number of active virtual system migrations allowed.</span></span> <span data-ttu-id="4254f-173">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) da classe [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4254f-173">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4254f-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4254f-174">Requirements</span></span>



| <span data-ttu-id="4254f-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="4254f-175">Requirement</span></span> | <span data-ttu-id="4254f-176">Valor</span><span class="sxs-lookup"><span data-stu-id="4254f-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4254f-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4254f-177">Minimum supported client</span></span><br/> | <span data-ttu-id="4254f-178">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4254f-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4254f-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4254f-179">Minimum supported server</span></span><br/> | <span data-ttu-id="4254f-180">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4254f-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4254f-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="4254f-181">Namespace</span></span><br/>                | <span data-ttu-id="4254f-182">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4254f-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4254f-183">MOF</span><span class="sxs-lookup"><span data-stu-id="4254f-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4254f-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4254f-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4254f-185">DLL</span><span class="sxs-lookup"><span data-stu-id="4254f-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4254f-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4254f-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4254f-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="4254f-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4254f-188">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="4254f-188">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="4254f-189">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="4254f-189">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

