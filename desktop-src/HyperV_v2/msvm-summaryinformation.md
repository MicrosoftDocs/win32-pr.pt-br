---
description: Usado nos métodos GetSummaryInformation e GetDefinitionFileSummaryInformation da \_ classe Msvm VirtualSystemManagementService para recuperar rapidamente informações comuns relacionadas a uma máquina virtual ou instantâneo.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Classe Msvm_SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 817d025551ae10002b008a181edd8a7dfd2ec68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747563"
---
# <a name="msvm_summaryinformation-class"></a><span data-ttu-id="a1c82-103">\_Classe Msvm SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="a1c82-103">Msvm\_SummaryInformation class</span></span>

<span data-ttu-id="a1c82-104">Usado nos métodos [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) e [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para recuperar rapidamente informações comuns relacionadas a uma máquina virtual ou instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a1c82-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) and [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) methods in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual machine or snapshot.</span></span>

<span data-ttu-id="a1c82-105">A sintaxe a seguir é simplificada formato MOF código (MOF).</span><span class="sxs-lookup"><span data-stu-id="a1c82-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1c82-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1c82-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="a1c82-107">Membros</span><span class="sxs-lookup"><span data-stu-id="a1c82-107">Members</span></span>

<span data-ttu-id="a1c82-108">A classe **Msvm \_ SummaryInformation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a1c82-108">The **Msvm\_SummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="a1c82-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1c82-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1c82-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1c82-110">Properties</span></span>

<span data-ttu-id="a1c82-111">A classe **Msvm \_ SummaryInformation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a1c82-111">The **Msvm\_SummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1c82-112">**AllocatedGPU**</span><span class="sxs-lookup"><span data-stu-id="a1c82-112">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-115">O identificador da GPU (unidade de processamento gráfico) física alocada a esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-115">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="a1c82-116">Essa propriedade só se aplica a máquinas virtuais que usam o RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="a1c82-116">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-117">**ApplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="a1c82-117">**ApplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-118">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-120">O status de integridade do aplicativo atual para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-120">The current application health status for the virtual machine.</span></span> <span data-ttu-id="a1c82-121">Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-121">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a1c82-122">**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="a1c82-122">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

<span data-ttu-id="a1c82-123">**Aplicativo crítico** (32782)</span><span class="sxs-lookup"><span data-stu-id="a1c82-123">**Application Critical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a1c82-124">**Desabilitado** (32896)</span><span class="sxs-lookup"><span data-stu-id="a1c82-124">**Disabled** (32896)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1c82-125">**AsynchronousTasks**</span><span class="sxs-lookup"><span data-stu-id="a1c82-125">**AsynchronousTasks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-126">Tipo de dados: matriz de **\_ ConcreteJob CIM**</span><span class="sxs-lookup"><span data-stu-id="a1c82-126">Data type: **CIM\_ConcreteJob** array</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-128">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="a1c82-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-129">Uma matriz de instâncias do [**Msvm \_ ConcreteJob**](msvm-concretejob.md) que representam as operações assíncronas relacionadas à máquina virtual em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="a1c82-129">An array of [**Msvm\_ConcreteJob**](msvm-concretejob.md) instances that represent any asynchronous operations related to the virtual machine that are currently executing.</span></span> <span data-ttu-id="a1c82-130">Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-130">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-131">**AvailableMemoryBuffer**</span><span class="sxs-lookup"><span data-stu-id="a1c82-131">**AvailableMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a1c82-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-134">A porcentagem de buffer de memória disponível para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-134">The percentage of available memory buffer for the virtual machine.</span></span> <span data-ttu-id="a1c82-135">Quando a memória dinâmica está habilitada para uma máquina virtual, essa propriedade representa a taxa de buffer de memória disponível para o buffer de memória ideal para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-135">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory buffer to the ideal memory buffer for the virtual machine.</span></span> <span data-ttu-id="a1c82-136">O tamanho de buffer de memória ideal é configurado usando a propriedade **TargetMemoryBuffer** da classe [**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="a1c82-136">The ideal memory buffer size is configured by using the **TargetMemoryBuffer** property of the [**Msvm\_MemorySettingData**](msvm-memorysettingdata.md) class.</span></span>

