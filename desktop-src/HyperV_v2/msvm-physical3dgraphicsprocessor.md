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
# <a name="msvm_physical3dgraphicsprocessor-class"></a><span data-ttu-id="2015c-103">\_Classe Msvm Physical3dGraphicsProcessor</span><span class="sxs-lookup"><span data-stu-id="2015c-103">Msvm\_Physical3dGraphicsProcessor class</span></span>

<span data-ttu-id="2015c-104">Descreve a GPU (unidade de processamento gráfico) 3-D física.</span><span class="sxs-lookup"><span data-stu-id="2015c-104">Describes the physical 3-D graphics processing unit (GPU).</span></span>

<span data-ttu-id="2015c-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2015c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2015c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2015c-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="2015c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2015c-107">Members</span></span>

<span data-ttu-id="2015c-108">A classe **Msvm \_ Physical3dGraphicsProcessor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2015c-108">The **Msvm\_Physical3dGraphicsProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="2015c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2015c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2015c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2015c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2015c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2015c-111">Methods</span></span>

<span data-ttu-id="2015c-112">A classe **Msvm \_ Physical3dGraphicsProcessor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2015c-112">The **Msvm\_Physical3dGraphicsProcessor** class has these methods.</span></span>



| <span data-ttu-id="2015c-113">Método</span><span class="sxs-lookup"><span data-stu-id="2015c-113">Method</span></span>                 | <span data-ttu-id="2015c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2015c-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="2015c-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="2015c-115">**EnableDevice**</span></span>       | <span data-ttu-id="2015c-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2015c-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2015c-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="2015c-117">**OnlineDevice**</span></span>       | <span data-ttu-id="2015c-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2015c-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2015c-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="2015c-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="2015c-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2015c-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2015c-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2015c-121">**RequestStateChange**</span></span> | <span data-ttu-id="2015c-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2015c-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2015c-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="2015c-123">**Reset**</span></span>              | <span data-ttu-id="2015c-124">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2015c-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2015c-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="2015c-125">**RestoreProperties**</span></span>  | <span data-ttu-id="2015c-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2015c-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2015c-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="2015c-127">**SaveProperties**</span></span>     | <span data-ttu-id="2015c-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2015c-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2015c-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2015c-129">**SetPowerState**</span></span>      | <span data-ttu-id="2015c-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2015c-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2015c-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2015c-131">Properties</span></span>

