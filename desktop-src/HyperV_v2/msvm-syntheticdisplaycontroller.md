---
description: Representa o estado do controlador de vídeo sintético que está presente em cada configuração de máquina virtual.
ms.assetid: E496B887-9032-43D8-A7D2-67BB77342AFD
title: Classe Msvm_SyntheticDisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayController
- Msvm_SyntheticDisplayController.SetPowerState
- Msvm_SyntheticDisplayController.EnableDevice
- Msvm_SyntheticDisplayController.OnlineDevice
- Msvm_SyntheticDisplayController.QuiesceDevice
- Msvm_SyntheticDisplayController.SaveProperties
- Msvm_SyntheticDisplayController.RestoreProperties
- Msvm_SyntheticDisplayController.InstanceID
- Msvm_SyntheticDisplayController.Caption
- Msvm_SyntheticDisplayController.Description
- Msvm_SyntheticDisplayController.ElementName
- Msvm_SyntheticDisplayController.InstallDate
- Msvm_SyntheticDisplayController.Name
- Msvm_SyntheticDisplayController.OperationalStatus
- Msvm_SyntheticDisplayController.StatusDescriptions
- Msvm_SyntheticDisplayController.Status
- Msvm_SyntheticDisplayController.HealthState
- Msvm_SyntheticDisplayController.CommunicationStatus
- Msvm_SyntheticDisplayController.DetailedStatus
- Msvm_SyntheticDisplayController.OperatingStatus
- Msvm_SyntheticDisplayController.PrimaryStatus
- Msvm_SyntheticDisplayController.EnabledState
- Msvm_SyntheticDisplayController.OtherEnabledState
- Msvm_SyntheticDisplayController.RequestedState
- Msvm_SyntheticDisplayController.EnabledDefault
- Msvm_SyntheticDisplayController.TimeOfLastStateChange
- Msvm_SyntheticDisplayController.AvailableRequestedStates
- Msvm_SyntheticDisplayController.TransitioningToState
- Msvm_SyntheticDisplayController.SystemCreationClassName
- Msvm_SyntheticDisplayController.SystemName
- Msvm_SyntheticDisplayController.CreationClassName
- Msvm_SyntheticDisplayController.DeviceID
- Msvm_SyntheticDisplayController.PowerManagementSupported
- Msvm_SyntheticDisplayController.PowerManagementCapabilities
- Msvm_SyntheticDisplayController.Availability
- Msvm_SyntheticDisplayController.StatusInfo
- Msvm_SyntheticDisplayController.LastErrorCode
- Msvm_SyntheticDisplayController.ErrorDescription
- Msvm_SyntheticDisplayController.ErrorCleared
- Msvm_SyntheticDisplayController.PowerOnHours
- Msvm_SyntheticDisplayController.TotalPowerOnHours
- Msvm_SyntheticDisplayController.OtherIdentifyingInfo
- Msvm_SyntheticDisplayController.IdentifyingDescriptions
- Msvm_SyntheticDisplayController.AdditionalAvailability
- Msvm_SyntheticDisplayController.MaxQuiesceTime
- Msvm_SyntheticDisplayController.TimeOfLastReset
- Msvm_SyntheticDisplayController.ProtocolSupported
- Msvm_SyntheticDisplayController.MaxNumberControlled
- Msvm_SyntheticDisplayController.ProtocolDescription
- Msvm_SyntheticDisplayController.VideoProcessor
- Msvm_SyntheticDisplayController.VideoMemoryType
- Msvm_SyntheticDisplayController.OtherVideoMemoryType
- Msvm_SyntheticDisplayController.NumberOfVideoPages
- Msvm_SyntheticDisplayController.MaxMemorySupported
- Msvm_SyntheticDisplayController.AcceleratorCapabilities
- Msvm_SyntheticDisplayController.CapabilityDescriptions
- Msvm_SyntheticDisplayController.OtherVideoArchitecture
- Msvm_SyntheticDisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7f566bf2a75b3ed4f503da245d7b6ce428dce5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827609"
---
# <a name="msvm_syntheticdisplaycontroller-class"></a><span data-ttu-id="d384a-103">\_Classe Msvm SyntheticDisplayController</span><span class="sxs-lookup"><span data-stu-id="d384a-103">Msvm\_SyntheticDisplayController class</span></span>