<span data-ttu-id="a1c82-137">Essa propriedade não é válida para instâncias da classe **Msvm \_ SummaryInformation** que representam máquinas virtuais para as quais a memória dinâmica não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a1c82-137">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="a1c82-138">Essa propriedade não é válida para instâncias da classe **Msvm \_ SummaryInformation** que representa um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-138">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-139">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="a1c82-139">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-140">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a1c82-140">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-142">A hora em que a máquina virtual ou o instantâneo foi criado.</span><span class="sxs-lookup"><span data-stu-id="a1c82-142">The time at which the virtual machine or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a1c82-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-146">O nome de exibição para a máquina virtual ou o instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a1c82-146">The display name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-147">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a1c82-147">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-148">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-150">O estado atual da máquina virtual ou do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a1c82-150">The current state of the virtual machine or snapshot.</span></span> <span data-ttu-id="a1c82-151">Consulte a propriedade **enabledstate** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a1c82-151">See the **EnabledState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-152">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="a1c82-152">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-153">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-155">Indica se as conexões de modo avançado são permitidas pelo host e, se forem permitidas, se estão disponíveis para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-155">Indicates whether enhanced mode connections are allowed by the host, and if allowed, whether they are available to the virtual machine.</span></span>

<span data-ttu-id="a1c82-156">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="a1c82-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="a1c82-157">**Permitido e disponível** (2)</span><span class="sxs-lookup"><span data-stu-id="a1c82-157">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="a1c82-158">**Não permitido** (3)</span><span class="sxs-lookup"><span data-stu-id="a1c82-158">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="a1c82-159">**Permitido, mas não disponível** (6)</span><span class="sxs-lookup"><span data-stu-id="a1c82-159">**Allowed but not available** (6 )</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1c82-160">**GuestOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="a1c82-160">**GuestOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-163">O nome do sistema operacional convidado, se disponível.</span><span class="sxs-lookup"><span data-stu-id="a1c82-163">The name of the guest operating system, if available.</span></span> <span data-ttu-id="a1c82-164">Se essas informações não estiverem disponíveis, o valor dessa propriedade será **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a1c82-164">If this information is not available, the value of this property is **Null**.</span></span> <span data-ttu-id="a1c82-165">Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-165">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-166">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a1c82-166">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-169">O estado de integridade atual para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-169">The current health state for the virtual machine.</span></span> <span data-ttu-id="a1c82-170">Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-170">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-171">**Pulsação**</span><span class="sxs-lookup"><span data-stu-id="a1c82-171">**Heartbeat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-172">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-174">O status de pulsação atual para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-174">The current heartbeat status for the virtual machine.</span></span> <span data-ttu-id="a1c82-175">Para obter mais informações, consulte a documentação da propriedade [**StatusDescriptions**](msvm-heartbeatcomponent.md) da classe **Msvm \_ HeartbeatComponent** .</span><span class="sxs-lookup"><span data-stu-id="a1c82-175">For more information, see the documentation for the [**StatusDescriptions**](msvm-heartbeatcomponent.md) property of the **Msvm\_HeartbeatComponent** class.</span></span> <span data-ttu-id="a1c82-176">Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-176">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dl> <dt>

