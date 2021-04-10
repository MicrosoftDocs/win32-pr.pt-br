---
description: Representa as configurações específicas de replicação para uma máquina virtual.
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Classe Msvm_ReplicationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35bb97e531f8aca5f74801d55a71e5b3f2850c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170064"
---
# <a name="msvm_replicationsettingdata-class"></a><span data-ttu-id="03d93-103">\_Classe Msvm ReplicationSettingData</span><span class="sxs-lookup"><span data-stu-id="03d93-103">Msvm\_ReplicationSettingData class</span></span>

<span data-ttu-id="03d93-104">Representa as configurações específicas de replicação para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="03d93-104">Represents the replication-specific settings for a virtual machine.</span></span> <span data-ttu-id="03d93-105">O cliente passa uma instância dessa classe para [**Msvm \_ ReplicationService. CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) para criar uma relação de replicação.</span><span class="sxs-lookup"><span data-stu-id="03d93-105">The client passes an instance of this class to [**Msvm\_ReplicationService.CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) to create a replication relationship.</span></span> <span data-ttu-id="03d93-106">O cliente não pode alterar diretamente os valores de qualquer uma das propriedades para essa classe; Ele deve chamar o método [**Msvm \_ ReplicationService. ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) para alterar os valores.</span><span class="sxs-lookup"><span data-stu-id="03d93-106">The client can't directly change the values of any of the properties for this class; it must call the [**Msvm\_ReplicationService.ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) method to change the values.</span></span> <span data-ttu-id="03d93-107">Cada relação de replicação tem uma única instância de configurações.</span><span class="sxs-lookup"><span data-stu-id="03d93-107">Each replication relationship has a single instance of settings.</span></span>

<span data-ttu-id="03d93-108">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="03d93-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d93-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03d93-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a><span data-ttu-id="03d93-110">Membros</span><span class="sxs-lookup"><span data-stu-id="03d93-110">Members</span></span>

<span data-ttu-id="03d93-111">A classe **Msvm \_ ReplicationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="03d93-111">The **Msvm\_ReplicationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="03d93-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03d93-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03d93-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03d93-113">Properties</span></span>

<span data-ttu-id="03d93-114">A classe **Msvm \_ ReplicationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="03d93-114">The **Msvm\_ReplicationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03d93-115">**AdditionalSettings**</span><span class="sxs-lookup"><span data-stu-id="03d93-115">**AdditionalSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-118">Configurações de replicação adicionais que o provedor de ponto de extremidade pode usar.</span><span class="sxs-lookup"><span data-stu-id="03d93-118">Additional replication settings that the endpoint provider can use.</span></span>

<span data-ttu-id="03d93-119">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="03d93-119">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-120">**ApplicationConsistentSnapshotInterval**</span><span class="sxs-lookup"><span data-stu-id="03d93-120">**ApplicationConsistentSnapshotInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-121">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d93-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-123">O intervalo de tempo entre instantâneos consistentes do aplicativo, especificado em horas.</span><span class="sxs-lookup"><span data-stu-id="03d93-123">The time interval between application consistent snapshots, specified in hours.</span></span> <span data-ttu-id="03d93-124">Os valores válidos são de 1 hora a 12 horas.</span><span class="sxs-lookup"><span data-stu-id="03d93-124">Valid values are from 1 hour to 12 hours.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-125">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="03d93-125">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d93-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-128">Defina o modo de autenticação usado para se conectar ao servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="03d93-128">Define authentication mode used to connect to recover server.</span></span>

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="03d93-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Autenticação Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="03d93-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="03d93-130">Autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="03d93-130">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="03d93-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticação baseada em certificado** (2)</span><span class="sxs-lookup"><span data-stu-id="03d93-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="03d93-132">Autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="03d93-132">Certificate based authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="03d93-133">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="03d93-133">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-134">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d93-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-136">Não usado.</span><span class="sxs-lookup"><span data-stu-id="03d93-136">Not used.</span></span>

<span data-ttu-id="03d93-137">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d93-137">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d93-138">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="03d93-138">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d93-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-141">Não usado.</span><span class="sxs-lookup"><span data-stu-id="03d93-141">Not used.</span></span>

<span data-ttu-id="03d93-142">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d93-142">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d93-143">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="03d93-143">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d93-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-146">Não usado.</span><span class="sxs-lookup"><span data-stu-id="03d93-146">Not used.</span></span>

