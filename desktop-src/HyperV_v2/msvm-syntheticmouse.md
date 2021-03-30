---
description: Representa um dispositivo de mouse sintético.
ms.assetid: c04b7aa1-44fe-41f5-943f-ff49ce64be96
title: Classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse
- Msvm_SyntheticMouse.SetPowerState
- Msvm_SyntheticMouse.EnableDevice
- Msvm_SyntheticMouse.OnlineDevice
- Msvm_SyntheticMouse.QuiesceDevice
- Msvm_SyntheticMouse.SaveProperties
- Msvm_SyntheticMouse.RestoreProperties
- Msvm_SyntheticMouse.InstanceID
- Msvm_SyntheticMouse.Caption
- Msvm_SyntheticMouse.Description
- Msvm_SyntheticMouse.ElementName
- Msvm_SyntheticMouse.InstallDate
- Msvm_SyntheticMouse.Name
- Msvm_SyntheticMouse.OperationalStatus
- Msvm_SyntheticMouse.StatusDescriptions
- Msvm_SyntheticMouse.Status
- Msvm_SyntheticMouse.HealthState
- Msvm_SyntheticMouse.CommunicationStatus
- Msvm_SyntheticMouse.DetailedStatus
- Msvm_SyntheticMouse.OperatingStatus
- Msvm_SyntheticMouse.PrimaryStatus
- Msvm_SyntheticMouse.EnabledState
- Msvm_SyntheticMouse.OtherEnabledState
- Msvm_SyntheticMouse.RequestedState
- Msvm_SyntheticMouse.EnabledDefault
- Msvm_SyntheticMouse.TimeOfLastStateChange
- Msvm_SyntheticMouse.AvailableRequestedStates
- Msvm_SyntheticMouse.TransitioningToState
- Msvm_SyntheticMouse.SystemCreationClassName
- Msvm_SyntheticMouse.SystemName
- Msvm_SyntheticMouse.CreationClassName
- Msvm_SyntheticMouse.DeviceID
- Msvm_SyntheticMouse.PowerManagementSupported
- Msvm_SyntheticMouse.PowerManagementCapabilities
- Msvm_SyntheticMouse.Availability
- Msvm_SyntheticMouse.StatusInfo
- Msvm_SyntheticMouse.LastErrorCode
- Msvm_SyntheticMouse.ErrorDescription
- Msvm_SyntheticMouse.ErrorCleared
- Msvm_SyntheticMouse.OtherIdentifyingInfo
- Msvm_SyntheticMouse.PowerOnHours
- Msvm_SyntheticMouse.TotalPowerOnHours
- Msvm_SyntheticMouse.IdentifyingDescriptions
- Msvm_SyntheticMouse.AdditionalAvailability
- Msvm_SyntheticMouse.MaxQuiesceTime
- Msvm_SyntheticMouse.IsLocked
- Msvm_SyntheticMouse.PointingType
- Msvm_SyntheticMouse.NumberOfButtons
- Msvm_SyntheticMouse.Handedness
- Msvm_SyntheticMouse.Resolution
- Msvm_SyntheticMouse.AbsoluteCoordinates
- Msvm_SyntheticMouse.HorizontalPosition
- Msvm_SyntheticMouse.VerticalPosition
- Msvm_SyntheticMouse.ScrollPosition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c5be44637c91ebd57867c5062eba6f9e57ee543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646823"
---
# <a name="msvm_syntheticmouse-class"></a><span data-ttu-id="1f051-103">\_Classe Msvm SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="1f051-103">Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="1f051-104">Representa um dispositivo de mouse sintético.</span><span class="sxs-lookup"><span data-stu-id="1f051-104">Represents a synthetic mouse device.</span></span>