<span data-ttu-id="2015c-132">A classe **Msvm \_ Physical3dGraphicsProcessor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2015c-132">The **Msvm\_Physical3dGraphicsProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2015c-133">**AdapterIndexID**</span><span class="sxs-lookup"><span data-stu-id="2015c-133">**AdapterIndexID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-134">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2015c-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-136">Especifica o identificador de índice do adaptador alocado para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2015c-136">Specifies the adapter index identifier allocated to this device.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="2015c-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-138">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2015c-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-140">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2015c-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="2015c-141">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-142">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="2015c-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-145">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2015c-145">The primary availability and status of the device.</span></span> <span data-ttu-id="2015c-146">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2015c-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-148">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2015c-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-150">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="2015c-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="2015c-151">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2015c-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-152">**AvailableVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="2015c-152">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-153">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2015c-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-155">Especifica a quantidade de memória de vídeo, em bytes, que está disponível para a GPU.</span><span class="sxs-lookup"><span data-stu-id="2015c-155">Specifies the amount of video memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-156">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="2015c-156">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-159">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="2015c-159">A short description of the object.</span></span> <span data-ttu-id="2015c-160">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-161">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2015c-161">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-162">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-164">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="2015c-164">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2015c-165">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2015c-165">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2015c-166">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2015c-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2015c-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="2015c-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="2015c-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="2015c-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="2015c-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2015c-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2015c-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2015c-174">)</span><span class="sxs-lookup"><span data-stu-id="2015c-174">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2015c-175">**CompatibleForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="2015c-175">**CompatibleForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-176">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2015c-176">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-178">**true** se for compatível para virtualização; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="2015c-178">**true** if compatible for virtualization; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="2015c-179">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="2015c-179">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="2015c-180">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2015c-180">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-183">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="2015c-183">The scoping system's creation class name.</span></span> <span data-ttu-id="2015c-184">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2015c-184">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-185">**DedicatedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="2015c-185">**DedicatedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-186">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2015c-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-188">Especifica a quantidade de memória do sistema, em bytes, que é dedicada à GPU.</span><span class="sxs-lookup"><span data-stu-id="2015c-188">Specifies the amount of system memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-189">**DedicatedVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="2015c-189">**DedicatedVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-190">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2015c-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-192">Especifica a quantidade de memória de vídeo, em bytes, que é dedicada à GPU.</span><span class="sxs-lookup"><span data-stu-id="2015c-192">Specifies the amount of video memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-193">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2015c-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-196">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="2015c-196">A description of the object.</span></span> <span data-ttu-id="2015c-197">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-198">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2015c-198">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-199">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-201">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="2015c-201">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2015c-202">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2015c-202">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2015c-203">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2015c-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="2015c-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="2015c-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="2015c-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="2015c-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="2015c-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="2015c-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2015c-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2015c-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2015c-212">)</span><span class="sxs-lookup"><span data-stu-id="2015c-212">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2015c-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2015c-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-216">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2015c-216">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="2015c-217">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2015c-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-218">**DirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="2015c-218">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2015c-221">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2015c-221">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2015c-222">Especifica o versão do DirectX que é suportado pela GPU.</span><span class="sxs-lookup"><span data-stu-id="2015c-222">Specifies the verison of DirectX that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-223">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="2015c-223">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-224">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2015c-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-226">Especifica a data de compilação do driver.</span><span class="sxs-lookup"><span data-stu-id="2015c-226">Specifies the driver build date.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-227">**DriverInstalled**</span><span class="sxs-lookup"><span data-stu-id="2015c-227">**DriverInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-228">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2015c-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-230">Especifica a data e a hora em que o driver foi instalado.</span><span class="sxs-lookup"><span data-stu-id="2015c-230">Specifies the date and time that the driver was installed.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-231">**DriverModelVersion**</span><span class="sxs-lookup"><span data-stu-id="2015c-231">**DriverModelVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2015c-234">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2015c-234">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2015c-235">Especifica a versão do modelo de driver.</span><span class="sxs-lookup"><span data-stu-id="2015c-235">Specifies the driver model version.</span></span>