<span data-ttu-id="d384a-104">Representa o estado do controlador de vídeo sintético que está presente em cada configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d384a-104">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="d384a-105">Somente um controlador de vídeo pode estar ativo em uma máquina virtual a qualquer momento e o controlador sintético pode ser ativado somente quando o sistema operacional convidado carregou os serviços de aceleração de vídeo necessários.</span><span class="sxs-lookup"><span data-stu-id="d384a-105">Only one display controller can be active in a virtual machine at any time and the synthetic controller can be activated only when the guest operating system has loaded the required video acceleration services.</span></span>

<span data-ttu-id="d384a-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d384a-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d384a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d384a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Synthetic Display Controller";
  string   ElementName = "Display Controller";
  datetime InstallDate;
  string   Name = "Display Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_SyntheticDisplayController";
  string   DeviceID = "Microsoft:GUID";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 1024;
  uint32   MaxMemorySupported = 4194304;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="d384a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d384a-108">Members</span></span>

<span data-ttu-id="d384a-109">A classe **Msvm \_ SyntheticDisplayController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d384a-109">The **Msvm\_SyntheticDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="d384a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d384a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d384a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d384a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d384a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d384a-112">Methods</span></span>

<span data-ttu-id="d384a-113">A classe **Msvm \_ SyntheticDisplayController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d384a-113">The **Msvm\_SyntheticDisplayController** class has these methods.</span></span>



| <span data-ttu-id="d384a-114">Método</span><span class="sxs-lookup"><span data-stu-id="d384a-114">Method</span></span>                                                                           | <span data-ttu-id="d384a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d384a-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="d384a-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d384a-116">**EnableDevice**</span></span>                                                                 | <span data-ttu-id="d384a-117">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d384a-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d384a-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="d384a-118">**OnlineDevice**</span></span>                                                                 | <span data-ttu-id="d384a-119">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d384a-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d384a-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="d384a-120">**QuiesceDevice**</span></span>                                                                | <span data-ttu-id="d384a-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d384a-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d384a-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d384a-122">**RequestStateChange**</span></span>](msvm-syntheticdisplaycontroller-requeststatechange.md) | <span data-ttu-id="d384a-123">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="d384a-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="d384a-124">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="d384a-124">**Reset**</span></span>](msvm-syntheticdisplaycontroller-reset.md)                           | <span data-ttu-id="d384a-125">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="d384a-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="d384a-126">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="d384a-126">**RestoreProperties**</span></span>                                                            | <span data-ttu-id="d384a-127">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d384a-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d384a-128">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="d384a-128">**SaveProperties**</span></span>                                                               | <span data-ttu-id="d384a-129">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d384a-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d384a-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d384a-130">**SetPowerState**</span></span>                                                                | <span data-ttu-id="d384a-131">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d384a-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d384a-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d384a-132">Properties</span></span>

<span data-ttu-id="d384a-133">A classe **Msvm \_ SyntheticDisplayController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d384a-133">The **Msvm\_SyntheticDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d384a-134">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d384a-134">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-135">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d384a-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-137">Os elementos gráficos e as funcionalidades 3D do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d384a-137">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="d384a-138">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))e é sempre definida como 2 (acelerador de gráficos).</span><span class="sxs-lookup"><span data-stu-id="d384a-138">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (Graphics Accelerator).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="d384a-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-140">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d384a-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-142">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="d384a-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-143">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="d384a-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-146">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="d384a-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d384a-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-148">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d384a-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-150">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d384a-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d384a-151">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d384a-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-152">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d384a-152">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-153">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d384a-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-155">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos do acelerador de vídeo indicados na matriz da propriedade **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="d384a-155">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="d384a-156">Cada entrada dessa matriz está relacionada à entrada na matriz da propriedade **AcceleratorCapabilities** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="d384a-156">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="d384a-157">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))e é sempre definida como "acelerador de gráficos".</span><span class="sxs-lookup"><span data-stu-id="d384a-157">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Graphics Accelerator".</span></span>