<span data-ttu-id="a1c82-177"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="a1c82-177"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (6)</span><span class="sxs-lookup"><span data-stu-id="a1c82-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sem contato** (12)</span><span class="sxs-lookup"><span data-stu-id="a1c82-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (13)</span><span class="sxs-lookup"><span data-stu-id="a1c82-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a1c82-181">**HostComputerSystemName**</span><span class="sxs-lookup"><span data-stu-id="a1c82-181">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-184">O nome do computador que hospeda esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-184">The name of the computer hosting this virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="a1c82-185">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a1c82-185">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="a1c82-186">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a1c82-186">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-189">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ managedelement. InstanceId"), [**chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a1c82-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-190">InstanceID é uma propriedade opcional que pode ser usada para identificar de forma opaca e exclusiva uma instância dessa classe dentro do escopo do namespace de instanciação.</span><span class="sxs-lookup"><span data-stu-id="a1c82-190">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="a1c82-191">Várias subclasses dessa classe podem substituir essa propriedade para torná-la necessária ou uma chave.</span><span class="sxs-lookup"><span data-stu-id="a1c82-191">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="a1c82-192">Essas subclasses também podem modificar os algoritmos preferenciais para garantir a exclusividade definida abaixo.</span><span class="sxs-lookup"><span data-stu-id="a1c82-192">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="a1c82-193">Para garantir a exclusividade no NameSpace, o valor de InstanceID deve ser construído usando o seguinte algoritmo "preferencial":</span><span class="sxs-lookup"><span data-stu-id="a1c82-193">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="a1c82-194"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="a1c82-194"><OrgID>:<LocalID></span></span>

<span data-ttu-id="a1c82-195">Onde <OrgID> e <LocalID> são separados por dois-pontos (:), e onde <OrgID> devem incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que está criando ou definindo a InstanceId ou que é uma ID registrada atribuída à entidade de negócios por uma autoridade global reconhecida.</span><span class="sxs-lookup"><span data-stu-id="a1c82-195">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="a1c82-196">(Esse requisito é semelhante ao <Schema Name> \_ <Class Name> estrutura de nomes de classe de esquema.) Além disso, para garantir a exclusividade, <OrgID> não deve conter dois-pontos (:).</span><span class="sxs-lookup"><span data-stu-id="a1c82-196">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="a1c82-197">Ao usar esse algoritmo, os primeiros dois-pontos a serem exibidos em InstanceID devem aparecer entre <OrgID> e <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="a1c82-197">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="a1c82-198"><LocalID> é escolhido pela entidade de negócios e não deve ser reutilizado para identificar elementos subjacentes (reais) diferentes.</span><span class="sxs-lookup"><span data-stu-id="a1c82-198"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="a1c82-199">Se não for nulo e o algoritmo "preferencial" acima não for usado, a entidade de definição deverá garantir que a InstanceID resultante não seja reutilizada em quaisquer InstanceIDs produzidas por este ou outros provedores para o NameSpace dessa instância.</span><span class="sxs-lookup"><span data-stu-id="a1c82-199">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="a1c82-200">Se não estiver definido como nulo para instâncias definidas por DMTF, o algoritmo "preferencial" deverá ser usado com o <OrgID> conjunto como CIM.</span><span class="sxs-lookup"><span data-stu-id="a1c82-200">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

> [!Note]  
> <span data-ttu-id="a1c82-201">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a1c82-201">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="a1c82-202">**IntegrationServicesVersionState**</span><span class="sxs-lookup"><span data-stu-id="a1c82-202">**IntegrationServicesVersionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-203">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-205">Indica se os serviços de integração instalados na máquina virtual estão atualizados.</span><span class="sxs-lookup"><span data-stu-id="a1c82-205">Indicates whether the integration services installed in the virtual machine are up to date.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a1c82-206">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a1c82-206">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

<span data-ttu-id="a1c82-207">**UpToDate** (1)</span><span class="sxs-lookup"><span data-stu-id="a1c82-207">**UpToDate** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

<span data-ttu-id="a1c82-208">**Incompatibilidade** (2)</span><span class="sxs-lookup"><span data-stu-id="a1c82-208">**Mismatch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1c82-209">**MemoryAvailable**</span><span class="sxs-lookup"><span data-stu-id="a1c82-209">**MemoryAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-210">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a1c82-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-212">A porcentagem da memória atual disponível para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-212">The percentage of the current memory available to the virtual machine.</span></span> <span data-ttu-id="a1c82-213">Quando a memória dinâmica está habilitada para uma máquina virtual, essa propriedade representa a taxa de memória disponível da máquina virtual para a memória física total atribuída à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-213">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory of the virtual machine to the total physical memory assigned to the virtual machine.</span></span> <span data-ttu-id="a1c82-214">Quando uma máquina virtual não tem memória disponível, essa propriedade será negativa e conterá a taxa de memória necessária para a máquina virtual para a memória física total atribuída à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-214">When a virtual machine has no available memory, this property will be negative, and it will contain the ratio of memory needed for the virtual machine to the total physical memory assigned to the virtual machine.</span></span>

<span data-ttu-id="a1c82-215">Essa propriedade não é válida para instâncias da classe **Msvm \_ SummaryInformation** que representam máquinas virtuais para as quais a memória dinâmica não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a1c82-215">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="a1c82-216">Essa propriedade não é válida para instâncias da classe **Msvm \_ SummaryInformation** que representa um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-216">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-217">**MemorySpansPhysicalNumaNodes**</span><span class="sxs-lookup"><span data-stu-id="a1c82-217">**MemorySpansPhysicalNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-218">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a1c82-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-220">Indica se a memória de um ou mais nós NUMA (acesso virtual não uniforme de memória) da máquina virtual abrange vários nós NUMA físicos do sistema de computador host.</span><span class="sxs-lookup"><span data-stu-id="a1c82-220">Indicates whether the memory of the one or more of the virtual nonuniform memory access (NUMA) nodes of the virtual machine spans multiple physical NUMA nodes of the hosting computer system.</span></span> <span data-ttu-id="a1c82-221">Contém **true** se a memória abranger vários nós numa físicos ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a1c82-221">Contains **True** if the memory spans multiple physical NUMA nodes or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-222">**MemoryUsage**</span><span class="sxs-lookup"><span data-stu-id="a1c82-222">**MemoryUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-223">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1c82-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-225">O uso de memória atual, em megabytes, da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-225">The current memory usage, in megabytes, of the virtual machine.</span></span> <span data-ttu-id="a1c82-226">Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-226">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-227">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a1c82-227">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-230">O nome exclusivo para a máquina virtual ou o instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a1c82-230">The unique name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-231">**Observações**</span><span class="sxs-lookup"><span data-stu-id="a1c82-231">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-234">As notas associadas à máquina virtual ou ao instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a1c82-234">The notes associated with the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-235">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="a1c82-235">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-236">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-238">O número total de processadores virtuais alocados para a máquina virtual ou instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a1c82-238">The total number of virtual processors allocated to the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-239">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a1c82-239">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-240">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-242">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="a1c82-242">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-243">Os status operacionais atuais da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-243">The current operational statuses of the virtual machine.</span></span> <span data-ttu-id="a1c82-244">Consulte a propriedade **OperationalStatus** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a1c82-244">See the **OperationalStatus** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-245">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a1c82-245">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-248">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1.</span><span class="sxs-lookup"><span data-stu-id="a1c82-248">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1.</span></span> <span data-ttu-id="a1c82-249">Essa propriedade será definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="a1c82-249">This property will be set to **Null** when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-250">**ProcessorLoad**</span><span class="sxs-lookup"><span data-stu-id="a1c82-250">**ProcessorLoad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-251">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-253">O uso atual do processador da máquina virtual, em porcentagem.</span><span class="sxs-lookup"><span data-stu-id="a1c82-253">The current processor usage of the virtual machine, in percentage.</span></span> <span data-ttu-id="a1c82-254">Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-254">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-255">**ProcessorLoadHistory**</span><span class="sxs-lookup"><span data-stu-id="a1c82-255">**ProcessorLoadHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-256">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-258">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="a1c82-258">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-259">Uma matriz dos 100 exemplos anteriores do uso do processador, em porcentagem, para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-259">An array of the previous 100 samples of the processor usage, in percentage, for the virtual machine.</span></span> <span data-ttu-id="a1c82-260">Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-260">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-261">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="a1c82-261">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-262">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-264">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm \_ SummaryInformation**.**ReplicationHealthEx**")</span><span class="sxs-lookup"><span data-stu-id="a1c82-264">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationHealthEx**")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-265">A integridade da replicação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-265">The replication health for the virtual machine.</span></span> <span data-ttu-id="a1c82-266">Consulte a propriedade **ReplicationHealth** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a1c82-266">See the **ReplicationHealth** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="a1c82-267">Esta propriedade foi preterida a partir de Windows 8.1; em vez disso, use o **ReplicationHealthEx**.</span><span class="sxs-lookup"><span data-stu-id="a1c82-267">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationHealthEx**.</span></span>

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a1c82-268">**Não aplicável** (0)</span><span class="sxs-lookup"><span data-stu-id="a1c82-268">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="a1c82-269">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="a1c82-269">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a1c82-270">**Aviso** (2)</span><span class="sxs-lookup"><span data-stu-id="a1c82-270">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a1c82-271">**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="a1c82-271">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1c82-272">**ReplicationHealthEx**</span><span class="sxs-lookup"><span data-stu-id="a1c82-272">**ReplicationHealthEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-273">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-275">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="a1c82-275">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-276">A matriz de valores de integridade de replicação para os vários relacionamentos de replicação da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-276">The array of replication health values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="a1c82-277">Consulte a propriedade **ReplicationHealth** da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a1c82-277">See the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a1c82-278">**Não aplicável** (0)</span><span class="sxs-lookup"><span data-stu-id="a1c82-278">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="a1c82-279">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="a1c82-279">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a1c82-280">**Aviso** (2)</span><span class="sxs-lookup"><span data-stu-id="a1c82-280">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a1c82-281">**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="a1c82-281">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1c82-282">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="a1c82-282">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-283">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-285">O tipo de replicação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-285">The replication type for the virtual machine.</span></span> <span data-ttu-id="a1c82-286">Consulte a propriedade **replicationmode** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a1c82-286">See the **ReplicationMode** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="a1c82-287">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="a1c82-287">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="a1c82-288">**Primário** (1)</span><span class="sxs-lookup"><span data-stu-id="a1c82-288">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="a1c82-289">**Réplica** (2)</span><span class="sxs-lookup"><span data-stu-id="a1c82-289">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="a1c82-290">**Réplica de teste** (3)</span><span class="sxs-lookup"><span data-stu-id="a1c82-290">**Test Replica** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="a1c82-291">**Réplica estendida** (4)</span><span class="sxs-lookup"><span data-stu-id="a1c82-291">**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1c82-292">**ReplicationProviderId**</span><span class="sxs-lookup"><span data-stu-id="a1c82-292">**ReplicationProviderId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-293">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-295">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="a1c82-295">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-296">Para a máquina virtual de réplica primária ou estendida, esta é a ID de provedor de replicação primária.</span><span class="sxs-lookup"><span data-stu-id="a1c82-296">For the primary or extended replica virtual machine, this is the primary replication provider ID.</span></span> <span data-ttu-id="a1c82-297">Para uma máquina virtual de réplica e se a replicação estendida estiver habilitada, essa será a ID do provedor para a relação estendida.</span><span class="sxs-lookup"><span data-stu-id="a1c82-297">For a replica virtual machine and if extended replication is enabled, this is the provider ID for extended relationship.</span></span>