<span data-ttu-id="1f051-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1f051-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f051-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f051-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticMouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Synthetic Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {
                "OK"
              };
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
  string   CreationClassName = "Msvm_SyntheticMouse";
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
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = True;
  sint32   HorizontalPosition;
  sint32   VerticalPosition;
  sint32   ScrollPosition;
};
```

## <a name="members"></a><span data-ttu-id="1f051-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1f051-107">Members</span></span>

<span data-ttu-id="1f051-108">A classe **Msvm \_ SyntheticMouse** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1f051-108">The **Msvm\_SyntheticMouse** class has these types of members:</span></span>

-   [<span data-ttu-id="1f051-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f051-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1f051-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f051-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1f051-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1f051-111">Methods</span></span>

<span data-ttu-id="1f051-112">A classe **Msvm \_ SyntheticMouse** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1f051-112">The **Msvm\_SyntheticMouse** class has these methods.</span></span>



| <span data-ttu-id="1f051-113">Método</span><span class="sxs-lookup"><span data-stu-id="1f051-113">Method</span></span>                                                                 | <span data-ttu-id="1f051-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f051-114">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="1f051-115">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="1f051-115">**ClickButton**</span></span>](clickbutton-msvm-syntheticmouse.md)                 | <span data-ttu-id="1f051-116">Simula um clique de botão do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="1f051-116">Simulates a button click of the specified device button.</span></span><br/>           |
| <span data-ttu-id="1f051-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="1f051-117">**EnableDevice**</span></span>                                                       | <span data-ttu-id="1f051-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="1f051-118">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="1f051-119">**Getbuttonstate**</span><span class="sxs-lookup"><span data-stu-id="1f051-119">**GetButtonState**</span></span>](getbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="1f051-120">Recupera o estado atual do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="1f051-120">Retrieves the current state of the specified device button.</span></span><br/>        |
| <span data-ttu-id="1f051-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="1f051-121">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="1f051-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="1f051-122">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="1f051-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="1f051-123">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="1f051-124">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="1f051-124">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="1f051-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="1f051-125">**RequestStateChange**</span></span>](msvm-syntheticmouse-requeststatechange.md)   | <span data-ttu-id="1f051-126">Solicita uma alteração de estado</span><span class="sxs-lookup"><span data-stu-id="1f051-126">Requests a state change</span></span><br/>                                            |
| [<span data-ttu-id="1f051-127">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="1f051-127">**Reset**</span></span>](msvm-syntheticmouse-reset.md)                             | <span data-ttu-id="1f051-128">Redefine o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1f051-128">Resets the device.</span></span><br/>                                                 |
| <span data-ttu-id="1f051-129">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="1f051-129">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="1f051-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="1f051-130">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="1f051-131">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="1f051-131">**SaveProperties**</span></span>                                                     | <span data-ttu-id="1f051-132">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="1f051-132">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="1f051-133">**SetAbsolutePosition**</span><span class="sxs-lookup"><span data-stu-id="1f051-133">**SetAbsolutePosition**</span></span>](setabsoluteposition-msvm-syntheticmouse.md) | <span data-ttu-id="1f051-134">Define a posição horizontal e vertical do cursor do mouse.</span><span class="sxs-lookup"><span data-stu-id="1f051-134">Sets the horizontal and vertical position of the mouse cursor.</span></span><br/>     |
| [<span data-ttu-id="1f051-135">**Setbuttonstate**</span><span class="sxs-lookup"><span data-stu-id="1f051-135">**SetButtonState**</span></span>](setbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="1f051-136">Define o estado atual do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="1f051-136">Sets the current state of the specified device button.</span></span><br/>             |
| <span data-ttu-id="1f051-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1f051-137">**SetPowerState**</span></span>                                                      | <span data-ttu-id="1f051-138">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="1f051-138">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="1f051-139">**SetScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="1f051-139">**SetScrollPosition**</span></span>](setscrollposition-msvm-syntheticmouse.md)     | <span data-ttu-id="1f051-140">Define a coordenada z do controle de roda do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="1f051-140">Sets the z-coordinate of the wheel control of the pointing device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1f051-141">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1f051-141">Properties</span></span>

<span data-ttu-id="1f051-142">A classe **Msvm \_ SyntheticMouse** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1f051-142">The **Msvm\_SyntheticMouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f051-143">**AbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="1f051-143">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-144">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1f051-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-146">Indica se o dispositivo opera em coordenadas absolutas ou relativas.</span><span class="sxs-lookup"><span data-stu-id="1f051-146">Indicates whether the device operates on absolute or relative coordinates.</span></span>



| <span data-ttu-id="1f051-147">Valor</span><span class="sxs-lookup"><span data-stu-id="1f051-147">Value</span></span>                                                                                | <span data-ttu-id="1f051-148">Significado</span><span class="sxs-lookup"><span data-stu-id="1f051-148">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="1f051-149"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-149"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="1f051-150">As coordenadas do dispositivo são absolutas.</span><span class="sxs-lookup"><span data-stu-id="1f051-150">The device's coordinates are absolute.</span></span><br/> |
| <dl> <span data-ttu-id="1f051-151"><dt>**For**</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-151"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="1f051-152">As coordenadas do dispositivo são relativas.</span><span class="sxs-lookup"><span data-stu-id="1f051-152">The device's coordinates are relative.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f051-153">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="1f051-153">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-154">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1f051-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-156">Qualquer disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="1f051-156">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="1f051-157">A propriedade de **disponibilidade** denota o status primário e a disponibilidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1f051-157">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="1f051-158">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-158">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="1f051-159">Valor</span><span class="sxs-lookup"><span data-stu-id="1f051-159">Value</span></span>                                                                          | <span data-ttu-id="1f051-160">Significado</span><span class="sxs-lookup"><span data-stu-id="1f051-160">Meaning</span></span>                   |
|--------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>{6}</dt> </dl> | <span data-ttu-id="1f051-161">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="1f051-161">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f051-162">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="1f051-162">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-165">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1f051-165">The primary availability and status of the device.</span></span> <span data-ttu-id="1f051-166">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-166">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="1f051-167">Valor</span><span class="sxs-lookup"><span data-stu-id="1f051-167">Value</span></span>                                                                        | <span data-ttu-id="1f051-168">Significado</span><span class="sxs-lookup"><span data-stu-id="1f051-168">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="1f051-169"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-169"><dt>6</dt></span></span> </dl> | <span data-ttu-id="1f051-170">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="1f051-170">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f051-171">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="1f051-171">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-172">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-172">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1f051-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-174">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="1f051-174">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="1f051-175">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f051-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-176">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1f051-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-179">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1f051-179">A short description of the object.</span></span> <span data-ttu-id="1f051-180">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-181">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="1f051-181">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-182">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-184">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="1f051-184">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1f051-185">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1f051-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1f051-186">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1f051-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1f051-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="1f051-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="1f051-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="1f051-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="1f051-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1f051-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1f051-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1f051-194">)</span><span class="sxs-lookup"><span data-stu-id="1f051-194">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f051-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1f051-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f051-198">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1f051-198">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="1f051-199">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="1f051-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1f051-200">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="1f051-200">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="1f051-201">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-202">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1f051-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-205">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="1f051-205">A description of the object.</span></span> <span data-ttu-id="1f051-206">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1f051-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-210">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="1f051-210">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1f051-211">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1f051-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1f051-212">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1f051-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="1f051-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="1f051-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="1f051-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="1f051-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="1f051-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="1f051-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1f051-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1f051-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1f051-221">)</span><span class="sxs-lookup"><span data-stu-id="1f051-221">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f051-222">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1f051-222">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f051-225">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="1f051-225">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="1f051-226">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1f051-226">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="1f051-227">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="1f051-227">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="1f051-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1f051-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-229">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-231">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1f051-231">A display name for the object.</span></span> <span data-ttu-id="1f051-232">Essa propriedade permite que cada instância defina um nome de exibição além de suas propriedades de chave, dados de identidade e informações de descrição.</span><span class="sxs-lookup"><span data-stu-id="1f051-232">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="1f051-233">A propriedade [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) da classe **CIM \_ ManagedSystemElement** também é definida como um nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="1f051-233">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="1f051-234">Mas, muitas vezes, é uma subclasse para ser uma chave.</span><span class="sxs-lookup"><span data-stu-id="1f051-234">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="1f051-235">Não é razoável que a mesma propriedade possa transmitir a identidade e um nome de exibição, sem inconsistências.</span><span class="sxs-lookup"><span data-stu-id="1f051-235">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="1f051-236">Onde [**Name**](msvm-keyboard.md) existe e não é uma chave (como para instâncias de LogicalDevice), as mesmas informações podem estar presentes nas propriedades **Name** e **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="1f051-236">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="1f051-237">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="1f051-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-239">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-241">A configuração de inicialização ou padrão de um administrador para o **enabledstate** de um elemento.</span><span class="sxs-lookup"><span data-stu-id="1f051-241">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="1f051-242">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f051-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1f051-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-244">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-246">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="1f051-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1f051-247">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f051-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="1f051-248">Valor</span><span class="sxs-lookup"><span data-stu-id="1f051-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="1f051-249">Significado</span><span class="sxs-lookup"><span data-stu-id="1f051-249">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="1f051-250"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="1f051-251">A máquina virtual convidada dá suporte a um mouse sintético.</span><span class="sxs-lookup"><span data-stu-id="1f051-251">The guest virtual machine supports a synthetic mouse.</span></span><br/>         |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="1f051-252"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="1f051-253">A máquina virtual convidada não dá suporte a um mouse sintético.</span><span class="sxs-lookup"><span data-stu-id="1f051-253">The guest virtual machine does not support a synthetic mouse.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f051-254">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1f051-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-255">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1f051-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-257">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="1f051-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="1f051-258">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="1f051-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1f051-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-260">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-262">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="1f051-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="1f051-263">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="1f051-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-264">**Direção**</span><span class="sxs-lookup"><span data-stu-id="1f051-264">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-265">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-265">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-267">A configuração do dispositivo apontador para a operação do lado direito ou esquerdo.</span><span class="sxs-lookup"><span data-stu-id="1f051-267">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="1f051-268">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-268">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="1f051-269">Valor</span><span class="sxs-lookup"><span data-stu-id="1f051-269">Value</span></span>                                                                        | <span data-ttu-id="1f051-270">Significado</span><span class="sxs-lookup"><span data-stu-id="1f051-270">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="1f051-271"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-271"><dt>0</dt></span></span> </dl> | <span data-ttu-id="1f051-272">Unknown</span><span class="sxs-lookup"><span data-stu-id="1f051-272">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="1f051-273"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-273"><dt>1</dt></span></span> </dl> | <span data-ttu-id="1f051-274">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="1f051-274">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="1f051-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1f051-276">Operação de mão direita.</span><span class="sxs-lookup"><span data-stu-id="1f051-276">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="1f051-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="1f051-278">Operação da mão esquerda.</span><span class="sxs-lookup"><span data-stu-id="1f051-278">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="1f051-279">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1f051-279">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-280">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-282">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="1f051-282">The current health of the element.</span></span> <span data-ttu-id="1f051-283">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-283">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-284">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="1f051-284">**HorizontalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-285">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1f051-285">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-287">A coordenada x absoluta do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="1f051-287">The absolute x-coordinate of the pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1f051-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-289">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1f051-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-291">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="1f051-291">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="1f051-292">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1f051-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-294">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1f051-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-296">A data e a hora em que a máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="1f051-296">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="1f051-297">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1f051-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-299">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f051-301">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="1f051-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1f051-302">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="1f051-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1f051-303">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="1f051-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-305">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1f051-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-307">Indica se o dispositivo está bloqueado, impedindo a entrada ou saída do usuário.</span><span class="sxs-lookup"><span data-stu-id="1f051-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="1f051-308">Essa propriedade é herdada [**do \_ userdevice do CIM**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1f051-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-310">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f051-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-312">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1f051-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="1f051-313">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="1f051-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-314">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="1f051-314">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-315">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1f051-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-317">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="1f051-317">This property has been deprecated.</span></span> <span data-ttu-id="1f051-318">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-319">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1f051-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f051-322">Qualificadores: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="1f051-322">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="1f051-323">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="1f051-323">The label by which the object is known.</span></span> <span data-ttu-id="1f051-324">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="1f051-324">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="1f051-325">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-326">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="1f051-326">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-327">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="1f051-327">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-329">O número de botões no dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="1f051-329">The number of buttons on the pointing device.</span></span> <span data-ttu-id="1f051-330">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-330">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-331">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="1f051-331">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-332">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-334">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="1f051-334">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1f051-335">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1f051-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1f051-336">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1f051-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1f051-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="1f051-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="1f051-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="1f051-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="1f051-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="1f051-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="1f051-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="1f051-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="1f051-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="1f051-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="1f051-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="1f051-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="1f051-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="1f051-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="1f051-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="1f051-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="1f051-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1f051-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1f051-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1f051-356">)</span><span class="sxs-lookup"><span data-stu-id="1f051-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f051-357">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1f051-357">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-358">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1f051-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-360">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="1f051-360">The current status of the element.</span></span> <span data-ttu-id="1f051-361">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-362">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="1f051-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-363">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-365">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="1f051-365">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="1f051-366">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="1f051-366">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="1f051-367">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f051-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1f051-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-369">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1f051-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-371">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1f051-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="1f051-372">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-373">**Ponto de apontar**</span><span class="sxs-lookup"><span data-stu-id="1f051-373">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-374">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-376">O tipo de dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="1f051-376">The type of pointing device.</span></span> <span data-ttu-id="1f051-377">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-377">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="1f051-378">Valor</span><span class="sxs-lookup"><span data-stu-id="1f051-378">Value</span></span>                                                                        | <span data-ttu-id="1f051-379">Significado</span><span class="sxs-lookup"><span data-stu-id="1f051-379">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="1f051-380"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-380"><dt>3</dt></span></span> </dl> | <span data-ttu-id="1f051-381">Mouse</span><span class="sxs-lookup"><span data-stu-id="1f051-381">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f051-382">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1f051-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-383">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1f051-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-385">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1f051-385">The power management capabilities of the device.</span></span> <span data-ttu-id="1f051-386">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="1f051-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1f051-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-388">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1f051-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-390">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="1f051-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="1f051-391">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="1f051-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-392">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="1f051-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-393">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1f051-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-395">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="1f051-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="1f051-396">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="1f051-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-397">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="1f051-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-398">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-400">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="1f051-400">Provides high level status information.</span></span> <span data-ttu-id="1f051-401">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="1f051-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1f051-402">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1f051-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1f051-403">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1f051-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1f051-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="1f051-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="1f051-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="1f051-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1f051-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1f051-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1f051-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1f051-410">)</span><span class="sxs-lookup"><span data-stu-id="1f051-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1f051-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1f051-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-412">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-414">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="1f051-414">The last requested or desired state for the element.</span></span> <span data-ttu-id="1f051-415">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f051-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="1f051-416">Valor</span><span class="sxs-lookup"><span data-stu-id="1f051-416">Value</span></span>                                                                         | <span data-ttu-id="1f051-417">Significado</span><span class="sxs-lookup"><span data-stu-id="1f051-417">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="1f051-418"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-418"><dt>12</dt></span></span> </dl> | <span data-ttu-id="1f051-419">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="1f051-419">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f051-420">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="1f051-420">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-421">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f051-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-423">A resolução de rastreamento do dispositivo apontador, em contagens por polegada.</span><span class="sxs-lookup"><span data-stu-id="1f051-423">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="1f051-424">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-424">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-425">**ScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="1f051-425">**ScrollPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-426">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1f051-426">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-427">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f051-428">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="1f051-428">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="1f051-429">A posição da coordenada z do dispositivo de mouse.</span><span class="sxs-lookup"><span data-stu-id="1f051-429">The z-coordinate position of the mouse device.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-430">**Status**</span><span class="sxs-lookup"><span data-stu-id="1f051-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-431">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-433">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1f051-433">The current status of the object.</span></span> <span data-ttu-id="1f051-434">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="1f051-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-435">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1f051-435">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-436">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-436">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1f051-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-438">Cadeias de caracteres que descrevem os vários valores de matriz de [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="1f051-438">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="1f051-439">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1f051-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1f051-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-441">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-443">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1f051-443">The current state of the logical device.</span></span> <span data-ttu-id="1f051-444">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="1f051-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-445">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1f051-445">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-446">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f051-448">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1f051-448">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="1f051-449">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="1f051-449">The creation class name of the scoping system.</span></span> <span data-ttu-id="1f051-450">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-451">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1f051-451">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-452">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f051-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f051-454">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1f051-454">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="1f051-455">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="1f051-455">The name of the scoping system.</span></span> <span data-ttu-id="1f051-456">Esse valor corresponde ao valor da propriedade [**Name**](msvm-computersystem.md) da classe **Msvm \_ ComputerSystem** para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="1f051-456">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="1f051-457">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="1f051-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1f051-458">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="1f051-458">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-459">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1f051-459">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-461">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="1f051-461">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1f051-462">Se o estado do elemento não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de 0.</span><span class="sxs-lookup"><span data-stu-id="1f051-462">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="1f051-463">Se uma alteração de estado foi solicitada, mas rejeitada ou ainda não processada, a propriedade não deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="1f051-463">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="1f051-464">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f051-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="1f051-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-466">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1f051-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-467">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-468">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="1f051-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="1f051-469">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="1f051-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-470">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="1f051-470">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-471">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f051-471">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-473">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="1f051-473">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1f051-474">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f051-474">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1f051-475">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="1f051-475">**VerticalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f051-476">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1f051-476">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f051-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1f051-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f051-478">A coordenada y absoluta do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="1f051-478">The absolute y-coordinate of the pointing device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f051-479">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f051-479">Remarks</span></span>

<span data-ttu-id="1f051-480">O acesso à classe **Msvm \_ SyntheticMouse** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="1f051-480">Access to the **Msvm\_SyntheticMouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1f051-481">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1f051-481">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f051-482">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f051-482">Requirements</span></span>



| <span data-ttu-id="1f051-483">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f051-483">Requirement</span></span> | <span data-ttu-id="1f051-484">Valor</span><span class="sxs-lookup"><span data-stu-id="1f051-484">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f051-485">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f051-485">Minimum supported client</span></span><br/> | <span data-ttu-id="1f051-486">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1f051-486">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1f051-487">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f051-487">Minimum supported server</span></span><br/> | <span data-ttu-id="1f051-488">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1f051-488">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f051-489">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f051-489">Namespace</span></span><br/>                | <span data-ttu-id="1f051-490">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1f051-490">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1f051-491">MOF</span><span class="sxs-lookup"><span data-stu-id="1f051-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f051-492"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-492"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f051-493">DLL</span><span class="sxs-lookup"><span data-stu-id="1f051-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f051-494"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f051-494"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1f051-495">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f051-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f051-496">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1f051-496">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="1f051-497">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1f051-497">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="1f051-498">Classes de entrada</span><span class="sxs-lookup"><span data-stu-id="1f051-498">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

