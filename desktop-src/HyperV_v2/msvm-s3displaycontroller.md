---
description: Representa o estado do controlador S3 emulado que está presente em cada configuração de máquina virtual.
ms.assetid: 194E0195-1AFF-4298-8000-2249495818C2
title: Classe Msvm_S3DisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_S3DisplayController
- Msvm_S3DisplayController.SetPowerState
- Msvm_S3DisplayController.EnableDevice
- Msvm_S3DisplayController.OnlineDevice
- Msvm_S3DisplayController.QuiesceDevice
- Msvm_S3DisplayController.SaveProperties
- Msvm_S3DisplayController.RestoreProperties
- Msvm_S3DisplayController.InstanceID
- Msvm_S3DisplayController.Caption
- Msvm_S3DisplayController.Description
- Msvm_S3DisplayController.ElementName
- Msvm_S3DisplayController.InstallDate
- Msvm_S3DisplayController.Name
- Msvm_S3DisplayController.OperationalStatus
- Msvm_S3DisplayController.StatusDescriptions
- Msvm_S3DisplayController.Status
- Msvm_S3DisplayController.HealthState
- Msvm_S3DisplayController.CommunicationStatus
- Msvm_S3DisplayController.DetailedStatus
- Msvm_S3DisplayController.OperatingStatus
- Msvm_S3DisplayController.PrimaryStatus
- Msvm_S3DisplayController.EnabledState
- Msvm_S3DisplayController.OtherEnabledState
- Msvm_S3DisplayController.RequestedState
- Msvm_S3DisplayController.EnabledDefault
- Msvm_S3DisplayController.TimeOfLastStateChange
- Msvm_S3DisplayController.AvailableRequestedStates
- Msvm_S3DisplayController.TransitioningToState
- Msvm_S3DisplayController.SystemCreationClassName
- Msvm_S3DisplayController.SystemName
- Msvm_S3DisplayController.CreationClassName
- Msvm_S3DisplayController.DeviceID
- Msvm_S3DisplayController.PowerManagementSupported
- Msvm_S3DisplayController.PowerManagementCapabilities
- Msvm_S3DisplayController.Availability
- Msvm_S3DisplayController.StatusInfo
- Msvm_S3DisplayController.LastErrorCode
- Msvm_S3DisplayController.ErrorDescription
- Msvm_S3DisplayController.ErrorCleared
- Msvm_S3DisplayController.OtherIdentifyingInfo
- Msvm_S3DisplayController.PowerOnHours
- Msvm_S3DisplayController.TotalPowerOnHours
- Msvm_S3DisplayController.IdentifyingDescriptions
- Msvm_S3DisplayController.AdditionalAvailability
- Msvm_S3DisplayController.MaxQuiesceTime
- Msvm_S3DisplayController.TimeOfLastReset
- Msvm_S3DisplayController.ProtocolSupported
- Msvm_S3DisplayController.MaxNumberControlled
- Msvm_S3DisplayController.ProtocolDescription
- Msvm_S3DisplayController.VideoProcessor
- Msvm_S3DisplayController.VideoMemoryType
- Msvm_S3DisplayController.OtherVideoMemoryType
- Msvm_S3DisplayController.NumberOfVideoPages
- Msvm_S3DisplayController.MaxMemorySupported
- Msvm_S3DisplayController.AcceleratorCapabilities
- Msvm_S3DisplayController.CapabilityDescriptions
- Msvm_S3DisplayController.OtherVideoArchitecture
- Msvm_S3DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a4195ff8947bf92d8e4af3a95df320ed950ab21e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091845"
---
# <a name="msvm_s3displaycontroller-class"></a><span data-ttu-id="a22a8-103">\_Classe Msvm S3DisplayController</span><span class="sxs-lookup"><span data-stu-id="a22a8-103">Msvm\_S3DisplayController class</span></span>

<span data-ttu-id="a22a8-104">Representa o estado do controlador S3 emulado que está presente em cada configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a22a8-104">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="a22a8-105">Somente um controlador de vídeo pode estar ativo em uma máquina virtual a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="a22a8-105">Only one display controller can be active in a virtual machine at any time.</span></span>

> [!Note]  
> <span data-ttu-id="a22a8-106">Essa classe se aplica somente a máquinas virtuais de geração 1.</span><span class="sxs-lookup"><span data-stu-id="a22a8-106">This class only applies to generation 1 virtual machines.</span></span>

 

