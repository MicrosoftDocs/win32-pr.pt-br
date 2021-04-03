---
description: Descreve a GPU (unidade de processamento gráfico) 3-D física.
ms.assetid: 24e3d141-cbfe-4d40-907c-9a467c586c46
title: Classe Msvm_Physical3dGraphicsProcessor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Physical3dGraphicsProcessor
- Msvm_Physical3dGraphicsProcessor.RequestStateChange
- Msvm_Physical3dGraphicsProcessor.SetPowerState
- Msvm_Physical3dGraphicsProcessor.Reset
- Msvm_Physical3dGraphicsProcessor.EnableDevice
- Msvm_Physical3dGraphicsProcessor.OnlineDevice
- Msvm_Physical3dGraphicsProcessor.QuiesceDevice
- Msvm_Physical3dGraphicsProcessor.SaveProperties
- Msvm_Physical3dGraphicsProcessor.RestoreProperties
- Msvm_Physical3dGraphicsProcessor.InstanceID
- Msvm_Physical3dGraphicsProcessor.Caption
- Msvm_Physical3dGraphicsProcessor.Description
- Msvm_Physical3dGraphicsProcessor.ElementName
- Msvm_Physical3dGraphicsProcessor.InstallDate
- Msvm_Physical3dGraphicsProcessor.Name
- Msvm_Physical3dGraphicsProcessor.OperationalStatus
- Msvm_Physical3dGraphicsProcessor.StatusDescriptions
- Msvm_Physical3dGraphicsProcessor.Status
- Msvm_Physical3dGraphicsProcessor.HealthState
- Msvm_Physical3dGraphicsProcessor.CommunicationStatus
- Msvm_Physical3dGraphicsProcessor.DetailedStatus
- Msvm_Physical3dGraphicsProcessor.OperatingStatus
- Msvm_Physical3dGraphicsProcessor.PrimaryStatus
- Msvm_Physical3dGraphicsProcessor.EnabledState
- Msvm_Physical3dGraphicsProcessor.OtherEnabledState
- Msvm_Physical3dGraphicsProcessor.RequestedState
- Msvm_Physical3dGraphicsProcessor.EnabledDefault
- Msvm_Physical3dGraphicsProcessor.TimeOfLastStateChange
- Msvm_Physical3dGraphicsProcessor.AvailableRequestedStates
- Msvm_Physical3dGraphicsProcessor.TransitioningToState
- Msvm_Physical3dGraphicsProcessor.SystemCreationClassName
- Msvm_Physical3dGraphicsProcessor.SystemName
- Msvm_Physical3dGraphicsProcessor.CreationClassName
- Msvm_Physical3dGraphicsProcessor.DeviceID
- Msvm_Physical3dGraphicsProcessor.PowerManagementSupported
- Msvm_Physical3dGraphicsProcessor.PowerManagementCapabilities
- Msvm_Physical3dGraphicsProcessor.Availability
- Msvm_Physical3dGraphicsProcessor.StatusInfo
- Msvm_Physical3dGraphicsProcessor.LastErrorCode
- Msvm_Physical3dGraphicsProcessor.ErrorDescription
- Msvm_Physical3dGraphicsProcessor.ErrorCleared
- Msvm_Physical3dGraphicsProcessor.OtherIdentifyingInfo
- Msvm_Physical3dGraphicsProcessor.PowerOnHours
- Msvm_Physical3dGraphicsProcessor.TotalPowerOnHours
- Msvm_Physical3dGraphicsProcessor.IdentifyingDescriptions
- Msvm_Physical3dGraphicsProcessor.AdditionalAvailability
- Msvm_Physical3dGraphicsProcessor.MaxQuiesceTime
- Msvm_Physical3dGraphicsProcessor.EnabledForVirtualization
- Msvm_Physical3dGraphicsProcessor.CompatibleForVirtualization
- Msvm_Physical3dGraphicsProcessor.GPUID
- Msvm_Physical3dGraphicsProcessor.DirectXVersion
- Msvm_Physical3dGraphicsProcessor.PixelShaderVersion
- Msvm_Physical3dGraphicsProcessor.DedicatedVideoMemory
- Msvm_Physical3dGraphicsProcessor.DedicatedSystemMemory
- Msvm_Physical3dGraphicsProcessor.SharedSystemMemory
- Msvm_Physical3dGraphicsProcessor.TotalVideoMemory
- Msvm_Physical3dGraphicsProcessor.AvailableVideoMemory
- Msvm_Physical3dGraphicsProcessor.DriverProvider
- Msvm_Physical3dGraphicsProcessor.DriverDate
- Msvm_Physical3dGraphicsProcessor.DriverInstalled
- Msvm_Physical3dGraphicsProcessor.DriverVersion
- Msvm_Physical3dGraphicsProcessor.DriverModelVersion
- Msvm_Physical3dGraphicsProcessor.Rating
- Msvm_Physical3dGraphicsProcessor.AdapterIndexID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e257fa319b1d1b55562f47c7a3049a694fc27f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663203"
---
# <a name="msvm_physical3dgraphicsprocessor-class"></a><span data-ttu-id="08045-103">\_Classe Msvm Physical3dGraphicsProcessor</span><span class="sxs-lookup"><span data-stu-id="08045-103">Msvm\_Physical3dGraphicsProcessor class</span></span>

