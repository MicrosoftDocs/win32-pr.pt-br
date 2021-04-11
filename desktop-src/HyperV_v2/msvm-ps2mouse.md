---
description: Representa um dispositivo de mouse PS2.
ms.assetid: 5e02ec15-95e6-4d82-833e-a48ca117a890
title: Classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse
- Msvm_Ps2Mouse.SetPowerState
- Msvm_Ps2Mouse.EnableDevice
- Msvm_Ps2Mouse.OnlineDevice
- Msvm_Ps2Mouse.QuiesceDevice
- Msvm_Ps2Mouse.SaveProperties
- Msvm_Ps2Mouse.RestoreProperties
- Msvm_Ps2Mouse.InstanceID
- Msvm_Ps2Mouse.Caption
- Msvm_Ps2Mouse.Description
- Msvm_Ps2Mouse.ElementName
- Msvm_Ps2Mouse.InstallDate
- Msvm_Ps2Mouse.Name
- Msvm_Ps2Mouse.OperationalStatus
- Msvm_Ps2Mouse.StatusDescriptions
- Msvm_Ps2Mouse.Status
- Msvm_Ps2Mouse.HealthState
- Msvm_Ps2Mouse.CommunicationStatus
- Msvm_Ps2Mouse.DetailedStatus
- Msvm_Ps2Mouse.OperatingStatus
- Msvm_Ps2Mouse.PrimaryStatus
- Msvm_Ps2Mouse.EnabledState
- Msvm_Ps2Mouse.OtherEnabledState
- Msvm_Ps2Mouse.RequestedState
- Msvm_Ps2Mouse.EnabledDefault
- Msvm_Ps2Mouse.TimeOfLastStateChange
- Msvm_Ps2Mouse.AvailableRequestedStates
- Msvm_Ps2Mouse.TransitioningToState
- Msvm_Ps2Mouse.SystemCreationClassName
- Msvm_Ps2Mouse.SystemName
- Msvm_Ps2Mouse.CreationClassName
- Msvm_Ps2Mouse.DeviceID
- Msvm_Ps2Mouse.PowerManagementSupported
- Msvm_Ps2Mouse.PowerManagementCapabilities
- Msvm_Ps2Mouse.Availability
- Msvm_Ps2Mouse.StatusInfo
- Msvm_Ps2Mouse.LastErrorCode
- Msvm_Ps2Mouse.ErrorDescription
- Msvm_Ps2Mouse.ErrorCleared
- Msvm_Ps2Mouse.OtherIdentifyingInfo
- Msvm_Ps2Mouse.PowerOnHours
- Msvm_Ps2Mouse.TotalPowerOnHours
- Msvm_Ps2Mouse.IdentifyingDescriptions
- Msvm_Ps2Mouse.AdditionalAvailability
- Msvm_Ps2Mouse.MaxQuiesceTime
- Msvm_Ps2Mouse.IsLocked
- Msvm_Ps2Mouse.PointingType
- Msvm_Ps2Mouse.NumberOfButtons
- Msvm_Ps2Mouse.Handedness
- Msvm_Ps2Mouse.Resolution
- Msvm_Ps2Mouse.AbsoluteCoordinates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d25d168b85a79c5212afc719ce6ec83ca9780395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296804"
---
# <a name="msvm_ps2mouse-class"></a><span data-ttu-id="d98ff-103">\_Classe Msvm Ps2Mouse</span><span class="sxs-lookup"><span data-stu-id="d98ff-103">Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="d98ff-104">Representa um dispositivo de mouse PS2.</span><span class="sxs-lookup"><span data-stu-id="d98ff-104">Represents a PS2 mouse device.</span></span> <span data-ttu-id="d98ff-105">As instâncias dessa classe são dispositivos lógicos que estão sempre presentes em uma máquina virtual e, portanto, não são alocados por meio de um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="d98ff-105">Instances of this class are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="d98ff-106">Uma instância está sempre presente em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d98ff-106">One instance is always present in a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="d98ff-107">Essa classe não está disponível para máquinas virtuais de geração 2.</span><span class="sxs-lookup"><span data-stu-id="d98ff-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="d98ff-108">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d98ff-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d98ff-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d98ff-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Ps2Mouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Emulated Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
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
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_PS2Mouse";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = False;
};
```

## <a name="members"></a><span data-ttu-id="d98ff-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d98ff-110">Members</span></span>

<span data-ttu-id="d98ff-111">A classe **Msvm \_ Ps2Mouse** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d98ff-111">The **Msvm\_Ps2Mouse** class has these types of members:</span></span>

-   [<span data-ttu-id="d98ff-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d98ff-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d98ff-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d98ff-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d98ff-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d98ff-114">Methods</span></span>

<span data-ttu-id="d98ff-115">A classe **Msvm \_ Ps2Mouse** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d98ff-115">The **Msvm\_Ps2Mouse** class has these methods.</span></span>



| <span data-ttu-id="d98ff-116">Método</span><span class="sxs-lookup"><span data-stu-id="d98ff-116">Method</span></span>                                                           | <span data-ttu-id="d98ff-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d98ff-117">Description</span></span>                                                                                           |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d98ff-118">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="d98ff-118">**ClickButton**</span></span>](clickbutton-msvm-ps2mouse.md)                 | <span data-ttu-id="d98ff-119">Simula um clique de botão, uma sequência para baixo, no botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d98ff-119">Simulates a button click, a down-up sequence, on the specified device button.</span></span><br/>              |
| <span data-ttu-id="d98ff-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d98ff-120">**EnableDevice**</span></span>                                                 | <span data-ttu-id="d98ff-121">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d98ff-121">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="d98ff-122">**Getbuttonstate**</span><span class="sxs-lookup"><span data-stu-id="d98ff-122">**GetButtonState**</span></span>](getbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="d98ff-123">Recupera o estado atual do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d98ff-123">Retrieves the current state of the specified device button.</span></span><br/>                                |
| <span data-ttu-id="d98ff-124">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="d98ff-124">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="d98ff-125">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d98ff-125">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="d98ff-126">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="d98ff-126">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="d98ff-127">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d98ff-127">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="d98ff-128">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d98ff-128">**RequestStateChange**</span></span>](msvm-ps2mouse-requeststatechange.md)   | <span data-ttu-id="d98ff-129">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="d98ff-129">Requests a state change.</span></span><br/>                                                                   |
| [<span data-ttu-id="d98ff-130">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="d98ff-130">**Reset**</span></span>](msvm-ps2mouse-reset.md)                             | <span data-ttu-id="d98ff-131">Redefine o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d98ff-131">Resets the device.</span></span><br/>                                                                         |
| <span data-ttu-id="d98ff-132">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="d98ff-132">**RestoreProperties**</span></span>                                            | <span data-ttu-id="d98ff-133">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d98ff-133">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="d98ff-134">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="d98ff-134">**SaveProperties**</span></span>                                               | <span data-ttu-id="d98ff-135">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d98ff-135">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="d98ff-136">**Setbuttonstate**</span><span class="sxs-lookup"><span data-stu-id="d98ff-136">**SetButtonState**</span></span>](setbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="d98ff-137">Define o estado atual do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d98ff-137">Sets the current state of the specified device button.</span></span><br/>                                     |
| <span data-ttu-id="d98ff-138">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d98ff-138">**SetPowerState**</span></span>                                                | <span data-ttu-id="d98ff-139">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="d98ff-139">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="d98ff-140">**SetRelativePosition**</span><span class="sxs-lookup"><span data-stu-id="d98ff-140">**SetRelativePosition**</span></span>](setrelativeposition-msvm-ps2mouse.md) | <span data-ttu-id="d98ff-141">Desloca a posição do ponteiro do mouse pelos deltas horizontais e verticais especificados.</span><span class="sxs-lookup"><span data-stu-id="d98ff-141">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span><br/> |
| [<span data-ttu-id="d98ff-142">**SetScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="d98ff-142">**SetScrollPosition**</span></span>](setscrollposition-msvm-ps2mouse.md)     | <span data-ttu-id="d98ff-143">Ajusta a coordenada z do controle de roda do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="d98ff-143">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="d98ff-144">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d98ff-144">Properties</span></span>

<span data-ttu-id="d98ff-145">A classe **Msvm \_ Ps2Mouse** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d98ff-145">The **Msvm\_Ps2Mouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d98ff-146">**AbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="d98ff-146">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-147">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d98ff-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-149">Indica se o dispositivo opera em coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="d98ff-149">Indicates whether the device operates on absolute coordinates.</span></span> <span data-ttu-id="d98ff-150">Se não estiver definido, as coordenadas do dispositivo serão relativas.</span><span class="sxs-lookup"><span data-stu-id="d98ff-150">If not set, the device's coordinates are relative.</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-151">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="d98ff-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-152">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-154">Qualquer disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="d98ff-154">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="d98ff-155">A propriedade de **disponibilidade** denota o status primário e a disponibilidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d98ff-155">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="d98ff-156">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-156">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="d98ff-157">Valor</span><span class="sxs-lookup"><span data-stu-id="d98ff-157">Value</span></span>                                                                        | <span data-ttu-id="d98ff-158">Significado</span><span class="sxs-lookup"><span data-stu-id="d98ff-158">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="d98ff-159"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d98ff-159"><dt>6</dt></span></span> </dl> | <span data-ttu-id="d98ff-160">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="d98ff-160">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d98ff-161">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="d98ff-161">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-162">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-164">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d98ff-164">The primary availability and status of the device.</span></span> <span data-ttu-id="d98ff-165">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-165">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="d98ff-166">Valor</span><span class="sxs-lookup"><span data-stu-id="d98ff-166">Value</span></span>                                                                        | <span data-ttu-id="d98ff-167">Significado</span><span class="sxs-lookup"><span data-stu-id="d98ff-167">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="d98ff-168"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d98ff-168"><dt>6</dt></span></span> </dl> | <span data-ttu-id="d98ff-169">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="d98ff-169">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d98ff-170">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d98ff-170">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-171">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-171">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-173">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d98ff-173">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d98ff-174">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d98ff-174">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-175">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d98ff-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-178">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d98ff-178">A short description of the object.</span></span> <span data-ttu-id="d98ff-179">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d98ff-179">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-180">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d98ff-180">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-181">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-183">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="d98ff-183">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d98ff-184">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-184">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d98ff-185">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d98ff-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d98ff-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d98ff-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="d98ff-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="d98ff-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="d98ff-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="d98ff-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d98ff-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d98ff-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d98ff-193">)</span><span class="sxs-lookup"><span data-stu-id="d98ff-193">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d98ff-194">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d98ff-194">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-197">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d98ff-197">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-198">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="d98ff-198">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d98ff-199">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="d98ff-199">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="d98ff-200">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-201">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d98ff-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-204">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="d98ff-204">A description of the object.</span></span> <span data-ttu-id="d98ff-205">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d98ff-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d98ff-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-207">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-209">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="d98ff-209">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d98ff-210">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d98ff-211">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d98ff-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d98ff-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="d98ff-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="d98ff-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="d98ff-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="d98ff-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="d98ff-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="d98ff-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d98ff-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d98ff-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d98ff-220">)</span><span class="sxs-lookup"><span data-stu-id="d98ff-220">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d98ff-221">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d98ff-221">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-224">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d98ff-224">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-225">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d98ff-225">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="d98ff-226">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="d98ff-226">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-227">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d98ff-227">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-230">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="d98ff-230">A display name for the object.</span></span> <span data-ttu-id="d98ff-231">Essa propriedade permite que cada instância defina um nome de exibição além de suas propriedades de chave, dados de identidade e informações de descrição.</span><span class="sxs-lookup"><span data-stu-id="d98ff-231">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="d98ff-232">A propriedade [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) da classe **CIM \_ ManagedSystemElement** também é definida como um nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="d98ff-232">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="d98ff-233">Mas, muitas vezes, é uma subclasse para ser uma chave.</span><span class="sxs-lookup"><span data-stu-id="d98ff-233">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="d98ff-234">Não é razoável que a mesma propriedade possa transmitir a identidade e um nome de exibição, sem inconsistências.</span><span class="sxs-lookup"><span data-stu-id="d98ff-234">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="d98ff-235">Onde [**Name**](msvm-keyboard.md) existe e não é uma chave (como para instâncias de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), as mesmas informações podem estar presentes nas propriedades **Name** e **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="d98ff-235">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="d98ff-236">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "mouse".</span><span class="sxs-lookup"><span data-stu-id="d98ff-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Mouse".</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-237">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d98ff-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-238">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-240">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="d98ff-240">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="d98ff-241">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d98ff-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d98ff-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-243">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-245">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="d98ff-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d98ff-246">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d98ff-246">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-247">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d98ff-247">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-248">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d98ff-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-250">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="d98ff-250">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="d98ff-251">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-252">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d98ff-252">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-253">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-255">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="d98ff-255">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="d98ff-256">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-257">**Direção**</span><span class="sxs-lookup"><span data-stu-id="d98ff-257">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-258">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-260">A configuração do dispositivo apontador para a operação do lado direito ou esquerdo.</span><span class="sxs-lookup"><span data-stu-id="d98ff-260">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="d98ff-261">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-261">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="d98ff-262">Valor</span><span class="sxs-lookup"><span data-stu-id="d98ff-262">Value</span></span>                                                                        | <span data-ttu-id="d98ff-263">Significado</span><span class="sxs-lookup"><span data-stu-id="d98ff-263">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="d98ff-264"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d98ff-264"><dt>0</dt></span></span> </dl> | <span data-ttu-id="d98ff-265">Unknown</span><span class="sxs-lookup"><span data-stu-id="d98ff-265">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="d98ff-266"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d98ff-266"><dt>1</dt></span></span> </dl> | <span data-ttu-id="d98ff-267">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="d98ff-267">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="d98ff-268"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d98ff-268"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d98ff-269">Operação de mão direita.</span><span class="sxs-lookup"><span data-stu-id="d98ff-269">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="d98ff-270"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d98ff-270"><dt>3</dt></span></span> </dl> | <span data-ttu-id="d98ff-271">Operação da mão esquerda.</span><span class="sxs-lookup"><span data-stu-id="d98ff-271">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="d98ff-272">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d98ff-272">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-273">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-275">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="d98ff-275">The current health of the element.</span></span> <span data-ttu-id="d98ff-276">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK)</span><span class="sxs-lookup"><span data-stu-id="d98ff-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK)</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-277">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d98ff-277">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-278">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-278">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-280">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="d98ff-280">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="d98ff-281">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d98ff-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-283">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d98ff-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-285">A data e a hora em que a máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-285">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="d98ff-286">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d98ff-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-287">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d98ff-287">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-290">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d98ff-290">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-291">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d98ff-291">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d98ff-292">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d98ff-292">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-293">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="d98ff-293">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-294">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d98ff-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-296">Indica se o dispositivo está bloqueado, impedindo a entrada ou saída do usuário.</span><span class="sxs-lookup"><span data-stu-id="d98ff-296">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="d98ff-297">Essa propriedade é herdada [**do \_ userdevice do CIM**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-297">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-298">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d98ff-298">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-299">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d98ff-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-301">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d98ff-301">The last error code reported by the logical device.</span></span> <span data-ttu-id="d98ff-302">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-303">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="d98ff-303">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-304">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d98ff-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-306">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="d98ff-306">This property has been deprecated.</span></span> <span data-ttu-id="d98ff-307">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-308">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d98ff-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-311">Qualificadores: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="d98ff-311">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-312">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="d98ff-312">The label by which the object is known.</span></span> <span data-ttu-id="d98ff-313">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="d98ff-313">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="d98ff-314">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d98ff-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-315">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="d98ff-315">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-316">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="d98ff-316">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-318">O número de botões no dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="d98ff-318">The number of buttons on the pointing device.</span></span> <span data-ttu-id="d98ff-319">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-319">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d98ff-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-321">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-323">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="d98ff-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d98ff-324">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d98ff-325">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d98ff-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d98ff-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d98ff-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="d98ff-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="d98ff-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="d98ff-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="d98ff-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="d98ff-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="d98ff-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="d98ff-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="d98ff-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="d98ff-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="d98ff-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="d98ff-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="d98ff-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="d98ff-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="d98ff-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="d98ff-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="d98ff-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d98ff-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d98ff-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d98ff-345">)</span><span class="sxs-lookup"><span data-stu-id="d98ff-345">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d98ff-346">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d98ff-346">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-347">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-349">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="d98ff-349">The current status of the element.</span></span> <span data-ttu-id="d98ff-350">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="d98ff-350">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-351">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d98ff-351">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-354">O estado habilitado ou desabilitado do elemento quando a propriedade [**enabledstate**](msvm-keyboard.md) é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="d98ff-354">The enabled or disabled state of the element when the [**EnabledState**](msvm-keyboard.md) property is set to 1 (Other).</span></span> <span data-ttu-id="d98ff-355">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="d98ff-355">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d98ff-356">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d98ff-356">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-357">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d98ff-357">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-358">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-360">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d98ff-360">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="d98ff-361">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-362">**Ponto de apontar**</span><span class="sxs-lookup"><span data-stu-id="d98ff-362">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-363">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-363">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-365">O tipo do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="d98ff-365">The type of the pointing device.</span></span> <span data-ttu-id="d98ff-366">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-366">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="d98ff-367">Valor</span><span class="sxs-lookup"><span data-stu-id="d98ff-367">Value</span></span>                                                                        | <span data-ttu-id="d98ff-368">Significado</span><span class="sxs-lookup"><span data-stu-id="d98ff-368">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="d98ff-369"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d98ff-369"><dt>3</dt></span></span> </dl> | <span data-ttu-id="d98ff-370">Mouse</span><span class="sxs-lookup"><span data-stu-id="d98ff-370">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d98ff-371">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d98ff-371">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-372">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-372">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-374">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d98ff-374">The power management capabilities of the device.</span></span> <span data-ttu-id="d98ff-375">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-376">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d98ff-376">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-377">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d98ff-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-379">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="d98ff-379">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="d98ff-380">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-381">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d98ff-381">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-382">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d98ff-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-384">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="d98ff-384">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="d98ff-385">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-386">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d98ff-386">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-387">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-389">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="d98ff-389">Provides high level status information.</span></span> <span data-ttu-id="d98ff-390">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="d98ff-390">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d98ff-391">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d98ff-392">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d98ff-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d98ff-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d98ff-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-394"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d98ff-394"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="d98ff-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="d98ff-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d98ff-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d98ff-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d98ff-399">)</span><span class="sxs-lookup"><span data-stu-id="d98ff-399">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d98ff-400">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d98ff-400">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-401">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-403">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="d98ff-403">The last requested or desired state for the element.</span></span> <span data-ttu-id="d98ff-404">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d98ff-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d98ff-405">Valor</span><span class="sxs-lookup"><span data-stu-id="d98ff-405">Value</span></span>                                                                         | <span data-ttu-id="d98ff-406">Significado</span><span class="sxs-lookup"><span data-stu-id="d98ff-406">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="d98ff-407"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d98ff-407"><dt>12</dt></span></span> </dl> | <span data-ttu-id="d98ff-408">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="d98ff-408">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d98ff-409">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="d98ff-409">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-410">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d98ff-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-411">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-412">A resolução de rastreamento do dispositivo apontador, em contagens por polegada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-412">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="d98ff-413">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-413">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-414">**Status**</span><span class="sxs-lookup"><span data-stu-id="d98ff-414">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-415">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-417">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d98ff-417">The current status of the object.</span></span> <span data-ttu-id="d98ff-418">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-419">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d98ff-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-420">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-422">Cadeias de caracteres que descrevem os vários valores de matriz de [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="d98ff-422">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="d98ff-423">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) e é sempre definida como "OK".</span><span class="sxs-lookup"><span data-stu-id="d98ff-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-424">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d98ff-424">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-425">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-425">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-426">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-427">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d98ff-427">The current state of the logical device.</span></span> <span data-ttu-id="d98ff-428">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-429">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d98ff-429">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-430">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-432">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d98ff-432">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-433">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d98ff-433">The scoping system's creation class name.</span></span> <span data-ttu-id="d98ff-434">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-435">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d98ff-435">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-436">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d98ff-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-438">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d98ff-438">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-439">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="d98ff-439">The scoping system's name.</span></span> <span data-ttu-id="d98ff-440">Esse valor corresponde ao valor da propriedade [**Name**](msvm-computersystem.md) da classe **Msvm \_ ComputerSystem** para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="d98ff-440">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="d98ff-441">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d98ff-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-442">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d98ff-442">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-443">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d98ff-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-445">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="d98ff-445">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d98ff-446">Se o estado do elemento não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de 0.</span><span class="sxs-lookup"><span data-stu-id="d98ff-446">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="d98ff-447">Se uma alteração de estado foi solicitada, mas rejeitada ou ainda não processada, a propriedade não deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-447">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="d98ff-448">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d98ff-448">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-449">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d98ff-449">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-450">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d98ff-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-452">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="d98ff-452">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="d98ff-453">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d98ff-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98ff-454">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d98ff-454">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d98ff-455">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d98ff-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d98ff-456">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d98ff-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d98ff-457">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="d98ff-457">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d98ff-458">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d98ff-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d98ff-459">Comentários</span><span class="sxs-lookup"><span data-stu-id="d98ff-459">Remarks</span></span>

<span data-ttu-id="d98ff-460">O acesso à classe **Msvm \_ Ps2Mouse** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="d98ff-460">Access to the **Msvm\_Ps2Mouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d98ff-461">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d98ff-461">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d98ff-462">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d98ff-462">Requirements</span></span>



| <span data-ttu-id="d98ff-463">Requisito</span><span class="sxs-lookup"><span data-stu-id="d98ff-463">Requirement</span></span> | <span data-ttu-id="d98ff-464">Valor</span><span class="sxs-lookup"><span data-stu-id="d98ff-464">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d98ff-465">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d98ff-465">Minimum supported client</span></span><br/> | <span data-ttu-id="d98ff-466">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d98ff-466">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d98ff-467">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d98ff-467">Minimum supported server</span></span><br/> | <span data-ttu-id="d98ff-468">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d98ff-468">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d98ff-469">Namespace</span><span class="sxs-lookup"><span data-stu-id="d98ff-469">Namespace</span></span><br/>                | <span data-ttu-id="d98ff-470">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d98ff-470">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d98ff-471">MOF</span><span class="sxs-lookup"><span data-stu-id="d98ff-471">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d98ff-472"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d98ff-472"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d98ff-473">DLL</span><span class="sxs-lookup"><span data-stu-id="d98ff-473">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d98ff-474"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d98ff-474"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d98ff-475">Confira também</span><span class="sxs-lookup"><span data-stu-id="d98ff-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d98ff-476">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d98ff-476">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="d98ff-477">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d98ff-477">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="d98ff-478">Classes de entrada</span><span class="sxs-lookup"><span data-stu-id="d98ff-478">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