</dd> <dt>

<span data-ttu-id="d384a-158">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d384a-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-161">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d384a-161">A short description of the object.</span></span> <span data-ttu-id="d384a-162">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "controlador de vídeo".</span><span class="sxs-lookup"><span data-stu-id="d384a-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="d384a-163">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d384a-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-164">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-166">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="d384a-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d384a-167">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d384a-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d384a-168">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d384a-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d384a-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d384a-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="d384a-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="d384a-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="d384a-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="d384a-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d384a-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d384a-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d384a-176">)</span><span class="sxs-lookup"><span data-stu-id="d384a-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d384a-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d384a-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-178">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-180">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="d384a-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d384a-181">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Msvm \_ SyntheticDisplayController".</span><span class="sxs-lookup"><span data-stu-id="d384a-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_SyntheticDisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="d384a-182">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d384a-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-185">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="d384a-185">A description of the object.</span></span> <span data-ttu-id="d384a-186">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "controlador de vídeo sintético da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="d384a-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Synthetic Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="d384a-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d384a-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-188">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-190">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="d384a-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d384a-191">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d384a-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d384a-192">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d384a-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d384a-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="d384a-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="d384a-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="d384a-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="d384a-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="d384a-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="d384a-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d384a-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d384a-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d384a-201">)</span><span class="sxs-lookup"><span data-stu-id="d384a-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d384a-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d384a-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-205">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="d384a-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="d384a-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d384a-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-209">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d384a-209">A display name for the object.</span></span> <span data-ttu-id="d384a-210">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "controlador de vídeo" por padrão.</span><span class="sxs-lookup"><span data-stu-id="d384a-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller" by default.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d384a-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-212">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-214">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="d384a-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d384a-215">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="d384a-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-216">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d384a-216">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-219">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="d384a-219">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d384a-220">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="d384a-220">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="d384a-221">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado) ou 3 (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="d384a-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-222">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d384a-222">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-223">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d384a-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-225">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d384a-225">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-226">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d384a-226">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-229">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d384a-229">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-230">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d384a-230">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-231">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-233">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="d384a-233">The current health of the element.</span></span> <span data-ttu-id="d384a-234">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subelementos.</span><span class="sxs-lookup"><span data-stu-id="d384a-234">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="d384a-235">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="d384a-235">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d384a-236">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="d384a-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-237">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d384a-237">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-238">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-238">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d384a-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-240">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d384a-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d384a-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-242">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d384a-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-244">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="d384a-244">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d384a-245">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d384a-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d384a-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d384a-249">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d384a-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d384a-250">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d384a-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d384a-251">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d384a-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-252">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d384a-252">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-253">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d384a-253">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-255">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d384a-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-256">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="d384a-256">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-257">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d384a-257">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-259">A quantidade máxima de memória com suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d384a-259">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="d384a-260">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))e é sempre definida como 4.194.304 (0x400000).</span><span class="sxs-lookup"><span data-stu-id="d384a-260">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 4,194,304 (0x400000).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-261">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="d384a-261">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-262">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d384a-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-264">O número máximo de entidades diretamente endereçáveis que são suportadas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="d384a-264">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="d384a-265">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="d384a-265">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="d384a-266">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="d384a-266">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="d384a-267">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)e é sempre definida como 1.</span><span class="sxs-lookup"><span data-stu-id="d384a-267">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-268">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="d384a-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-269">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d384a-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-271">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d384a-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-272">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d384a-272">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-275">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="d384a-275">The label by which the object is known.</span></span> <span data-ttu-id="d384a-276">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é a mesma que a propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="d384a-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-277">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="d384a-277">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-278">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d384a-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-280">O número de páginas de vídeo com suporte dadas as resoluções atuais e a memória disponível.</span><span class="sxs-lookup"><span data-stu-id="d384a-280">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="d384a-281">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))e é sempre definida como 1024.</span><span class="sxs-lookup"><span data-stu-id="d384a-281">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 1024.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-282">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d384a-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-283">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-285">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="d384a-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d384a-286">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d384a-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d384a-287">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d384a-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d384a-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d384a-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="d384a-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="d384a-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="d384a-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="d384a-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="d384a-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="d384a-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="d384a-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="d384a-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="d384a-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="d384a-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="d384a-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="d384a-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="d384a-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="d384a-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="d384a-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="d384a-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d384a-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d384a-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d384a-307">)</span><span class="sxs-lookup"><span data-stu-id="d384a-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d384a-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d384a-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-309">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d384a-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-311">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="d384a-311">The current statuses of the object.</span></span> <span data-ttu-id="d384a-312">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="d384a-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-313">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d384a-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-314">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-316">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="d384a-316">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d384a-317">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="d384a-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d384a-318">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d384a-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d384a-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-320">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d384a-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-322">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d384a-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-323">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="d384a-323">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-326">Uma cadeia de caracteres que descreve o tipo de arquitetura de vídeo quando a propriedade **VideoArchitecture** é 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="d384a-326">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="d384a-327">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d384a-327">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-328">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="d384a-328">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-329">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-331">O tipo de memória de vídeo quando a propriedade **VideoMemoryType** da instância é 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="d384a-331">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="d384a-332">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d384a-332">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-333">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d384a-333">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-334">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-334">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d384a-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-336">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d384a-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-337">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d384a-337">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-338">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d384a-338">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-340">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d384a-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-341">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d384a-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-342">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d384a-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-344">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d384a-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-345">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d384a-345">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-346">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-348">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="d384a-348">Provides high level status information.</span></span> <span data-ttu-id="d384a-349">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="d384a-349">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d384a-350">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d384a-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d384a-351">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d384a-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d384a-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d384a-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-353"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d384a-353"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="d384a-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="d384a-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d384a-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d384a-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d384a-358">)</span><span class="sxs-lookup"><span data-stu-id="d384a-358">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d384a-359">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="d384a-359">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-362">Uma cadeia de caracteres que fornece mais informações relacionadas ao protocolo suportado pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="d384a-362">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="d384a-363">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)e é sempre definida como "vídeo".</span><span class="sxs-lookup"><span data-stu-id="d384a-363">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to "Video".</span></span>