<span data-ttu-id="03d93-147">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d93-147">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d93-148">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="03d93-148">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-149">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03d93-149">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-151">O tempo de atraso antes que a máquina virtual seja iniciada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="03d93-151">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="03d93-152">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d93-152">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-153">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="03d93-153">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-154">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d93-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-156">Um número que indica a sequência relativa de ativação da máquina virtual quando o sistema host é iniciado.</span><span class="sxs-lookup"><span data-stu-id="03d93-156">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="03d93-157">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d93-157">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-158">**AutoResynchronizeEnabled**</span><span class="sxs-lookup"><span data-stu-id="03d93-158">**AutoResynchronizeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-159">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="03d93-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-161">Especifica se as operações de ressincronização são disparadas automaticamente quando ocorre um erro de replicação devido a falhas de energia e de hardware.</span><span class="sxs-lookup"><span data-stu-id="03d93-161">Specifies whether resynchronization operations are automatically triggered when a replication error occurs due to power and hardware failures.</span></span> <span data-ttu-id="03d93-162">As operações de ressincronização são disparadas apenas quando a falha ocorre entre os tempos especificados pelas propriedades **AutoResynchronizeIntervalStart** e **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="03d93-162">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="03d93-163">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="03d93-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-164">**AutoResynchronizeIntervalEnd**</span><span class="sxs-lookup"><span data-stu-id="03d93-164">**AutoResynchronizeIntervalEnd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-165">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03d93-165">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-167">Especifica a hora de término para operações de ressincronização automática a serem disparadas.</span><span class="sxs-lookup"><span data-stu-id="03d93-167">Specifies the end time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="03d93-168">Esse valor está na hora local.</span><span class="sxs-lookup"><span data-stu-id="03d93-168">This value is in local time.</span></span> <span data-ttu-id="03d93-169">O valor padrão é 06:00 (6:00 A.M.).</span><span class="sxs-lookup"><span data-stu-id="03d93-169">The default value is 06:00 (6:00 A.M.).</span></span>

<span data-ttu-id="03d93-170">As operações de ressincronização são disparadas apenas quando a falha ocorre entre os tempos especificados pelas propriedades **AutoResynchronizeIntervalStart** e **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="03d93-170">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="03d93-171">As operações de ressincronização também podem ser agendadas para que sejam disparadas durante o próximo intervalo.</span><span class="sxs-lookup"><span data-stu-id="03d93-171">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-172">**AutoResynchronizeIntervalStart**</span><span class="sxs-lookup"><span data-stu-id="03d93-172">**AutoResynchronizeIntervalStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-173">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03d93-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-175">Especifica a hora de início para operações de ressincronização automática a serem disparadas.</span><span class="sxs-lookup"><span data-stu-id="03d93-175">Specifies the start time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="03d93-176">Esse valor está na hora local.</span><span class="sxs-lookup"><span data-stu-id="03d93-176">This value is in local time.</span></span> <span data-ttu-id="03d93-177">O valor padrão é 18:30 (6:30 P.M.).</span><span class="sxs-lookup"><span data-stu-id="03d93-177">The default value is 18:30 (6:30 P.M.).</span></span>

<span data-ttu-id="03d93-178">As operações de ressincronização são disparadas apenas quando a falha ocorre entre os tempos especificados pelas propriedades **AutoResynchronizeIntervalStart** e **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="03d93-178">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="03d93-179">As operações de ressincronização também podem ser agendadas para que sejam disparadas durante o próximo intervalo.</span><span class="sxs-lookup"><span data-stu-id="03d93-179">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-180">**BypassProxyServer**</span><span class="sxs-lookup"><span data-stu-id="03d93-180">**BypassProxyServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-181">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="03d93-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-183">Especifica se o servidor proxy deve ser ignorado ao se conectar a um servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="03d93-183">Specifies whether the proxy server should be bypassed when connecting to a recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-184">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="03d93-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-187">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="03d93-187">A short description of the object.</span></span> <span data-ttu-id="03d93-188">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de replicação".</span><span class="sxs-lookup"><span data-stu-id="03d93-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Settings".</span></span>

</dd> <dt>

<span data-ttu-id="03d93-189">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="03d93-189">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d93-192">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="03d93-192">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="03d93-193">Impressão digital do certificado a ser usada quando a propriedade **AuthenticationType** for autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="03d93-193">Certificate thumbprint to use when the **AuthenticationType** property is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-194">**CompressionEnabled**</span><span class="sxs-lookup"><span data-stu-id="03d93-194">**CompressionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-195">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="03d93-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-197">Especifica se os dados de replicação serão compactados ao enviá-los para o servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="03d93-197">Specifies whether replication data will be compressed while sending it to the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-198">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="03d93-198">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-201">Não usado.</span><span class="sxs-lookup"><span data-stu-id="03d93-201">Not used.</span></span>