<span data-ttu-id="a1c82-298">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="a1c82-298">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-299">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="a1c82-299">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-300">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-302">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm \_ SummaryInformation**.**ReplicationStateEx**")</span><span class="sxs-lookup"><span data-stu-id="a1c82-302">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationStateEx**")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-303">O estado de replicação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-303">The replication state for the virtual machine.</span></span> <span data-ttu-id="a1c82-304">Consulte a propriedade **replicationstate** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a1c82-304">See the **ReplicationState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="a1c82-305">Esta propriedade foi preterida a partir de Windows 8.1; em vez disso, use o **ReplicationStateEx**.</span><span class="sxs-lookup"><span data-stu-id="a1c82-305">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationStateEx**.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a1c82-306">**Desabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="a1c82-306">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="a1c82-307">**Pronto para replicação** (1)</span><span class="sxs-lookup"><span data-stu-id="a1c82-307">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="a1c82-308">**Aguardando para concluir a replicação inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="a1c82-308">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="a1c82-309">**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="a1c82-309">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="a1c82-310">**Replicação sincronizada concluída** (4)</span><span class="sxs-lookup"><span data-stu-id="a1c82-310">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="a1c82-311">**Recuperado** (5)</span><span class="sxs-lookup"><span data-stu-id="a1c82-311">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="a1c82-312">**Confirmado** (6)</span><span class="sxs-lookup"><span data-stu-id="a1c82-312">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="a1c82-313">**Suspenso** (7)</span><span class="sxs-lookup"><span data-stu-id="a1c82-313">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a1c82-314">**Crítico** (8)</span><span class="sxs-lookup"><span data-stu-id="a1c82-314">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="a1c82-315">**Aguardando para iniciar a ressincronização** (9)</span><span class="sxs-lookup"><span data-stu-id="a1c82-315">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="a1c82-316">**Ressincronização** (10)</span><span class="sxs-lookup"><span data-stu-id="a1c82-316">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="a1c82-317">**Ressincronização suspensa** (11)</span><span class="sxs-lookup"><span data-stu-id="a1c82-317">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="a1c82-318">**Failover em andamento** (12)</span><span class="sxs-lookup"><span data-stu-id="a1c82-318">**Failover in progress** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a1c82-319">**ReplicationStateEx**</span><span class="sxs-lookup"><span data-stu-id="a1c82-319">**ReplicationStateEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-320">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-322">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="a1c82-322">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-323">A matriz de valores de estado de replicação para os vários relacionamentos de replicação da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-323">The array of replication state values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="a1c82-324">Consulte a propriedade **replicationstate** da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a1c82-324">See the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a1c82-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="a1c82-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="a1c82-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Pronto para replicação** (1)</span><span class="sxs-lookup"><span data-stu-id="a1c82-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="a1c82-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Aguardando para concluir a replicação inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="a1c82-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="a1c82-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="a1c82-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="a1c82-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicação sincronizada concluída** (4)</span><span class="sxs-lookup"><span data-stu-id="a1c82-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="a1c82-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recuperado** (5)</span><span class="sxs-lookup"><span data-stu-id="a1c82-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="a1c82-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Confirmado** (6)</span><span class="sxs-lookup"><span data-stu-id="a1c82-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="a1c82-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspenso** (7)</span><span class="sxs-lookup"><span data-stu-id="a1c82-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a1c82-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (8)</span><span class="sxs-lookup"><span data-stu-id="a1c82-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="a1c82-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Aguardando para iniciar a ressincronização** (9)</span><span class="sxs-lookup"><span data-stu-id="a1c82-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="a1c82-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Ressincronização** (10)</span><span class="sxs-lookup"><span data-stu-id="a1c82-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="a1c82-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Ressincronização suspensa** (11)</span><span class="sxs-lookup"><span data-stu-id="a1c82-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="a1c82-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover em andamento** (12)</span><span class="sxs-lookup"><span data-stu-id="a1c82-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="a1c82-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback em andamento** (13)</span><span class="sxs-lookup"><span data-stu-id="a1c82-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="a1c82-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback concluído** (14)</span><span class="sxs-lookup"><span data-stu-id="a1c82-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="a1c82-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Atualização de disco em andamento** (15)</span><span class="sxs-lookup"><span data-stu-id="a1c82-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a1c82-341">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1c82-341">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="a1c82-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Atualização de disco crítica** (16)</span><span class="sxs-lookup"><span data-stu-id="a1c82-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a1c82-343">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1c82-343">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a1c82-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (17)</span><span class="sxs-lookup"><span data-stu-id="a1c82-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a1c82-345">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1c82-345">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="a1c82-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Replicação de redefinição em andamento** (18)</span><span class="sxs-lookup"><span data-stu-id="a1c82-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a1c82-347">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1c82-347">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="a1c82-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Preparado para replicação de sincronização** (19)</span><span class="sxs-lookup"><span data-stu-id="a1c82-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a1c82-349">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1c82-349">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="a1c82-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Preparado para replicação inversa de grupo** (20)</span><span class="sxs-lookup"><span data-stu-id="a1c82-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a1c82-351">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1c82-351">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="a1c82-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill em andamento** (21)</span><span class="sxs-lookup"><span data-stu-id="a1c82-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="a1c82-353">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1c82-353">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a1c82-354">**Blindado**</span><span class="sxs-lookup"><span data-stu-id="a1c82-354">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-355">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a1c82-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-357">Indica se a blindagem está configurada para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-357">Indicates whether or not shielding is configured for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="a1c82-358">Adicionado no Windows 10, versão 1703 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1c82-358">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="a1c82-359">**Instantâneos**</span><span class="sxs-lookup"><span data-stu-id="a1c82-359">**Snapshots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-360">Tipo de dados: matriz de **\_ VirtualSystemSettingData CIM**</span><span class="sxs-lookup"><span data-stu-id="a1c82-360">Data type: **CIM\_VirtualSystemSettingData** array</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-362">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="a1c82-362">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-363">Uma matriz de instâncias [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representam os instantâneos para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-363">An array of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances that represent the snapshots for the virtual machine.</span></span> <span data-ttu-id="a1c82-364">Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-364">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-365">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a1c82-365">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-366">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-368">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="a1c82-368">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-369">Cadeias de caracteres que descrevem os valores correspondentes da matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a1c82-369">Strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="a1c82-370">Isso corresponde à propriedade **StatusDescriptions** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="a1c82-370">This corresponds to the **StatusDescriptions** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-371">**SwapFilesInUse**</span><span class="sxs-lookup"><span data-stu-id="a1c82-371">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-372">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a1c82-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-374">Indica se a paginação de segundo nível está ativa.</span><span class="sxs-lookup"><span data-stu-id="a1c82-374">Indicates whether second level paging is active.</span></span> <span data-ttu-id="a1c82-375">Contém **true** se a paginação de segundo nível estiver ativa ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a1c82-375">Contains **True** if second level paging is active or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-376">**TestReplicaSystem**</span><span class="sxs-lookup"><span data-stu-id="a1c82-376">**TestReplicaSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-377">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="a1c82-377">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-379">Referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual de réplica de teste para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-379">Reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the test replica virtual machine for the virtual machine.</span></span> <span data-ttu-id="a1c82-380">Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-380">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-381">**ThumbnailImage**</span><span class="sxs-lookup"><span data-stu-id="a1c82-381">**ThumbnailImage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-382">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="a1c82-382">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-384">Qualificadores: **octetstring**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImageWidth**","**Msvm \_ SummaryInformation**.**ThumbnailImageHeight**")</span><span class="sxs-lookup"><span data-stu-id="a1c82-384">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImageWidth**", "**Msvm\_SummaryInformation**.**ThumbnailImageHeight**")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-385">Uma matriz que contém uma imagem pequena e de tamanho de miniatura da área de trabalho para a máquina virtual ou o instantâneo no formato RGB565.</span><span class="sxs-lookup"><span data-stu-id="a1c82-385">An array that contains a small, thumbnail-sized image of the desktop for the virtual machine or snapshot in RGB565 format.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-386">**ThumbnailImageHeight**</span><span class="sxs-lookup"><span data-stu-id="a1c82-386">**ThumbnailImageHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-387">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-389">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImage**")</span><span class="sxs-lookup"><span data-stu-id="a1c82-389">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-390">A altura em pixels da imagem na propriedade ThumbnailImage.</span><span class="sxs-lookup"><span data-stu-id="a1c82-390">The height in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="a1c82-391">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a1c82-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="a1c82-392">**ThumbnailImageWidth**</span><span class="sxs-lookup"><span data-stu-id="a1c82-392">**ThumbnailImageWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-393">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a1c82-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-395">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImage**")</span><span class="sxs-lookup"><span data-stu-id="a1c82-395">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-396">A largura em pixels da imagem na propriedade ThumbnailImage.</span><span class="sxs-lookup"><span data-stu-id="a1c82-396">The width in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="a1c82-397">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a1c82-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="a1c82-398">**Atividade**</span><span class="sxs-lookup"><span data-stu-id="a1c82-398">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-399">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a1c82-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-401">A quantidade de tempo desde a última inicialização da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-401">The amount of time since the virtual machine was last booted.</span></span> <span data-ttu-id="a1c82-402">Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-402">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-403">**Versão**</span><span class="sxs-lookup"><span data-stu-id="a1c82-403">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-404">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-406">A versão do sistema virtual em um formato de "Major. Minor", por exemplo, "2,0".</span><span class="sxs-lookup"><span data-stu-id="a1c82-406">The version of the virtual system in a format of "major.minor", for example "2.0".</span></span>