</dd> <dt>

<span data-ttu-id="d384a-364">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="d384a-364">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-365">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-367">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="d384a-367">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="d384a-368">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)e é sempre definida como 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="d384a-368">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d384a-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-370">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-372">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="d384a-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="d384a-373">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="d384a-373">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="d384a-374">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="d384a-374">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="d384a-375">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte A **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="d384a-375">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="d384a-376">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="d384a-376">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="d384a-377">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement** e é definida como 2 (habilitado), 3 (desabilitado) ou 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="d384a-377">This property is inherited from **CIM\_EnabledLogicalElement**, and it is set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="d384a-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-381">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d384a-381">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-382">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d384a-382">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-383">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-383">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d384a-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-385">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d384a-385">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d384a-386">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="d384a-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="d384a-387">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d384a-387">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-388">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-390">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d384a-390">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-391">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d384a-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-392">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-394">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d384a-394">The scoping system's creation class name.</span></span> <span data-ttu-id="d384a-395">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="d384a-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="d384a-396">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d384a-396">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-397">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-398">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-399">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="d384a-399">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="d384a-400">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d384a-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-401">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="d384a-401">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-402">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d384a-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-404">A última vez em que a máquina virtual estava ligada.</span><span class="sxs-lookup"><span data-stu-id="d384a-404">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="d384a-405">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="d384a-405">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-406">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d384a-406">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-407">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d384a-407">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-409">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="d384a-409">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d384a-410">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d384a-410">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-411">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d384a-411">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-412">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d384a-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-414">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d384a-414">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-415">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d384a-415">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-416">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-417">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-418">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="d384a-418">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d384a-419">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d384a-419">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d384a-420">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="d384a-420">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-421">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-423">Especifica a arquitetura de vídeo do controlador de vídeo usada para gerar o sinal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d384a-423">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="d384a-424">Normalmente, um processador de vídeo dedicado gera o sinal de vídeo de acordo com a arquitetura especificada.</span><span class="sxs-lookup"><span data-stu-id="d384a-424">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="d384a-425">É um indicador da capacidade de resolução máxima do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d384a-425">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="d384a-426">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d384a-426">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d384a-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d384a-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d384a-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="d384a-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="d384a-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="d384a-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="d384a-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="d384a-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="d384a-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="d384a-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="d384a-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="d384a-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Buffer de quadro linear** (11)</span><span class="sxs-lookup"><span data-stu-id="d384a-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="d384a-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d384a-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d384a-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d384a-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d384a-442">)</span><span class="sxs-lookup"><span data-stu-id="d384a-442">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d384a-443">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="d384a-443">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-444">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d384a-444">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-445">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-446">O tipo de memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d384a-446">The type of video memory.</span></span> <span data-ttu-id="d384a-447">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))e é sempre definida como 2 (VRAM).</span><span class="sxs-lookup"><span data-stu-id="d384a-447">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (VRAM).</span></span>