<span data-ttu-id="03d93-202">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d93-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d93-203">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="03d93-203">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-206">O caminho relativo e o nome de arquivo de um arquivo em que as informações sobre a configuração da máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="03d93-206">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="03d93-207">Esse caminho é relativo à propriedade **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="03d93-207">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="03d93-208">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d93-208">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-209">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="03d93-209">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-212">O identificador exclusivo da configuração da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="03d93-212">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="03d93-213">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d93-213">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-214">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="03d93-214">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-215">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03d93-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-217">A data e a hora em que as configurações da máquina virtual foram criadas.</span><span class="sxs-lookup"><span data-stu-id="03d93-217">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="03d93-218">Se esse objeto representar as configurações atuais para a máquina virtual, esse valor será a hora em que o sistema foi criado.</span><span class="sxs-lookup"><span data-stu-id="03d93-218">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="03d93-219">Se esse objeto representar as configurações de instantâneo para a máquina virtual, esse valor será a hora em que o instantâneo foi tirado.</span><span class="sxs-lookup"><span data-stu-id="03d93-219">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="03d93-220">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d93-220">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="03d93-221">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="03d93-221">This is a read-only property, but it can be changed by using the [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="03d93-222">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d93-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d93-223">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="03d93-223">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-224">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-226">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="03d93-226">A description of the object.</span></span> <span data-ttu-id="03d93-227">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "dados de configurações de replicação da máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="03d93-227">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="03d93-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="03d93-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-229">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-231">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="03d93-231">A display name for the object.</span></span> <span data-ttu-id="03d93-232">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e é definida como o nome de exibição para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="03d93-232">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is set to the display name for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-233">**EnableWriteOrderPreservationAcrossDisks**</span><span class="sxs-lookup"><span data-stu-id="03d93-233">**EnableWriteOrderPreservationAcrossDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-234">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="03d93-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d93-236">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor")</span><span class="sxs-lookup"><span data-stu-id="03d93-236">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="03d93-237">Especifica se todos os discos rígidos virtuais de replicação para a máquina virtual são replicados para o mesmo ponto no tempo.</span><span class="sxs-lookup"><span data-stu-id="03d93-237">Specifies whether all replicating virtual hard disks for the virtual machine are replicated to the same point in time.</span></span> <span data-ttu-id="03d93-238">Isso garante que a replicação obedeça a ordem de gravação dos aplicativos na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="03d93-238">This ensures replication honors the write-order of the applications in the virtual machine.</span></span>

<span data-ttu-id="03d93-239">**Windows 8.1:** A partir do Windows 8.1 e do Windows Server 2012 R2, essa propriedade é preterida e sempre é definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="03d93-239">**Windows 8.1:** Beginning with Windows 8.1 and Windows Server 2012 R2, this property is deprecated and always set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-240">**IncludedDisks**</span><span class="sxs-lookup"><span data-stu-id="03d93-240">**IncludedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-241">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="03d93-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d93-243">Qualificadores: **HyperVEmbeddedInstance** ("CIM \_ StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="03d93-243">Qualifiers: **HyperVEmbeddedInstance** ("CIM\_StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="03d93-244">A lista de VHDs (discos rígidos virtuais) conectados ao sistema que será replicado pelo mecanismo de replicação.</span><span class="sxs-lookup"><span data-stu-id="03d93-244">The list of virtual hard disks (VHDs) attached to the system that will be replicated by the replication engine.</span></span> <span data-ttu-id="03d93-245">Essa é uma matriz de cadeias de caracteres, cada uma contendo a **InstanceId** do [**\_ StorageAllocationSettingData MSVM**](msvm-storageallocationsettingdata.md) que representa o VHD.</span><span class="sxs-lookup"><span data-stu-id="03d93-245">This is an array of strings, each containing the **InstanceID** of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) that represents the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="03d93-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d93-249">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="03d93-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="03d93-250">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="03d93-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="03d93-251">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d93-251">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="03d93-252">Para o Windows 8, ele é sempre definido como "Microsoft:*Virtual Machine GUID* \\ HVR".</span><span class="sxs-lookup"><span data-stu-id="03d93-252">For Windows 8, it is always set to "Microsoft:*Virtual Machine GUID*\\HVR".</span></span> <span data-ttu-id="03d93-253">Por Windows 8.1, ele é definido como "Microsoft:*GUID da máquina virtual* \\ HVR \\<0/1>".</span><span class="sxs-lookup"><span data-stu-id="03d93-253">For Windows 8.1, it is set to "Microsoft:*Virtual Machine GUID*\\HVR\\<0/1>".</span></span> <span data-ttu-id="03d93-254">No Windows 8.1 valor, 0 indica primário e 1 indica replicação estendida.</span><span class="sxs-lookup"><span data-stu-id="03d93-254">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="03d93-255">Para obter mais informações sobre a replicação estendida, consulte [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="03d93-255">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="03d93-256">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="03d93-256">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-259">O caminho de um diretório em que as informações de log para a máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="03d93-259">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="03d93-260">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d93-260">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-261">**Observações**</span><span class="sxs-lookup"><span data-stu-id="03d93-261">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-262">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="03d93-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-264">Não usado e não pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="03d93-264">Not used and can't be set.</span></span>

<span data-ttu-id="03d93-265">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d93-265">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d93-266">**PrimaryConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="03d93-266">**PrimaryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-267">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d93-269">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="03d93-269">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03d93-270">O nome do ponto de conexão primário.</span><span class="sxs-lookup"><span data-stu-id="03d93-270">The name of the primary connection point.</span></span> <span data-ttu-id="03d93-271">No caso de um cluster primário, esse é o nome da extremidade do agente.</span><span class="sxs-lookup"><span data-stu-id="03d93-271">In the case of a primary cluster, this is the broker CAP name.</span></span> <span data-ttu-id="03d93-272">No caso de um servidor primário autônomo, esse é o nome do sistema host.</span><span class="sxs-lookup"><span data-stu-id="03d93-272">In the case of a standalone primary server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-273">**PrimaryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="03d93-273">**PrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-274">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d93-276">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="03d93-276">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03d93-277">O nome de domínio totalmente qualificado do sistema de host primário que está hospedando a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="03d93-277">The fully qualified domain name of the primary host system that is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-278">**RecoveryConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="03d93-278">**RecoveryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d93-281">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="03d93-281">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03d93-282">O nome do ponto de conexão de recuperação.</span><span class="sxs-lookup"><span data-stu-id="03d93-282">The name of the recovery connection point.</span></span> <span data-ttu-id="03d93-283">No caso de um cluster de recuperação, esse é o nome da extremidade do agente.</span><span class="sxs-lookup"><span data-stu-id="03d93-283">In the case of a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="03d93-284">No caso de um servidor de recuperação autônomo, esse é o nome do sistema de host.</span><span class="sxs-lookup"><span data-stu-id="03d93-284">In the case of a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-285">**Recuperação de**</span><span class="sxs-lookup"><span data-stu-id="03d93-285">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-288">O caminho completo de um arquivo em que as informações relacionadas à recuperação para a máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="03d93-288">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="03d93-289">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d93-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-290">**RecoveryHistory**</span><span class="sxs-lookup"><span data-stu-id="03d93-290">**RecoveryHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-291">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d93-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-293">O número máximo de instantâneos de recuperação que serão armazenados no servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="03d93-293">The maximum number of recovery snapshots that will be stored on the recovery server.</span></span> <span data-ttu-id="03d93-294">Os valores válidos são de 0 a 24.</span><span class="sxs-lookup"><span data-stu-id="03d93-294">Valid values are from 0 to 24.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-295">**RecoveryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="03d93-295">**RecoveryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-296">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d93-298">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="03d93-298">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="03d93-299">O nome de domínio totalmente qualificado do sistema host de recuperação que está hospedando a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="03d93-299">The fully qualified domain name of the recovery host system which is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-300">**RecoveryServerPortNumber**</span><span class="sxs-lookup"><span data-stu-id="03d93-300">**RecoveryServerPortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-301">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d93-301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-303">O número da porta do servidor de recuperação a ser usado ao fazer uma conexão segura para replicação.</span><span class="sxs-lookup"><span data-stu-id="03d93-303">The recovery server port number to use when making a secure connection for replication.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-304">**ReplicateHostKvpItems**</span><span class="sxs-lookup"><span data-stu-id="03d93-304">**ReplicateHostKvpItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-305">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="03d93-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-307">Especifica se [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)s somente de host devem ser replicadas da máquina virtual primária para a máquina virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="03d93-307">Specifies whether host-only [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)s should be replicated from the primary virtual machine to the recovery virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-308">**ReplicationInterval**</span><span class="sxs-lookup"><span data-stu-id="03d93-308">**ReplicationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-309">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03d93-309">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-311">Intervalo de replicação de uma relação de replicação em segundos.</span><span class="sxs-lookup"><span data-stu-id="03d93-311">Replication interval of a replication relationship in seconds.</span></span> <span data-ttu-id="03d93-312">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="03d93-312">Valid values are:</span></span>

<span data-ttu-id="03d93-313">30</span><span class="sxs-lookup"><span data-stu-id="03d93-313">30</span></span>

<span data-ttu-id="03d93-314">300</span><span class="sxs-lookup"><span data-stu-id="03d93-314">300</span></span>

<span data-ttu-id="03d93-315">900</span><span class="sxs-lookup"><span data-stu-id="03d93-315">900</span></span>

<span data-ttu-id="03d93-316">O valor padrão é 300 segundos.</span><span class="sxs-lookup"><span data-stu-id="03d93-316">Default value is 300 seconds.</span></span>

<span data-ttu-id="03d93-317">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="03d93-317">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-318">**Replicationprovider**</span><span class="sxs-lookup"><span data-stu-id="03d93-318">**ReplicationProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-321">O caminho para a instância da classe [**Msvm \_ replicationprovider**](msvm-replicationprovider.md) que identifica o ponto de extremidade do provedor de replicação.</span><span class="sxs-lookup"><span data-stu-id="03d93-321">The path to the instance of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class that identifies the replication provider endpoint.</span></span>

<span data-ttu-id="03d93-322">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="03d93-322">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-323">**RootCertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="03d93-323">**RootCertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03d93-326">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="03d93-326">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="03d93-327">A impressão digital do certificado raiz do certificado em uso quando a **AuthenticationType** é 2 (autorização baseada em certificado).</span><span class="sxs-lookup"><span data-stu-id="03d93-327">Root certificate thumbprint of the certificate in use when **AuthenticationType** is 2 (certificate based authorization).</span></span>

</dd> <dt>

<span data-ttu-id="03d93-328">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="03d93-328">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-329">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-331">O caminho de um diretório em que as informações sobre os instantâneos de máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="03d93-331">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="03d93-332">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d93-332">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-333">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="03d93-333">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-336">O caminho de um diretório em que informações sobre as informações relacionadas à suspensão da máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="03d93-336">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="03d93-337">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d93-337">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-338">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="03d93-338">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-339">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-341">O caminho de um diretório em que os arquivos de permuta para a máquina virtual são armazenados.</span><span class="sxs-lookup"><span data-stu-id="03d93-341">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="03d93-342">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="03d93-342">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="03d93-343">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="03d93-343">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-344">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-346">O nome do objeto [**de \_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de dados CIM ao qual esses dados de configuração pertencem.</span><span class="sxs-lookup"><span data-stu-id="03d93-346">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="03d93-347">Essa propriedade é uma substituição do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03d93-347">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="03d93-348">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="03d93-348">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03d93-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03d93-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03d93-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03d93-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03d93-351">Especifica o tipo de máquina virtual que os dados de configuração representam.</span><span class="sxs-lookup"><span data-stu-id="03d93-351">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="03d93-352">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e é sempre definida como "Microsoft: Hyper-V: Replica".</span><span class="sxs-lookup"><span data-stu-id="03d93-352">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to "Microsoft:Hyper-V:Replica".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03d93-353">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03d93-353">Requirements</span></span>



| <span data-ttu-id="03d93-354">Requisito</span><span class="sxs-lookup"><span data-stu-id="03d93-354">Requirement</span></span> | <span data-ttu-id="03d93-355">Valor</span><span class="sxs-lookup"><span data-stu-id="03d93-355">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d93-356">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03d93-356">Minimum supported client</span></span><br/> | <span data-ttu-id="03d93-357">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="03d93-357">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="03d93-358">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03d93-358">Minimum supported server</span></span><br/> | <span data-ttu-id="03d93-359">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="03d93-359">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03d93-360">Namespace</span><span class="sxs-lookup"><span data-stu-id="03d93-360">Namespace</span></span><br/>                | <span data-ttu-id="03d93-361">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="03d93-361">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="03d93-362">MOF</span><span class="sxs-lookup"><span data-stu-id="03d93-362">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03d93-363"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03d93-363"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03d93-364">DLL</span><span class="sxs-lookup"><span data-stu-id="03d93-364">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03d93-365"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03d93-365"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="03d93-366">Confira também</span><span class="sxs-lookup"><span data-stu-id="03d93-366">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d93-367">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="03d93-367">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

[<span data-ttu-id="03d93-368">**ModifyReplicationSettings**</span><span class="sxs-lookup"><span data-stu-id="03d93-368">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