> [!Note]  
> <span data-ttu-id="a1c82-407">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a1c82-407">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="a1c82-408">**VirtualSwitchNames**</span><span class="sxs-lookup"><span data-stu-id="a1c82-408">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-409">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-411">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="a1c82-411">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-412">Cadeias de caracteres que especificam os nomes amigáveis dos comutadores virtuais aos quais a máquina virtual está conectada.</span><span class="sxs-lookup"><span data-stu-id="a1c82-412">Strings that specify the friendly names of the virtual switches the virtual machine is connected to.</span></span>

<span data-ttu-id="a1c82-413">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="a1c82-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="a1c82-414">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="a1c82-414">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1c82-415">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a1c82-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1c82-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a1c82-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1c82-417">O subtipo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="a1c82-417">The subtype of the virtual system.</span></span>

<span data-ttu-id="a1c82-418">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="a1c82-418">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="a1c82-419">**Microsoft: Hyper-V: subtipo: 1** ()</span><span class="sxs-lookup"><span data-stu-id="a1c82-419">**Microsoft:Hyper-V:SubType:1** ()</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="a1c82-420">**Microsoft: Hyper-V: subtipo: 2** ()</span><span class="sxs-lookup"><span data-stu-id="a1c82-420">**Microsoft:Hyper-V:SubType:2** ()</span></span>