<span data-ttu-id="a22a8-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a22a8-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22a8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a22a8-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_S3DisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Emulated Display Controller";
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
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_S3DisplayController";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Virtual S3 Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 32768;
  uint32   MaxMemorySupported = 134217728;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="a22a8-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a22a8-109">Members</span></span>

<span data-ttu-id="a22a8-110">A classe **Msvm \_ S3DisplayController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a22a8-110">The **Msvm\_S3DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="a22a8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a22a8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a22a8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a22a8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a22a8-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a22a8-113">Methods</span></span>

<span data-ttu-id="a22a8-114">A classe **Msvm \_ S3DisplayController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a22a8-114">The **Msvm\_S3DisplayController** class has these methods.</span></span>



| <span data-ttu-id="a22a8-115">Método</span><span class="sxs-lookup"><span data-stu-id="a22a8-115">Method</span></span>                                                                    | <span data-ttu-id="a22a8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a22a8-116">Description</span></span>                              |
|:--------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="a22a8-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="a22a8-117">**EnableDevice**</span></span>                                                          | <span data-ttu-id="a22a8-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a22a8-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a22a8-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="a22a8-119">**OnlineDevice**</span></span>                                                          | <span data-ttu-id="a22a8-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a22a8-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a22a8-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="a22a8-121">**QuiesceDevice**</span></span>                                                         | <span data-ttu-id="a22a8-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a22a8-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="a22a8-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a22a8-123">**RequestStateChange**</span></span>](msvm-s3displaycontroller-requeststatechange.md) | <span data-ttu-id="a22a8-124">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="a22a8-124">Requests a state change.</span></span> <br/>     |
| [<span data-ttu-id="a22a8-125">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="a22a8-125">**Reset**</span></span>](msvm-s3displaycontroller-reset.md)                           | <span data-ttu-id="a22a8-126">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="a22a8-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="a22a8-127">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="a22a8-127">**RestoreProperties**</span></span>                                                     | <span data-ttu-id="a22a8-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a22a8-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a22a8-129">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="a22a8-129">**SaveProperties**</span></span>                                                        | <span data-ttu-id="a22a8-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a22a8-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="a22a8-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a22a8-131">**SetPowerState**</span></span>                                                         | <span data-ttu-id="a22a8-132">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="a22a8-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a22a8-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a22a8-133">Properties</span></span>