<span data-ttu-id="08045-104">Descreve a GPU (unidade de processamento gráfico) 3-D física.</span><span class="sxs-lookup"><span data-stu-id="08045-104">Describes the physical 3-D graphics processing unit (GPU).</span></span>

<span data-ttu-id="08045-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="08045-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08045-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08045-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Physical3dGraphicsProcessor : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  Boolean  EnabledForVirtualization;
  Boolean  CompatibleForVirtualization;
  string   GPUID;
  string   DirectXVersion;
  string   PixelShaderVersion;
  uint64   DedicatedVideoMemory;
  uint64   DedicatedSystemMemory;
  uint64   SharedSystemMemory;
  uint64   TotalVideoMemory;
  uint64   AvailableVideoMemory;
  string   DriverProvider;
  datetime DriverDate;
  datetime DriverInstalled;
  string   DriverVersion;
  string   DriverModelVersion;
  uint64   Rating;
  uint64   AdapterIndexID;
};
```

## <a name="members"></a><span data-ttu-id="08045-107">Membros</span><span class="sxs-lookup"><span data-stu-id="08045-107">Members</span></span>

<span data-ttu-id="08045-108">A classe **Msvm \_ Physical3dGraphicsProcessor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="08045-108">The **Msvm\_Physical3dGraphicsProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="08045-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="08045-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="08045-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08045-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08045-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="08045-111">Methods</span></span>

<span data-ttu-id="08045-112">A classe **Msvm \_ Physical3dGraphicsProcessor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="08045-112">The **Msvm\_Physical3dGraphicsProcessor** class has these methods.</span></span>



| <span data-ttu-id="08045-113">Método</span><span class="sxs-lookup"><span data-stu-id="08045-113">Method</span></span>                 | <span data-ttu-id="08045-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="08045-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="08045-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="08045-115">**EnableDevice**</span></span>       | <span data-ttu-id="08045-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="08045-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="08045-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="08045-117">**OnlineDevice**</span></span>       | <span data-ttu-id="08045-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="08045-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="08045-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="08045-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="08045-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="08045-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="08045-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="08045-121">**RequestStateChange**</span></span> | <span data-ttu-id="08045-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="08045-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="08045-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="08045-123">**Reset**</span></span>              | <span data-ttu-id="08045-124">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="08045-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="08045-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="08045-125">**RestoreProperties**</span></span>  | <span data-ttu-id="08045-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="08045-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="08045-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="08045-127">**SaveProperties**</span></span>     | <span data-ttu-id="08045-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="08045-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="08045-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="08045-129">**SetPowerState**</span></span>      | <span data-ttu-id="08045-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="08045-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="08045-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08045-131">Properties</span></span>

<span data-ttu-id="08045-132">A classe **Msvm \_ Physical3dGraphicsProcessor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="08045-132">The **Msvm\_Physical3dGraphicsProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08045-133">**AdapterIndexID**</span><span class="sxs-lookup"><span data-stu-id="08045-133">**AdapterIndexID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-134">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08045-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08045-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-136">Especifica o identificador de índice do adaptador alocado para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08045-136">Specifies the adapter index identifier allocated to this device.</span></span>

</dd> <dt>

<span data-ttu-id="08045-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="08045-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-138">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="08045-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-140">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08045-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="08045-141">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-142">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="08045-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08045-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-145">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08045-145">The primary availability and status of the device.</span></span> <span data-ttu-id="08045-146">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="08045-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-148">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="08045-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-150">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="08045-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="08045-151">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="08045-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="08045-152">**AvailableVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="08045-152">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-153">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08045-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08045-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-155">Especifica a quantidade de memória de vídeo, em bytes, que está disponível para a GPU.</span><span class="sxs-lookup"><span data-stu-id="08045-155">Specifies the amount of video memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="08045-156">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="08045-156">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-159">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="08045-159">A short description of the object.</span></span> <span data-ttu-id="08045-160">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="08045-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="08045-161">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="08045-161">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-162">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08045-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-164">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="08045-164">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="08045-165">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="08045-165">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="08045-166">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08045-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="08045-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="08045-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08045-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="08045-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="08045-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="08045-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="08045-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="08045-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="08045-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="08045-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="08045-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="08045-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="08045-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="08045-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="08045-174">)</span><span class="sxs-lookup"><span data-stu-id="08045-174">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08045-175">**CompatibleForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="08045-175">**CompatibleForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-176">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="08045-176">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08045-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-178">**true** se for compatível para virtualização; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="08045-178">**true** if compatible for virtualization; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="08045-179">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="08045-179">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="08045-180">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="08045-180">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-183">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="08045-183">The scoping system's creation class name.</span></span> <span data-ttu-id="08045-184">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="08045-184">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="08045-185">**DedicatedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="08045-185">**DedicatedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-186">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08045-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08045-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-188">Especifica a quantidade de memória do sistema, em bytes, que é dedicada à GPU.</span><span class="sxs-lookup"><span data-stu-id="08045-188">Specifies the amount of system memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="08045-189">**DedicatedVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="08045-189">**DedicatedVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-190">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08045-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08045-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-192">Especifica a quantidade de memória de vídeo, em bytes, que é dedicada à GPU.</span><span class="sxs-lookup"><span data-stu-id="08045-192">Specifies the amount of video memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="08045-193">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="08045-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-196">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="08045-196">A description of the object.</span></span> <span data-ttu-id="08045-197">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="08045-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="08045-198">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="08045-198">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-199">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08045-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-201">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="08045-201">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="08045-202">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="08045-202">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="08045-203">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08045-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="08045-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="08045-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08045-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="08045-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="08045-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="08045-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="08045-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="08045-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="08045-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="08045-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="08045-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="08045-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="08045-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="08045-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="08045-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="08045-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="08045-212">)</span><span class="sxs-lookup"><span data-stu-id="08045-212">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08045-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="08045-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-216">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="08045-216">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="08045-217">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="08045-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="08045-218">**DirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="08045-218">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08045-221">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="08045-221">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="08045-222">Especifica o versão do DirectX que é suportado pela GPU.</span><span class="sxs-lookup"><span data-stu-id="08045-222">Specifies the verison of DirectX that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="08045-223">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="08045-223">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-224">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="08045-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08045-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-226">Especifica a data de compilação do driver.</span><span class="sxs-lookup"><span data-stu-id="08045-226">Specifies the driver build date.</span></span>

</dd> <dt>

<span data-ttu-id="08045-227">**DriverInstalled**</span><span class="sxs-lookup"><span data-stu-id="08045-227">**DriverInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-228">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="08045-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08045-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-230">Especifica a data e a hora em que o driver foi instalado.</span><span class="sxs-lookup"><span data-stu-id="08045-230">Specifies the date and time that the driver was installed.</span></span>

</dd> <dt>

<span data-ttu-id="08045-231">**DriverModelVersion**</span><span class="sxs-lookup"><span data-stu-id="08045-231">**DriverModelVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08045-234">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="08045-234">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="08045-235">Especifica a versão do modelo de driver.</span><span class="sxs-lookup"><span data-stu-id="08045-235">Specifies the driver model version.</span></span>

> [!Note]  
> <span data-ttu-id="08045-236">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="08045-236">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="08045-237">**Driverprovider**</span><span class="sxs-lookup"><span data-stu-id="08045-237">**DriverProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-238">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08045-240">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="08045-240">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="08045-241">Especifica o nome do provedor de driver.</span><span class="sxs-lookup"><span data-stu-id="08045-241">Specifies the name of the driver provider.</span></span>

</dd> <dt>

<span data-ttu-id="08045-242">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="08045-242">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08045-245">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="08045-245">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="08045-246">Especifica a versão do driver.</span><span class="sxs-lookup"><span data-stu-id="08045-246">Specifies the driver version.</span></span>

</dd> <dt>

<span data-ttu-id="08045-247">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="08045-247">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-250">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="08045-250">A display name for the object.</span></span> <span data-ttu-id="08045-251">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="08045-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="08045-252">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="08045-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-253">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08045-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-255">A configuração de inicialização ou padrão de um administrador para a propriedade **enabledstate** de um elemento.</span><span class="sxs-lookup"><span data-stu-id="08045-255">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="08045-256">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="08045-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="08045-257">**EnabledForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="08045-257">**EnabledForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-258">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="08045-258">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08045-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-260">Especifica se o adaptador foi habilitado para uso com o RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="08045-260">Specifies whether the adapter has been enabled for use with RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="08045-261">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="08045-261">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-262">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08045-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-264">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="08045-264">The enabled and disabled states of an element.</span></span> <span data-ttu-id="08045-265">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="08045-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="08045-266">Valor</span><span class="sxs-lookup"><span data-stu-id="08045-266">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="08045-267">Significado</span><span class="sxs-lookup"><span data-stu-id="08045-267">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="08045-268"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="08045-268"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="08045-269">Não foi possível determinar o estado do elemento.</span><span class="sxs-lookup"><span data-stu-id="08045-269">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="08045-270"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="08045-270"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="08045-271"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="08045-271"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="08045-272">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="08045-272">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="08045-273"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="08045-273"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="08045-274">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="08045-274">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="08045-275"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="08045-275"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="08045-276">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="08045-276">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="08045-277"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="08045-277"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="08045-278">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="08045-278">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="08045-279"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="08045-279"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="08045-280">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="08045-280">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="08045-281"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="08045-281"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="08045-282">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="08045-282">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="08045-283"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="08045-283"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="08045-284">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="08045-284">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="08045-285"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="08045-285"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="08045-286">O elemento está habilitado, mas em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="08045-286">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="08045-287">O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="08045-287">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="08045-288">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="08045-288">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="08045-289"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="08045-289"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="08045-290">O elemento está no processo de ir para um estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="08045-290">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="08045-291">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="08045-291">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="08045-292">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="08045-292">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-293">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="08045-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08045-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-295">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="08045-295">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="08045-296">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-297">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="08045-297">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-300">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="08045-300">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="08045-301">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-302">**GPUID**</span><span class="sxs-lookup"><span data-stu-id="08045-302">**GPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08045-305">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="08045-305">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="08045-306">Contém o identificador de GPU para o adaptador.</span><span class="sxs-lookup"><span data-stu-id="08045-306">Contains the GPU identifier for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="08045-307">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="08045-307">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-308">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08045-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-310">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="08045-310">The current health of the element.</span></span> <span data-ttu-id="08045-311">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08045-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08045-312">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="08045-312">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-313">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-313">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08045-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-315">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="08045-315">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="08045-316">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="08045-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-318">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="08045-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08045-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-320">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="08045-320">The date and time when the object was installed.</span></span> <span data-ttu-id="08045-321">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="08045-321">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="08045-322">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08045-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08045-323">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="08045-323">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08045-326">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="08045-326">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="08045-327">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="08045-327">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="08045-328">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="08045-328">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="08045-329">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="08045-329">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-330">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08045-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08045-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-332">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="08045-332">The last error code reported by the logical device.</span></span> <span data-ttu-id="08045-333">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-333">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-334">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="08045-334">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-335">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08045-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08045-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-337">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="08045-337">This property has been deprecated.</span></span> <span data-ttu-id="08045-338">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-339">**Nome**</span><span class="sxs-lookup"><span data-stu-id="08045-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-342">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="08045-342">The label by which the object is known.</span></span> <span data-ttu-id="08045-343">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08045-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08045-344">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="08045-344">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-345">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08045-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-347">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="08045-347">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="08045-348">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="08045-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="08045-349">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08045-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="08045-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="08045-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08045-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="08045-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="08045-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="08045-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="08045-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="08045-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="08045-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="08045-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="08045-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="08045-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="08045-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="08045-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="08045-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="08045-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="08045-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="08045-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="08045-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="08045-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="08045-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="08045-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="08045-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="08045-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="08045-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="08045-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="08045-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="08045-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="08045-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="08045-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="08045-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="08045-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="08045-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="08045-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="08045-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="08045-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="08045-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="08045-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="08045-369">)</span><span class="sxs-lookup"><span data-stu-id="08045-369">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08045-370">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="08045-370">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-371">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-371">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="08045-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-373">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="08045-373">The current statuses of the object.</span></span> <span data-ttu-id="08045-374">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08045-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08045-375">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="08045-375">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-378">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="08045-378">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="08045-379">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="08045-379">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="08045-380">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="08045-380">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="08045-381">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="08045-381">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-382">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-382">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08045-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-384">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="08045-384">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="08045-385">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-386">**PixelShaderVersion**</span><span class="sxs-lookup"><span data-stu-id="08045-386">**PixelShaderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-387">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08045-389">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="08045-389">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="08045-390">Especifica o sombreador de pixel versão que é suportado pela GPU.</span><span class="sxs-lookup"><span data-stu-id="08045-390">Specifies the pixel shader verison that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="08045-391">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="08045-391">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-392">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="08045-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-394">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08045-394">The power management capabilities of the device.</span></span> <span data-ttu-id="08045-395">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-396">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="08045-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-397">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="08045-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08045-398">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-399">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="08045-399">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="08045-400">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-401">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="08045-401">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-402">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08045-402">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08045-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-404">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="08045-404">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="08045-405">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-405">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-406">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="08045-406">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-407">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-407">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08045-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-409">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="08045-409">Provides high level status information.</span></span> <span data-ttu-id="08045-410">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="08045-410">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="08045-411">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="08045-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="08045-412">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08045-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="08045-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="08045-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08045-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="08045-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="08045-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="08045-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="08045-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="08045-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="08045-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="08045-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="08045-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="08045-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="08045-419">)</span><span class="sxs-lookup"><span data-stu-id="08045-419">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08045-420">**Classificação**</span><span class="sxs-lookup"><span data-stu-id="08045-420">**Rating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-421">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08045-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08045-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08045-423">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor")</span><span class="sxs-lookup"><span data-stu-id="08045-423">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="08045-424">Especifica a classificação RemoteFX de GPU para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08045-424">Specifies the GPU RemoteFX rating for this device.</span></span> <span data-ttu-id="08045-425">Esta propriedade não é usada no momento.</span><span class="sxs-lookup"><span data-stu-id="08045-425">This property is not currently used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-426">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="08045-426">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-427">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08045-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-429">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="08045-429">The last requested or desired state for the element.</span></span> <span data-ttu-id="08045-430">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="08045-430">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="08045-431">**SharedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="08045-431">**SharedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-432">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08045-432">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08045-433">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-434">Especifica a quantidade de memória do sistema compartilhada, em bytes, que está disponível para a GPU.</span><span class="sxs-lookup"><span data-stu-id="08045-434">Specifies the amount of shared system memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="08045-435">**Status**</span><span class="sxs-lookup"><span data-stu-id="08045-435">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-436">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-438">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="08045-438">The current status of the object.</span></span> <span data-ttu-id="08045-439">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-440">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="08045-440">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-441">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-441">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08045-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-443">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="08045-443">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="08045-444">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="08045-444">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="08045-445">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="08045-445">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-446">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08045-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-448">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="08045-448">The current state of the logical device.</span></span> <span data-ttu-id="08045-449">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-450">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="08045-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-451">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-452">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-453">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="08045-453">The scoping system's creation class name.</span></span> <span data-ttu-id="08045-454">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="08045-454">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="08045-455">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="08045-455">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-456">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="08045-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08045-457">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-458">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="08045-458">The scoping system's name.</span></span> <span data-ttu-id="08045-459">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="08045-459">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="08045-460">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="08045-460">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-461">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="08045-461">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08045-462">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-463">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="08045-463">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="08045-464">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="08045-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="08045-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="08045-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-466">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08045-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08045-467">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-468">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="08045-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="08045-469">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="08045-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="08045-470">**TotalVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="08045-470">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-471">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08045-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08045-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-473">Especifica a quantidade total de memória de vídeo, em bytes, presente na GPU.</span><span class="sxs-lookup"><span data-stu-id="08045-473">Specifies the total amount of video memory, in bytes, present on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="08045-474">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="08045-474">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08045-475">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08045-475">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08045-476">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08045-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08045-477">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="08045-477">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="08045-478">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="08045-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08045-479">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08045-479">Requirements</span></span>



| <span data-ttu-id="08045-480">Requisito</span><span class="sxs-lookup"><span data-stu-id="08045-480">Requirement</span></span> | <span data-ttu-id="08045-481">Valor</span><span class="sxs-lookup"><span data-stu-id="08045-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08045-482">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08045-482">Minimum supported client</span></span><br/> | <span data-ttu-id="08045-483">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="08045-483">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="08045-484">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08045-484">Minimum supported server</span></span><br/> | <span data-ttu-id="08045-485">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="08045-485">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="08045-486">Namespace</span><span class="sxs-lookup"><span data-stu-id="08045-486">Namespace</span></span><br/>                | <span data-ttu-id="08045-487">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="08045-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="08045-488">MOF</span><span class="sxs-lookup"><span data-stu-id="08045-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08045-489"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08045-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08045-490">DLL</span><span class="sxs-lookup"><span data-stu-id="08045-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08045-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08045-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

