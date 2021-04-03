---
description: Representa as configurações do serviço de replicação em um host de recuperação. As propriedades desta classe não podem ser modificadas diretamente. O cliente deve chamar o \_ método Msvm ReplicationService. ModifyServiceSettings para modificar qualquer uma dessas propriedades.
ms.assetid: a0c0b45a-3578-412a-910e-cd4b3ff0e262
title: Classe Msvm_ReplicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationServiceSettingData
- Msvm_ReplicationServiceSettingData.InstanceID
- Msvm_ReplicationServiceSettingData.Caption
- Msvm_ReplicationServiceSettingData.Description
- Msvm_ReplicationServiceSettingData.ElementName
- Msvm_ReplicationServiceSettingData.RecoveryServerEnabled
- Msvm_ReplicationServiceSettingData.AllowedAuthenticationType
- Msvm_ReplicationServiceSettingData.CertificateThumbPrint
- Msvm_ReplicationServiceSettingData.HttpsPort
- Msvm_ReplicationServiceSettingData.HttpPort
- Msvm_ReplicationServiceSettingData.MonitoringStartTime
- Msvm_ReplicationServiceSettingData.MonitoringInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e2886529ab74fed52ec0c6077bfa3d9222fca55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828890"
---
# <a name="msvm_replicationservicesettingdata-class"></a><span data-ttu-id="b5419-105">\_Classe Msvm ReplicationServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="b5419-105">Msvm\_ReplicationServiceSettingData class</span></span>