> [!Note]  
> <span data-ttu-id="2015c-236">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="2015c-236">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="2015c-237">**Driverprovider**</span><span class="sxs-lookup"><span data-stu-id="2015c-237">**DriverProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-238">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2015c-240">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2015c-240">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2015c-241">Especifica o nome do provedor de driver.</span><span class="sxs-lookup"><span data-stu-id="2015c-241">Specifies the name of the driver provider.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-242">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="2015c-242">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2015c-245">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2015c-245">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2015c-246">Especifica a versão do driver.</span><span class="sxs-lookup"><span data-stu-id="2015c-246">Specifies the driver version.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-247">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2015c-247">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-250">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="2015c-250">A display name for the object.</span></span> <span data-ttu-id="2015c-251">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-252">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2015c-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-253">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-255">A configuração de inicialização ou padrão de um administrador para a propriedade **enabledstate** de um elemento.</span><span class="sxs-lookup"><span data-stu-id="2015c-255">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="2015c-256">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="2015c-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-257">**EnabledForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="2015c-257">**EnabledForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-258">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2015c-258">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-260">Especifica se o adaptador foi habilitado para uso com o RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="2015c-260">Specifies whether the adapter has been enabled for use with RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-261">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2015c-261">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-262">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-264">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="2015c-264">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2015c-265">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2015c-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="2015c-266">Valor</span><span class="sxs-lookup"><span data-stu-id="2015c-266">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="2015c-267">Significado</span><span class="sxs-lookup"><span data-stu-id="2015c-267">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="2015c-268"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="2015c-268"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="2015c-269">Não foi possível determinar o estado do elemento.</span><span class="sxs-lookup"><span data-stu-id="2015c-269">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="2015c-270"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-270"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="2015c-271"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-271"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="2015c-272">O elemento está em execução.</span><span class="sxs-lookup"><span data-stu-id="2015c-272">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="2015c-273"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-273"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="2015c-274">O elemento está desativado.</span><span class="sxs-lookup"><span data-stu-id="2015c-274">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="2015c-275"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-275"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="2015c-276">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2015c-276">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="2015c-277"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-277"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="2015c-278">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2015c-278">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="2015c-279"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-279"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="2015c-280">O elemento pode estar concluindo comandos e removerá todas as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="2015c-280">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="2015c-281"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-281"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="2015c-282">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="2015c-282">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="2015c-283"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-283"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="2015c-284">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="2015c-284">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="2015c-285"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-285"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="2015c-286">O elemento está habilitado, mas em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="2015c-286">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="2015c-287">O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="2015c-287">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="2015c-288">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="2015c-288">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="2015c-289"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-289"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="2015c-290">O elemento está no processo de ir para um estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="2015c-290">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="2015c-291">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="2015c-291">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="2015c-292">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2015c-292">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-293">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2015c-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-295">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="2015c-295">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="2015c-296">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-297">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2015c-297">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-300">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="2015c-300">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="2015c-301">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-302">**GPUID**</span><span class="sxs-lookup"><span data-stu-id="2015c-302">**GPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2015c-305">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2015c-305">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2015c-306">Contém o identificador de GPU para o adaptador.</span><span class="sxs-lookup"><span data-stu-id="2015c-306">Contains the GPU identifier for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-307">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2015c-307">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-308">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-310">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="2015c-310">The current health of the element.</span></span> <span data-ttu-id="2015c-311">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-312">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2015c-312">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-313">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-313">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2015c-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-315">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="2015c-315">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="2015c-316">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2015c-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-318">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2015c-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-320">A data e a hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="2015c-320">The date and time when the object was installed.</span></span> <span data-ttu-id="2015c-321">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="2015c-321">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="2015c-322">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-323">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2015c-323">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2015c-326">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="2015c-326">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2015c-327">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="2015c-327">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2015c-328">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-328">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-329">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2015c-329">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-330">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2015c-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-332">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2015c-332">The last error code reported by the logical device.</span></span> <span data-ttu-id="2015c-333">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-333">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-334">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="2015c-334">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-335">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2015c-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-337">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="2015c-337">This property has been deprecated.</span></span> <span data-ttu-id="2015c-338">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-339">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2015c-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-342">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="2015c-342">The label by which the object is known.</span></span> <span data-ttu-id="2015c-343">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-344">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2015c-344">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-345">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-347">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="2015c-347">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2015c-348">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2015c-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2015c-349">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2015c-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2015c-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="2015c-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="2015c-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="2015c-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="2015c-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="2015c-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="2015c-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="2015c-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="2015c-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="2015c-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="2015c-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="2015c-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="2015c-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="2015c-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="2015c-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="2015c-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="2015c-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2015c-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2015c-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2015c-369">)</span><span class="sxs-lookup"><span data-stu-id="2015c-369">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2015c-370">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2015c-370">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-371">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-371">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2015c-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-373">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="2015c-373">The current statuses of the object.</span></span> <span data-ttu-id="2015c-374">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-375">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2015c-375">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-378">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="2015c-378">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="2015c-379">Essa propriedade deve ser definida como **NULL** quando a propriedade **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="2015c-379">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="2015c-380">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2015c-380">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-381">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2015c-381">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-382">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-382">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2015c-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-384">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2015c-384">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="2015c-385">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-386">**PixelShaderVersion**</span><span class="sxs-lookup"><span data-stu-id="2015c-386">**PixelShaderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-387">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2015c-389">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2015c-389">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2015c-390">Especifica o sombreador de pixel versão que é suportado pela GPU.</span><span class="sxs-lookup"><span data-stu-id="2015c-390">Specifies the pixel shader verison that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-391">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2015c-391">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-392">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2015c-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-394">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2015c-394">The power management capabilities of the device.</span></span> <span data-ttu-id="2015c-395">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-396">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2015c-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-397">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2015c-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-398">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-399">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="2015c-399">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="2015c-400">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-401">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2015c-401">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-402">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2015c-402">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-404">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="2015c-404">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="2015c-405">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-405">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-406">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2015c-406">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-407">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-407">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-409">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="2015c-409">Provides high level status information.</span></span> <span data-ttu-id="2015c-410">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="2015c-410">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="2015c-411">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2015c-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2015c-412">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2015c-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2015c-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="2015c-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="2015c-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="2015c-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2015c-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2015c-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2015c-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2015c-419">)</span><span class="sxs-lookup"><span data-stu-id="2015c-419">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2015c-420">**Classificação**</span><span class="sxs-lookup"><span data-stu-id="2015c-420">**Rating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-421">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2015c-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2015c-423">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor")</span><span class="sxs-lookup"><span data-stu-id="2015c-423">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="2015c-424">Especifica a classificação RemoteFX de GPU para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2015c-424">Specifies the GPU RemoteFX rating for this device.</span></span> <span data-ttu-id="2015c-425">Esta propriedade não é usada no momento.</span><span class="sxs-lookup"><span data-stu-id="2015c-425">This property is not currently used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-426">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2015c-426">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-427">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-429">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="2015c-429">The last requested or desired state for the element.</span></span> <span data-ttu-id="2015c-430">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="2015c-430">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-431">**SharedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="2015c-431">**SharedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-432">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2015c-432">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-433">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-434">Especifica a quantidade de memória do sistema compartilhada, em bytes, que está disponível para a GPU.</span><span class="sxs-lookup"><span data-stu-id="2015c-434">Specifies the amount of shared system memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-435">**Status**</span><span class="sxs-lookup"><span data-stu-id="2015c-435">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-436">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-438">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2015c-438">The current status of the object.</span></span> <span data-ttu-id="2015c-439">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-440">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2015c-440">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-441">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-441">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2015c-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-443">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="2015c-443">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2015c-444">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2015c-444">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-445">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2015c-445">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-446">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-448">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2015c-448">The current state of the logical device.</span></span> <span data-ttu-id="2015c-449">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-450">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2015c-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-451">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-452">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-453">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="2015c-453">The scoping system's creation class name.</span></span> <span data-ttu-id="2015c-454">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2015c-454">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-455">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2015c-455">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-456">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2015c-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-457">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-458">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="2015c-458">The scoping system's name.</span></span> <span data-ttu-id="2015c-459">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2015c-459">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2015c-460">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2015c-460">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-461">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2015c-461">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-462">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-463">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="2015c-463">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2015c-464">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2015c-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2015c-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-466">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2015c-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-467">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-468">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="2015c-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="2015c-469">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2015c-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-470">**TotalVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="2015c-470">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-471">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2015c-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-473">Especifica a quantidade total de memória de vídeo, em bytes, presente na GPU.</span><span class="sxs-lookup"><span data-stu-id="2015c-473">Specifies the total amount of video memory, in bytes, present on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2015c-474">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2015c-474">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2015c-475">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2015c-475">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2015c-476">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2015c-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2015c-477">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="2015c-477">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2015c-478">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2015c-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2015c-479">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2015c-479">Requirements</span></span>



| <span data-ttu-id="2015c-480">Requisito</span><span class="sxs-lookup"><span data-stu-id="2015c-480">Requirement</span></span> | <span data-ttu-id="2015c-481">Valor</span><span class="sxs-lookup"><span data-stu-id="2015c-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2015c-482">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2015c-482">Minimum supported client</span></span><br/> | <span data-ttu-id="2015c-483">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2015c-483">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2015c-484">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2015c-484">Minimum supported server</span></span><br/> | <span data-ttu-id="2015c-485">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="2015c-485">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2015c-486">Namespace</span><span class="sxs-lookup"><span data-stu-id="2015c-486">Namespace</span></span><br/>                | <span data-ttu-id="2015c-487">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2015c-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2015c-488">MOF</span><span class="sxs-lookup"><span data-stu-id="2015c-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2015c-489"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2015c-490">DLL</span><span class="sxs-lookup"><span data-stu-id="2015c-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2015c-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2015c-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