</dd> <dt>

<span data-ttu-id="d384a-448">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="d384a-448">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d384a-449">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d384a-449">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d384a-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d384a-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d384a-451">Uma cadeia de caracteres que descreve o controlador/processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d384a-451">A string that describes the video processor/controller.</span></span> <span data-ttu-id="d384a-452">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))e é sempre definida como "processador de vídeo sintético".</span><span class="sxs-lookup"><span data-stu-id="d384a-452">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Synthetic Video Processor".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d384a-453">Comentários</span><span class="sxs-lookup"><span data-stu-id="d384a-453">Remarks</span></span>

<span data-ttu-id="d384a-454">O acesso à classe **Msvm \_ SyntheticDisplayController** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="d384a-454">Access to the **Msvm\_SyntheticDisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d384a-455">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d384a-455">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d384a-456">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d384a-456">Requirements</span></span>



| <span data-ttu-id="d384a-457">Requisito</span><span class="sxs-lookup"><span data-stu-id="d384a-457">Requirement</span></span> | <span data-ttu-id="d384a-458">Valor</span><span class="sxs-lookup"><span data-stu-id="d384a-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d384a-459">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d384a-459">Minimum supported client</span></span><br/> | <span data-ttu-id="d384a-460">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d384a-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d384a-461">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d384a-461">Minimum supported server</span></span><br/> | <span data-ttu-id="d384a-462">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d384a-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d384a-463">Namespace</span><span class="sxs-lookup"><span data-stu-id="d384a-463">Namespace</span></span><br/>                | <span data-ttu-id="d384a-464">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d384a-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d384a-465">MOF</span><span class="sxs-lookup"><span data-stu-id="d384a-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d384a-466"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d384a-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d384a-467">DLL</span><span class="sxs-lookup"><span data-stu-id="d384a-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d384a-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d384a-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d384a-469">Confira também</span><span class="sxs-lookup"><span data-stu-id="d384a-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d384a-470">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="d384a-470">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="d384a-471">[**\_DISPLAYCONTROLLER CIM**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d384a-471">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d384a-472">Classes de vídeo</span><span class="sxs-lookup"><span data-stu-id="d384a-472">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