<span data-ttu-id="a1c82-421"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a1c82-421"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a1c82-422">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1c82-422">Remarks</span></span>

<span data-ttu-id="a1c82-423">O acesso à classe **Msvm \_ SummaryInformation** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="a1c82-423">Access to the **Msvm\_SummaryInformation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a1c82-424">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a1c82-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1c82-425">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1c82-425">Requirements</span></span>



| <span data-ttu-id="a1c82-426">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1c82-426">Requirement</span></span> | <span data-ttu-id="a1c82-427">Valor</span><span class="sxs-lookup"><span data-stu-id="a1c82-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c82-428">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1c82-428">Minimum supported client</span></span><br/> | <span data-ttu-id="a1c82-429">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a1c82-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a1c82-430">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1c82-430">Minimum supported server</span></span><br/> | <span data-ttu-id="a1c82-431">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a1c82-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a1c82-432">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1c82-432">Namespace</span></span><br/>                | <span data-ttu-id="a1c82-433">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a1c82-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a1c82-434">MOF</span><span class="sxs-lookup"><span data-stu-id="a1c82-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1c82-435"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1c82-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1c82-436">DLL</span><span class="sxs-lookup"><span data-stu-id="a1c82-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1c82-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a1c82-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a1c82-438">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1c82-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c82-439">**Msvm \_ SummaryInformationBase**</span><span class="sxs-lookup"><span data-stu-id="a1c82-439">**Msvm\_SummaryInformationBase**</span></span>](msvm-summaryinformationbase.md)
</dt> <dt>

[<span data-ttu-id="a1c82-440">Classes de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="a1c82-440">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

