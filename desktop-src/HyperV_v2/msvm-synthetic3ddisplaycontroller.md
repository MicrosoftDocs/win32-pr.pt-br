---
description: Representa o controlador de vídeo sintético 3D atribuído a uma máquina virtual.
ms.assetid: 5679668B-7D0B-421C-92B6-8A320090DFF7
title: Classe Msvm_Synthetic3DDisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayController
- Msvm_Synthetic3DDisplayController.RequestStateChange
- Msvm_Synthetic3DDisplayController.SetPowerState
- Msvm_Synthetic3DDisplayController.Reset
- Msvm_Synthetic3DDisplayController.EnableDevice
- Msvm_Synthetic3DDisplayController.OnlineDevice
- Msvm_Synthetic3DDisplayController.QuiesceDevice
- Msvm_Synthetic3DDisplayController.SaveProperties
- Msvm_Synthetic3DDisplayController.RestoreProperties
- Msvm_Synthetic3DDisplayController.InstanceID
- Msvm_Synthetic3DDisplayController.Caption
- Msvm_Synthetic3DDisplayController.Description
- Msvm_Synthetic3DDisplayController.ElementName
- Msvm_Synthetic3DDisplayController.InstallDate
- Msvm_Synthetic3DDisplayController.Name
- Msvm_Synthetic3DDisplayController.OperationalStatus
- Msvm_Synthetic3DDisplayController.StatusDescriptions
- Msvm_Synthetic3DDisplayController.Status
- Msvm_Synthetic3DDisplayController.HealthState
- Msvm_Synthetic3DDisplayController.CommunicationStatus
- Msvm_Synthetic3DDisplayController.DetailedStatus
- Msvm_Synthetic3DDisplayController.OperatingStatus
- Msvm_Synthetic3DDisplayController.PrimaryStatus
- Msvm_Synthetic3DDisplayController.EnabledState
- Msvm_Synthetic3DDisplayController.OtherEnabledState
- Msvm_Synthetic3DDisplayController.RequestedState
- Msvm_Synthetic3DDisplayController.EnabledDefault
- Msvm_Synthetic3DDisplayController.TimeOfLastStateChange
- Msvm_Synthetic3DDisplayController.AvailableRequestedStates
- Msvm_Synthetic3DDisplayController.TransitioningToState
- Msvm_Synthetic3DDisplayController.SystemCreationClassName
- Msvm_Synthetic3DDisplayController.SystemName
- Msvm_Synthetic3DDisplayController.CreationClassName
- Msvm_Synthetic3DDisplayController.DeviceID
- Msvm_Synthetic3DDisplayController.PowerManagementSupported
- Msvm_Synthetic3DDisplayController.PowerManagementCapabilities
- Msvm_Synthetic3DDisplayController.Availability
- Msvm_Synthetic3DDisplayController.StatusInfo
- Msvm_Synthetic3DDisplayController.LastErrorCode
- Msvm_Synthetic3DDisplayController.ErrorDescription
- Msvm_Synthetic3DDisplayController.ErrorCleared
- Msvm_Synthetic3DDisplayController.PowerOnHours
- Msvm_Synthetic3DDisplayController.TotalPowerOnHours
- Msvm_Synthetic3DDisplayController.OtherIdentifyingInfo
- Msvm_Synthetic3DDisplayController.IdentifyingDescriptions
- Msvm_Synthetic3DDisplayController.AdditionalAvailability
- Msvm_Synthetic3DDisplayController.MaxQuiesceTime
- Msvm_Synthetic3DDisplayController.TimeOfLastReset
- Msvm_Synthetic3DDisplayController.ProtocolSupported
- Msvm_Synthetic3DDisplayController.MaxNumberControlled
- Msvm_Synthetic3DDisplayController.ProtocolDescription
- Msvm_Synthetic3DDisplayController.VideoProcessor
- Msvm_Synthetic3DDisplayController.VideoMemoryType
- Msvm_Synthetic3DDisplayController.OtherVideoMemoryType
- Msvm_Synthetic3DDisplayController.NumberOfVideoPages
- Msvm_Synthetic3DDisplayController.MaxMemorySupported
- Msvm_Synthetic3DDisplayController.AcceleratorCapabilities
- Msvm_Synthetic3DDisplayController.CapabilityDescriptions
- Msvm_Synthetic3DDisplayController.OtherVideoArchitecture
- Msvm_Synthetic3DDisplayController.VideoArchitecture
- Msvm_Synthetic3DDisplayController.AllocatedGPU
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0cd102fe29cf34aa0930ca264c8820868da7daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760851"
---
# <a name="msvm_synthetic3ddisplaycontroller-class"></a><span data-ttu-id="fc82c-103">\_Classe Msvm Synthetic3DDisplayController</span><span class="sxs-lookup"><span data-stu-id="fc82c-103">Msvm\_Synthetic3DDisplayController class</span></span>