<span data-ttu-id="b5419-106">Representa as configurações do serviço de replicação em um host de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b5419-106">Represents the settings for the replication service on a recovery host.</span></span> <span data-ttu-id="b5419-107">As propriedades desta classe não podem ser modificadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="b5419-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="b5419-108">O cliente deve chamar o método [**Msvm \_ ReplicationService. ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) para modificar qualquer uma dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b5419-108">The client must call the [**Msvm\_ReplicationService.ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="b5419-109">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b5419-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5419-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5419-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Replication Service Settings";
  string   Description = "Virtual Machine Replication Service Settings Data";
  string   ElementName = "Replication Service Settings";
  boolean  RecoveryServerEnabled = False;
  uint16   AllowedAuthenticationType = 0;
  string   CertificateThumbPrint;
  uint16   HttpsPort = 443;
  uint16   HttpPort = 80;
  datetime MonitoringStartTime;
  uint32   MonitoringInterval = 43200;
};
```

## <a name="members"></a><span data-ttu-id="b5419-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b5419-111">Members</span></span>

<span data-ttu-id="b5419-112">A classe **Msvm \_ ReplicationServiceSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b5419-112">The **Msvm\_ReplicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b5419-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b5419-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5419-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b5419-114">Properties</span></span>

<span data-ttu-id="b5419-115">A classe **Msvm \_ ReplicationServiceSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b5419-115">The **Msvm\_ReplicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5419-116">**AllowedAuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="b5419-116">**AllowedAuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5419-117">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5419-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5419-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5419-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5419-119">Defina modos de autenticação permitidos para conexão com o servidor de host de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b5419-119">Define authentication modes allowed for connecting to recovery host server.</span></span>

<dt>

<span data-ttu-id="b5419-120">0</span><span class="sxs-lookup"><span data-stu-id="b5419-120">0</span></span>
</dt> <dd>

<span data-ttu-id="b5419-121">Não definido.</span><span class="sxs-lookup"><span data-stu-id="b5419-121">Not defined.</span></span>

</dd> <dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="b5419-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Autenticação Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="b5419-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b5419-123">Autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b5419-123">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="b5419-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticação baseada em certificado** (2)</span><span class="sxs-lookup"><span data-stu-id="b5419-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b5419-125">Autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="b5419-125">Certificate based authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="b5419-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Autenticação baseada em certificado e autenticação Kerberos** (3)</span><span class="sxs-lookup"><span data-stu-id="b5419-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Certificate based authentication and kerberos authentication** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b5419-127">Autenticação baseada em certificado e autenticação integrada.</span><span class="sxs-lookup"><span data-stu-id="b5419-127">Both certificate based authentication and integrated authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b5419-128">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b5419-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5419-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5419-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5419-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5419-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5419-131">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="b5419-131">A short description of the object.</span></span> <span data-ttu-id="b5419-132">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações do serviço de replicação".</span><span class="sxs-lookup"><span data-stu-id="b5419-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="b5419-133">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="b5419-133">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5419-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5419-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5419-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5419-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5419-136">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="b5419-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="b5419-137">Impressão digital do certificado a ser usada quando a **AuthenticationType** for autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="b5419-137">Certificate thumbprint to use when **AuthenticationType** is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="b5419-138">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b5419-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5419-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5419-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5419-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5419-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5419-141">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="b5419-141">A description of the object.</span></span> <span data-ttu-id="b5419-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "dados de configurações de replicação da máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="b5419-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="b5419-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b5419-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5419-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5419-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5419-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5419-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5419-146">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="b5419-146">A display name for the object.</span></span> <span data-ttu-id="b5419-147">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações do serviço de replicação".</span><span class="sxs-lookup"><span data-stu-id="b5419-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="b5419-148">**HttpPort**</span><span class="sxs-lookup"><span data-stu-id="b5419-148">**HttpPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5419-149">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5419-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5419-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5419-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5419-151">Número da porta do servidor de recuperação a ser usado ao aceitar uma conexão não segura para replicação.</span><span class="sxs-lookup"><span data-stu-id="b5419-151">Recovery server port number to use when accepting a nonsecure connection for replication.</span></span> <span data-ttu-id="b5419-152">O valor padrão é 80.</span><span class="sxs-lookup"><span data-stu-id="b5419-152">The default value is 80.</span></span>

</dd> <dt>

<span data-ttu-id="b5419-153">**HttpsPort**</span><span class="sxs-lookup"><span data-stu-id="b5419-153">**HttpsPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5419-154">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b5419-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b5419-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5419-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5419-156">Número da porta do servidor de recuperação a ser usado ao aceitar conexão segura para replicação.</span><span class="sxs-lookup"><span data-stu-id="b5419-156">Recovery server port number to use when accepting secure connection for replication.</span></span> <span data-ttu-id="b5419-157">O valor padrão é 443.</span><span class="sxs-lookup"><span data-stu-id="b5419-157">The default value is 443.</span></span>

</dd> <dt>

<span data-ttu-id="b5419-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b5419-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5419-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5419-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5419-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5419-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5419-161">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="b5419-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b5419-162">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="b5419-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b5419-163">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5419-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b5419-164">**MonitoringInterval**</span><span class="sxs-lookup"><span data-stu-id="b5419-164">**MonitoringInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5419-165">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5419-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5419-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5419-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5419-167">O intervalo, em segundos, no qual as estatísticas de replicação devem ser redefinidas.</span><span class="sxs-lookup"><span data-stu-id="b5419-167">The interval, in seconds, at which replication statistics should be reset.</span></span> <span data-ttu-id="b5419-168">O intervalo padrão é de 12 horas (43200 segundos).</span><span class="sxs-lookup"><span data-stu-id="b5419-168">The default interval is 12 hours (43200 seconds).</span></span> <span data-ttu-id="b5419-169">O valor mínimo válido é de 60 minutos (3600 segundos) e o valor máximo válido é de 7 dias (604800 segundos).</span><span class="sxs-lookup"><span data-stu-id="b5419-169">The minimum valid value is 60 minutes (3600 seconds), and the maximum valid value is 7 days (604800 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="b5419-170">**MonitoringStartTime**</span><span class="sxs-lookup"><span data-stu-id="b5419-170">**MonitoringStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5419-171">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b5419-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b5419-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5419-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5419-173">A hora de início para o monitoramento de replicação, em UTC.</span><span class="sxs-lookup"><span data-stu-id="b5419-173">The start time for replication monitoring, in UTC.</span></span> <span data-ttu-id="b5419-174">O valor padrão é 9:00 A.M., hora local, representado em UTC.</span><span class="sxs-lookup"><span data-stu-id="b5419-174">The default value is 9:00 A.M., local time, represented in UTC.</span></span> <span data-ttu-id="b5419-175">Os elementos de data do objeto **DateTime** devem ser zero.</span><span class="sxs-lookup"><span data-stu-id="b5419-175">The date elements of the **datetime** object must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b5419-176">**RecoveryServerEnabled**</span><span class="sxs-lookup"><span data-stu-id="b5419-176">**RecoveryServerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5419-177">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5419-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5419-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5419-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5419-179">Especifica se o host Hyper-V está habilitado como um servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b5419-179">Specifies whether the Hyper-V host is enabled as a recovery server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5419-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5419-180">Requirements</span></span>



| <span data-ttu-id="b5419-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5419-181">Requirement</span></span> | <span data-ttu-id="b5419-182">Valor</span><span class="sxs-lookup"><span data-stu-id="b5419-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5419-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5419-183">Minimum supported client</span></span><br/> | <span data-ttu-id="b5419-184">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b5419-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b5419-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5419-185">Minimum supported server</span></span><br/> | <span data-ttu-id="b5419-186">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b5419-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5419-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5419-187">Namespace</span></span><br/>                | <span data-ttu-id="b5419-188">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b5419-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b5419-189">MOF</span><span class="sxs-lookup"><span data-stu-id="b5419-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5419-190"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5419-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5419-191">DLL</span><span class="sxs-lookup"><span data-stu-id="b5419-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5419-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5419-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5419-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5419-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5419-194">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="b5419-194">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="b5419-195">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="b5419-195">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)
</dt> </dl>

 