<span data-ttu-id="a22a8-134">A classe **Msvm \_ S3DisplayController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a22a8-134">The **Msvm\_S3DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a22a8-135">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a22a8-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-136">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-138">Os recursos gráficos e 3D do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a22a8-138">The graphics and 3D capabilities of the display controller.</span></span> <span data-ttu-id="a22a8-139">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="a22a8-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-141">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-143">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a22a8-143">Any additional availability and status of the device.</span></span> <span data-ttu-id="a22a8-144">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a22a8-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-145">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="a22a8-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-146">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-148">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a22a8-148">The primary availability and status of the device.</span></span> <span data-ttu-id="a22a8-149">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a22a8-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="a22a8-150">Valor</span><span class="sxs-lookup"><span data-stu-id="a22a8-150">Value</span></span>                                                                        | <span data-ttu-id="a22a8-151">Significado</span><span class="sxs-lookup"><span data-stu-id="a22a8-151">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a22a8-152"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a22a8-152"><dt>6</dt></span></span> </dl> | <span data-ttu-id="a22a8-153">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="a22a8-153">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a22a8-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="a22a8-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-155">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-157">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a22a8-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="a22a8-158">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a22a8-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-159">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a22a8-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-160">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-162">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos do acelerador de vídeo indicados na matriz **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a22a8-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="a22a8-163">Cada entrada dessa matriz está relacionada à entrada na matriz **AcceleratorCapabilities** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="a22a8-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span> <span data-ttu-id="a22a8-164">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-165">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a22a8-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-168">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a22a8-168">A short description of the object.</span></span> <span data-ttu-id="a22a8-169">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a22a8-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-170">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a22a8-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-171">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-173">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="a22a8-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a22a8-174">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a22a8-175">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a22a8-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a22a8-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a22a8-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="a22a8-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="a22a8-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="a22a8-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="a22a8-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a22a8-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a22a8-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a22a8-183">)</span><span class="sxs-lookup"><span data-stu-id="a22a8-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a22a8-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a22a8-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-185">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-187">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a22a8-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a22a8-188">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Msvm \_ S3DisplayController".</span><span class="sxs-lookup"><span data-stu-id="a22a8-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_S3DisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-189">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a22a8-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-192">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="a22a8-192">A description of the object.</span></span> <span data-ttu-id="a22a8-193">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a22a8-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a22a8-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-195">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-197">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="a22a8-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a22a8-198">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a22a8-199">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a22a8-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a22a8-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="a22a8-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="a22a8-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="a22a8-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="a22a8-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="a22a8-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="a22a8-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a22a8-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a22a8-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a22a8-208">)</span><span class="sxs-lookup"><span data-stu-id="a22a8-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a22a8-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a22a8-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-212">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a22a8-212">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="a22a8-213">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a22a8-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a22a8-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-215">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-217">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="a22a8-217">A display name for the object.</span></span> <span data-ttu-id="a22a8-218">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a22a8-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-219">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="a22a8-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-220">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-222">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="a22a8-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="a22a8-223">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a22a8-224">Valor</span><span class="sxs-lookup"><span data-stu-id="a22a8-224">Value</span></span>                                                                        | <span data-ttu-id="a22a8-225">Significado</span><span class="sxs-lookup"><span data-stu-id="a22a8-225">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="a22a8-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a22a8-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a22a8-227">habilitado</span><span class="sxs-lookup"><span data-stu-id="a22a8-227">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="a22a8-228"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a22a8-228"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a22a8-229">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="a22a8-229">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a22a8-230">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a22a8-230">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-233">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="a22a8-233">The enabled and disabled states of an element.</span></span> <span data-ttu-id="a22a8-234">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="a22a8-234">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="a22a8-235">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado) ou 3 (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="a22a8-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="a22a8-236">Valor</span><span class="sxs-lookup"><span data-stu-id="a22a8-236">Value</span></span>                                                                        | <span data-ttu-id="a22a8-237">Significado</span><span class="sxs-lookup"><span data-stu-id="a22a8-237">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="a22a8-238"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a22a8-238"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a22a8-239">habilitado</span><span class="sxs-lookup"><span data-stu-id="a22a8-239">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="a22a8-240"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a22a8-240"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a22a8-241">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="a22a8-241">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a22a8-242">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a22a8-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-243">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a22a8-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-245">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="a22a8-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="a22a8-246">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a22a8-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-250">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="a22a8-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="a22a8-251">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a22a8-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-253">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-255">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="a22a8-255">The current health of the element.</span></span> <span data-ttu-id="a22a8-256">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a22a8-256">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a22a8-257">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="a22a8-257">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a22a8-258">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a22a8-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="a22a8-259">Valor</span><span class="sxs-lookup"><span data-stu-id="a22a8-259">Value</span></span>                                                                        | <span data-ttu-id="a22a8-260">Significado</span><span class="sxs-lookup"><span data-stu-id="a22a8-260">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="a22a8-261"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a22a8-261"><dt>5</dt></span></span> </dl> | <span data-ttu-id="a22a8-262">OK</span><span class="sxs-lookup"><span data-stu-id="a22a8-262">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a22a8-263">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a22a8-263">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-264">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-264">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-266">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="a22a8-266">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="a22a8-267">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a22a8-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a22a8-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-269">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a22a8-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-271">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="a22a8-272">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a22a8-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a22a8-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-274">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-276">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="a22a8-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-277">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="a22a8-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a22a8-278">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a22a8-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-279">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a22a8-279">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-280">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a22a8-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-282">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a22a8-282">The last error code reported by the logical device.</span></span> <span data-ttu-id="a22a8-283">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-284">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="a22a8-284">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-285">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a22a8-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-287">A quantidade máxima de memória com suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="a22a8-287">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="a22a8-288">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-288">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-289">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="a22a8-289">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-290">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a22a8-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-292">O número máximo de entidades diretamente endereçáveis que são suportadas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="a22a8-292">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="a22a8-293">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="a22a8-293">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="a22a8-294">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="a22a8-294">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="a22a8-295">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="a22a8-295">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-296">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="a22a8-296">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-297">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a22a8-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-299">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="a22a8-299">This property has been deprecated.</span></span> <span data-ttu-id="a22a8-300">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a22a8-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-301">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a22a8-301">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-302">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-304">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="a22a8-304">The label by which the object is known.</span></span> <span data-ttu-id="a22a8-305">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a22a8-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-306">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="a22a8-306">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-307">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a22a8-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-309">O número de páginas de vídeo com suporte dadas as resoluções atuais e a memória disponível.</span><span class="sxs-lookup"><span data-stu-id="a22a8-309">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="a22a8-310">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-310">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-311">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a22a8-311">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-312">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-312">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-314">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="a22a8-314">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a22a8-315">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-315">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a22a8-316">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a22a8-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a22a8-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a22a8-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="a22a8-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="a22a8-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="a22a8-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="a22a8-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="a22a8-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="a22a8-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="a22a8-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="a22a8-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="a22a8-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="a22a8-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="a22a8-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="a22a8-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="a22a8-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="a22a8-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="a22a8-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="a22a8-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a22a8-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a22a8-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a22a8-336">)</span><span class="sxs-lookup"><span data-stu-id="a22a8-336">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a22a8-337">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a22a8-337">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-338">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-340">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="a22a8-340">The current statuses of the object.</span></span> <span data-ttu-id="a22a8-341">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="a22a8-341">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-342">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a22a8-342">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-343">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-345">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="a22a8-345">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="a22a8-346">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="a22a8-346">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="a22a8-347">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a22a8-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a22a8-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-349">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-351">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a22a8-351">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="a22a8-352">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a22a8-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-353">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="a22a8-353">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-354">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-356">Uma cadeia de caracteres que descreve o tipo de arquitetura de vídeo quando a propriedade **VideoArchitecture** é 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="a22a8-356">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="a22a8-357">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-357">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-358">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="a22a8-358">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-359">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-360">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-361">O tipo de memória de vídeo quando a propriedade **VideoMemoryType** da instância é 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="a22a8-361">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="a22a8-362">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-362">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-363">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a22a8-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-364">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-366">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a22a8-366">The power management capabilities of the device.</span></span> <span data-ttu-id="a22a8-367">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-368">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a22a8-368">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-369">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a22a8-369">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-371">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="a22a8-371">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="a22a8-372">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-373">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="a22a8-373">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-374">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a22a8-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-376">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="a22a8-376">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="a22a8-377">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-377">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-378">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a22a8-378">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-379">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-381">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="a22a8-381">Provides high level status information.</span></span> <span data-ttu-id="a22a8-382">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a22a8-382">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a22a8-383">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a22a8-384">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a22a8-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a22a8-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a22a8-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-386"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="a22a8-386"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="a22a8-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="a22a8-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a22a8-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a22a8-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a22a8-391">)</span><span class="sxs-lookup"><span data-stu-id="a22a8-391">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a22a8-392">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="a22a8-392">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-393">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-395">Uma cadeia de caracteres que fornece mais informações relacionadas ao protocolo suportado pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="a22a8-395">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="a22a8-396">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="a22a8-396">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-397">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="a22a8-397">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-398">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-400">O protocolo usado pelo controlador para acessar dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="a22a8-400">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="a22a8-401">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="a22a8-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-402">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a22a8-402">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-403">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-405">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="a22a8-405">The last requested or desired state for the element.</span></span> <span data-ttu-id="a22a8-406">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="a22a8-406">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="a22a8-407">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="a22a8-407">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="a22a8-408">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-408">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a22a8-409">Valor</span><span class="sxs-lookup"><span data-stu-id="a22a8-409">Value</span></span>                                                                         | <span data-ttu-id="a22a8-410">Significado</span><span class="sxs-lookup"><span data-stu-id="a22a8-410">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="a22a8-411"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a22a8-411"><dt>12</dt></span></span> </dl> | <span data-ttu-id="a22a8-412">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="a22a8-412">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a22a8-413">**Status**</span><span class="sxs-lookup"><span data-stu-id="a22a8-413">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-414">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-416">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a22a8-416">The current status of the object.</span></span> <span data-ttu-id="a22a8-417">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-418">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a22a8-418">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-419">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-419">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-421">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a22a8-421">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a22a8-422">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="a22a8-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-423">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a22a8-423">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-424">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-426">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a22a8-426">The current state of the logical device.</span></span> <span data-ttu-id="a22a8-427">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-428">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a22a8-428">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-429">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-431">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="a22a8-431">The scoping system's creation class name.</span></span> <span data-ttu-id="a22a8-432">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a22a8-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a22a8-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-436">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="a22a8-436">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="a22a8-437">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="a22a8-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-438">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="a22a8-438">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-439">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a22a8-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-441">A última vez em que a máquina virtual estava ligada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-441">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="a22a8-442">Essa propriedade é herdada [**do \_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="a22a8-442">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-443">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="a22a8-443">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-444">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a22a8-444">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-445">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-446">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="a22a8-446">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a22a8-447">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-447">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-448">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="a22a8-448">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-449">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a22a8-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-451">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="a22a8-451">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="a22a8-452">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-453">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="a22a8-453">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-454">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-456">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="a22a8-456">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a22a8-457">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a22a8-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-458">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="a22a8-458">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-459">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-461">Especifica a arquitetura de vídeo do controlador de vídeo usada para gerar o sinal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a22a8-461">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="a22a8-462">Normalmente, um processador de vídeo dedicado gera o sinal de vídeo de acordo com a arquitetura especificada.</span><span class="sxs-lookup"><span data-stu-id="a22a8-462">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="a22a8-463">É um indicador da capacidade de resolução máxima do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a22a8-463">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="a22a8-464">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-464">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a22a8-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a22a8-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a22a8-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="a22a8-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="a22a8-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="a22a8-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="a22a8-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="a22a8-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="a22a8-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="a22a8-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="a22a8-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="a22a8-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Buffer de quadro linear** (11)</span><span class="sxs-lookup"><span data-stu-id="a22a8-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="a22a8-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a22a8-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="a22a8-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a22a8-480">)</span><span class="sxs-lookup"><span data-stu-id="a22a8-480">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a22a8-481">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="a22a8-481">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-482">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22a8-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-483">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-484">O tipo de memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a22a8-484">The type of video memory.</span></span> <span data-ttu-id="a22a8-485">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-485">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a22a8-486">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="a22a8-486">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22a8-487">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a22a8-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22a8-488">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a22a8-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22a8-489">Uma cadeia de caracteres que descreve o controlador/processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a22a8-489">A string that describes the video processor/controller.</span></span> <span data-ttu-id="a22a8-490">Essa propriedade é herdada do [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a22a8-490">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a22a8-491">Comentários</span><span class="sxs-lookup"><span data-stu-id="a22a8-491">Remarks</span></span>