<span data-ttu-id="fc82c-104">Representa o controlador de vídeo sintético 3D atribuído a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fc82c-104">Represents the synthetic 3-D display controller that is assigned to a virtual machine.</span></span> <span data-ttu-id="fc82c-105">Essa classe é usada somente com máquinas virtuais que usam o RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="fc82c-105">This class is only used with virtual machines that use RemoteFX.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc82c-106">Ao adicionar um controlador de vídeo sintético 3D a uma máquina virtual, você deve desabilitar qualquer controlador de vídeo sintético ([**Msvm \_ SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) que esteja anexado a essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fc82c-106">When you add a synthetic 3-D display controller to a virtual machine, you must disable any synthetic display controller ([**Msvm\_SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) that is attached to that virtual machine.</span></span>

 

<span data-ttu-id="fc82c-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fc82c-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc82c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc82c-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Synthetic3DDisplayController : CIM_DisplayController
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
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 2048;
  uint32   MaxMemorySupported = 8388608;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
  string   AllocatedGPU;
};
```

## <a name="members"></a><span data-ttu-id="fc82c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="fc82c-109">Members</span></span>

<span data-ttu-id="fc82c-110">A classe **Msvm \_ Synthetic3DDisplayController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fc82c-110">The **Msvm\_Synthetic3DDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="fc82c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc82c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fc82c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc82c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fc82c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc82c-113">Methods</span></span>

<span data-ttu-id="fc82c-114">A classe **Msvm \_ Synthetic3DDisplayController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fc82c-114">The **Msvm\_Synthetic3DDisplayController** class has these methods.</span></span>



| <span data-ttu-id="fc82c-115">Método</span><span class="sxs-lookup"><span data-stu-id="fc82c-115">Method</span></span>                 | <span data-ttu-id="fc82c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc82c-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="fc82c-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="fc82c-117">**EnableDevice**</span></span>       | <span data-ttu-id="fc82c-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fc82c-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fc82c-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="fc82c-119">**OnlineDevice**</span></span>       | <span data-ttu-id="fc82c-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fc82c-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fc82c-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="fc82c-121">**QuiesceDevice**</span></span>      | <span data-ttu-id="fc82c-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fc82c-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fc82c-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="fc82c-123">**RequestStateChange**</span></span> | <span data-ttu-id="fc82c-124">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fc82c-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fc82c-125">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="fc82c-125">**Reset**</span></span>              | <span data-ttu-id="fc82c-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fc82c-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fc82c-127">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="fc82c-127">**RestoreProperties**</span></span>  | <span data-ttu-id="fc82c-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fc82c-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fc82c-129">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="fc82c-129">**SaveProperties**</span></span>     | <span data-ttu-id="fc82c-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fc82c-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fc82c-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="fc82c-131">**SetPowerState**</span></span>      | <span data-ttu-id="fc82c-132">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="fc82c-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fc82c-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc82c-133">Properties</span></span>

<span data-ttu-id="fc82c-134">A classe **Msvm \_ Synthetic3DDisplayController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fc82c-134">The **Msvm\_Synthetic3DDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc82c-135">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fc82c-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-136">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-138">Os elementos gráficos e as funcionalidades 3D do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc82c-138">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="fc82c-139">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc82c-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="fc82c-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-141">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-143">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="fc82c-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-144">**AllocatedGPU**</span><span class="sxs-lookup"><span data-stu-id="fc82c-144">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-147">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="fc82c-147">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-148">O identificador da GPU (unidade de processamento gráfico) física alocada a esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fc82c-148">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="fc82c-149">Essa propriedade só se aplica a máquinas virtuais que usam o RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="fc82c-149">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-150">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="fc82c-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-153">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="fc82c-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="fc82c-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-155">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-157">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="fc82c-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="fc82c-158">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fc82c-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-159">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fc82c-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-160">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-162">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos do acelerador de vídeo indicados na matriz da propriedade **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="fc82c-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="fc82c-163">Cada entrada dessa matriz está relacionada à entrada na matriz da propriedade **AcceleratorCapabilities** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="fc82c-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="fc82c-164">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc82c-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-165">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="fc82c-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-168">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="fc82c-168">A short description of the object.</span></span> <span data-ttu-id="fc82c-169">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-170">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="fc82c-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-171">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-173">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="fc82c-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="fc82c-174">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fc82c-175">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fc82c-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fc82c-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="fc82c-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="fc82c-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="fc82c-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="fc82c-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fc82c-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="fc82c-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fc82c-183">)</span><span class="sxs-lookup"><span data-stu-id="fc82c-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fc82c-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fc82c-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-185">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-187">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="fc82c-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="fc82c-188">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="fc82c-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-189">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fc82c-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-192">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="fc82c-192">A description of the object.</span></span> <span data-ttu-id="fc82c-193">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="fc82c-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-195">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-197">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="fc82c-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="fc82c-198">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fc82c-199">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fc82c-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="fc82c-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="fc82c-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="fc82c-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="fc82c-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="fc82c-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="fc82c-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fc82c-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="fc82c-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fc82c-208">)</span><span class="sxs-lookup"><span data-stu-id="fc82c-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fc82c-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="fc82c-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-212">O identificador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc82c-212">The device identifier.</span></span> <span data-ttu-id="fc82c-213">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="fc82c-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fc82c-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-217">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="fc82c-217">A display name for the object.</span></span> <span data-ttu-id="fc82c-218">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-219">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="fc82c-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-220">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-222">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="fc82c-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="fc82c-223">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="fc82c-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-224">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="fc82c-224">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-227">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="fc82c-227">The enabled and disabled states of an element.</span></span> <span data-ttu-id="fc82c-228">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="fc82c-228">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="fc82c-229">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado) ou 3 (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="fc82c-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to either 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-230">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="fc82c-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-231">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fc82c-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-233">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fc82c-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-237">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="fc82c-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-239">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-241">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="fc82c-241">The current health of the element.</span></span> <span data-ttu-id="fc82c-242">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subelementos.</span><span class="sxs-lookup"><span data-stu-id="fc82c-242">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="fc82c-243">Os valores possíveis são de 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="fc82c-243">The possible values are from 0 through 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="fc82c-244">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fc82c-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-246">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-248">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fc82c-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fc82c-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-250">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fc82c-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-252">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-252">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="fc82c-253">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-253">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-254">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fc82c-254">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-257">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="fc82c-257">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-258">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="fc82c-258">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fc82c-259">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-259">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-260">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fc82c-260">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-261">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc82c-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-263">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-264">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="fc82c-264">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-265">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc82c-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-267">A quantidade máxima de memória com suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="fc82c-267">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="fc82c-268">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc82c-268">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-269">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="fc82c-269">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-270">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc82c-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-272">O número máximo de entidades diretamente endereçáveis que são suportadas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="fc82c-272">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="fc82c-273">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="fc82c-273">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="fc82c-274">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="fc82c-274">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="fc82c-275">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="fc82c-275">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-276">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="fc82c-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-277">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc82c-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-279">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-279">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-280">**Nome**</span><span class="sxs-lookup"><span data-stu-id="fc82c-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-281">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-283">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="fc82c-283">The label by which the object is known.</span></span> <span data-ttu-id="fc82c-284">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-285">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="fc82c-285">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-286">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc82c-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-288">O número de páginas de vídeo com suporte dadas as resoluções atuais e a memória disponível.</span><span class="sxs-lookup"><span data-stu-id="fc82c-288">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="fc82c-289">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc82c-289">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-290">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="fc82c-290">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-291">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-293">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="fc82c-293">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="fc82c-294">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-294">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fc82c-295">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fc82c-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fc82c-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="fc82c-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="fc82c-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="fc82c-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="fc82c-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="fc82c-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="fc82c-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="fc82c-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="fc82c-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="fc82c-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="fc82c-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="fc82c-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="fc82c-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="fc82c-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="fc82c-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="fc82c-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="fc82c-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fc82c-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="fc82c-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fc82c-315">)</span><span class="sxs-lookup"><span data-stu-id="fc82c-315">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fc82c-316">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="fc82c-316">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-317">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-317">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-319">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="fc82c-319">The current statuses of the object.</span></span> <span data-ttu-id="fc82c-320">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-321">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="fc82c-321">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-324">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="fc82c-324">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="fc82c-325">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="fc82c-325">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="fc82c-326">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fc82c-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-327">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="fc82c-327">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-328">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-330">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fc82c-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-331">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="fc82c-331">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-332">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-334">Uma cadeia de caracteres que descreve o tipo de arquitetura de vídeo quando a propriedade **VideoArchitecture** é 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="fc82c-334">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="fc82c-335">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc82c-335">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-336">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="fc82c-336">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-339">O tipo de memória de vídeo quando a propriedade **VideoMemoryType** da instância é 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="fc82c-339">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="fc82c-340">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc82c-340">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-341">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fc82c-341">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-342">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-342">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-344">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-345">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="fc82c-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-346">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fc82c-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-348">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-349">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="fc82c-349">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-350">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc82c-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-352">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-353">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="fc82c-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-354">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-356">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="fc82c-356">Provides high level status information.</span></span> <span data-ttu-id="fc82c-357">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="fc82c-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="fc82c-358">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fc82c-359">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fc82c-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fc82c-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="fc82c-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="fc82c-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="fc82c-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fc82c-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="fc82c-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fc82c-366">)</span><span class="sxs-lookup"><span data-stu-id="fc82c-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fc82c-367">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="fc82c-367">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-368">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-370">Uma cadeia de caracteres que fornece mais informações relacionadas ao protocolo suportado pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="fc82c-370">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="fc82c-371">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="fc82c-371">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-372">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="fc82c-372">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-373">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-375">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="fc82c-375">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="fc82c-376">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="fc82c-376">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-377">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="fc82c-377">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-378">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-378">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-379">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-380">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="fc82c-380">The last requested or desired state for the element.</span></span> <span data-ttu-id="fc82c-381">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="fc82c-381">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="fc82c-382">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="fc82c-382">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="fc82c-383">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte A **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="fc82c-383">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="fc82c-384">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="fc82c-384">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="fc82c-385">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement** e é sempre definida como 2 (habilitado), 3 (desabilitado) ou 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="fc82c-385">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-386">**Status**</span><span class="sxs-lookup"><span data-stu-id="fc82c-386">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-387">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-389">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-390">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fc82c-390">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-391">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-391">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-393">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="fc82c-393">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="fc82c-394">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fc82c-394">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-395">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="fc82c-395">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-396">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-398">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-399">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fc82c-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-400">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-401">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-402">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="fc82c-402">The scoping system's creation class name.</span></span> <span data-ttu-id="fc82c-403">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="fc82c-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="fc82c-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-405">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-406">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-407">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="fc82c-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="fc82c-408">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="fc82c-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-409">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="fc82c-409">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-410">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fc82c-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-411">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-412">A última vez em que a máquina virtual estava ligada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-412">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="fc82c-413">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="fc82c-413">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-414">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="fc82c-414">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-415">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fc82c-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-417">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="fc82c-417">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="fc82c-418">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc82c-418">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-419">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="fc82c-419">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-420">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc82c-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-422">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-423">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="fc82c-423">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-424">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-426">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="fc82c-426">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="fc82c-427">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fc82c-427">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-428">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="fc82c-428">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-429">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-431">Especifica a arquitetura de vídeo do controlador de vídeo usada para gerar o sinal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc82c-431">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="fc82c-432">Normalmente, um processador de vídeo dedicado gera o sinal de vídeo de acordo com a arquitetura especificada.</span><span class="sxs-lookup"><span data-stu-id="fc82c-432">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="fc82c-433">É um indicador da capacidade de resolução máxima do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc82c-433">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="fc82c-434">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc82c-434">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="fc82c-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fc82c-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="fc82c-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="fc82c-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="fc82c-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="fc82c-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="fc82c-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="fc82c-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="fc82c-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="fc82c-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="fc82c-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="fc82c-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Buffer de quadro linear** (11)</span><span class="sxs-lookup"><span data-stu-id="fc82c-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="fc82c-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fc82c-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="fc82c-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fc82c-450">)</span><span class="sxs-lookup"><span data-stu-id="fc82c-450">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fc82c-451">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="fc82c-451">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-452">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc82c-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-454">O tipo de memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc82c-454">The type of video memory.</span></span> <span data-ttu-id="fc82c-455">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc82c-455">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fc82c-456">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="fc82c-456">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc82c-457">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc82c-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc82c-458">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc82c-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc82c-459">Uma cadeia de caracteres que descreve o controlador/processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc82c-459">A string that describes the video processor/controller.</span></span> <span data-ttu-id="fc82c-460">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fc82c-460">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc82c-461">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc82c-461">Requirements</span></span>



| <span data-ttu-id="fc82c-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc82c-462">Requirement</span></span> | <span data-ttu-id="fc82c-463">Valor</span><span class="sxs-lookup"><span data-stu-id="fc82c-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc82c-464">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc82c-464">Minimum supported client</span></span><br/> | <span data-ttu-id="fc82c-465">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fc82c-465">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="fc82c-466">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc82c-466">Minimum supported server</span></span><br/> | <span data-ttu-id="fc82c-467">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="fc82c-467">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fc82c-468">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc82c-468">Namespace</span></span><br/>                | <span data-ttu-id="fc82c-469">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fc82c-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fc82c-470">MOF</span><span class="sxs-lookup"><span data-stu-id="fc82c-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc82c-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc82c-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc82c-472">DLL</span><span class="sxs-lookup"><span data-stu-id="fc82c-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc82c-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc82c-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc82c-474">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc82c-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc82c-475">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="fc82c-475">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> </dl>

 