<span data-ttu-id="a22a8-492">O acesso à classe **Msvm \_ S3DisplayController** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="a22a8-492">Access to the **Msvm\_S3DisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a22a8-493">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a22a8-493">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a22a8-494">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a22a8-494">Requirements</span></span>



| <span data-ttu-id="a22a8-495">Requisito</span><span class="sxs-lookup"><span data-stu-id="a22a8-495">Requirement</span></span> | <span data-ttu-id="a22a8-496">Valor</span><span class="sxs-lookup"><span data-stu-id="a22a8-496">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a22a8-497">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a22a8-497">Minimum supported client</span></span><br/> | <span data-ttu-id="a22a8-498">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a22a8-498">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a22a8-499">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a22a8-499">Minimum supported server</span></span><br/> | <span data-ttu-id="a22a8-500">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a22a8-500">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a22a8-501">Namespace</span><span class="sxs-lookup"><span data-stu-id="a22a8-501">Namespace</span></span><br/>                | <span data-ttu-id="a22a8-502">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a22a8-502">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a22a8-503">MOF</span><span class="sxs-lookup"><span data-stu-id="a22a8-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a22a8-504"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a22a8-504"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a22a8-505">DLL</span><span class="sxs-lookup"><span data-stu-id="a22a8-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a22a8-506"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a22a8-506"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a22a8-507">Confira também</span><span class="sxs-lookup"><span data-stu-id="a22a8-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22a8-508">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="a22a8-508">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="a22a8-509">[**\_DISPLAYCONTROLLER CIM**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a22a8-509">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a22a8-510">Classes de vídeo</span><span class="sxs-lookup"><span data-stu-id="a22a8-510">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

