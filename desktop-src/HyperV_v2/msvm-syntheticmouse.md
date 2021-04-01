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
# <a name="msvm_syntheticmouse-class"></a><span data-ttu-id="2e2e1-103">\_Classe Msvm SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="2e2e1-103">Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="2e2e1-104">Representa um dispositivo de mouse sintético.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-104">Represents a synthetic mouse device.</span></span>

<span data-ttu-id="2e2e1-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2e1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e2e1-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="2e2e1-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2e2e1-107">Members</span></span>

<span data-ttu-id="2e2e1-108">A classe **Msvm \_ SyntheticMouse** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2e2e1-108">The **Msvm\_SyntheticMouse** class has these types of members:</span></span>

-   [<span data-ttu-id="2e2e1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e2e1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2e2e1-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2e2e1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2e2e1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e2e1-111">Methods</span></span>

<span data-ttu-id="2e2e1-112">A classe **Msvm \_ SyntheticMouse** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-112">The **Msvm\_SyntheticMouse** class has these methods.</span></span>



| <span data-ttu-id="2e2e1-113">Método</span><span class="sxs-lookup"><span data-stu-id="2e2e1-113">Method</span></span>                                                                 | <span data-ttu-id="2e2e1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e2e1-114">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="2e2e1-115">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-115">**ClickButton**</span></span>](clickbutton-msvm-syntheticmouse.md)                 | <span data-ttu-id="2e2e1-116">Simula um clique de botão do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-116">Simulates a button click of the specified device button.</span></span><br/>           |
| <span data-ttu-id="2e2e1-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-117">**EnableDevice**</span></span>                                                       | <span data-ttu-id="2e2e1-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-118">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="2e2e1-119">**Getbuttonstate**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-119">**GetButtonState**</span></span>](getbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="2e2e1-120">Recupera o estado atual do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-120">Retrieves the current state of the specified device button.</span></span><br/>        |
| <span data-ttu-id="2e2e1-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-121">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="2e2e1-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-122">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="2e2e1-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-123">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="2e2e1-124">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-124">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="2e2e1-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-125">**RequestStateChange**</span></span>](msvm-syntheticmouse-requeststatechange.md)   | <span data-ttu-id="2e2e1-126">Solicita uma alteração de estado</span><span class="sxs-lookup"><span data-stu-id="2e2e1-126">Requests a state change</span></span><br/>                                            |
| [<span data-ttu-id="2e2e1-127">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-127">**Reset**</span></span>](msvm-syntheticmouse-reset.md)                             | <span data-ttu-id="2e2e1-128">Redefine o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-128">Resets the device.</span></span><br/>                                                 |
| <span data-ttu-id="2e2e1-129">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-129">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="2e2e1-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-130">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="2e2e1-131">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-131">**SaveProperties**</span></span>                                                     | <span data-ttu-id="2e2e1-132">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-132">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="2e2e1-133">**SetAbsolutePosition**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-133">**SetAbsolutePosition**</span></span>](setabsoluteposition-msvm-syntheticmouse.md) | <span data-ttu-id="2e2e1-134">Define a posição horizontal e vertical do cursor do mouse.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-134">Sets the horizontal and vertical position of the mouse cursor.</span></span><br/>     |
| [<span data-ttu-id="2e2e1-135">**Setbuttonstate**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-135">**SetButtonState**</span></span>](setbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="2e2e1-136">Define o estado atual do botão de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-136">Sets the current state of the specified device button.</span></span><br/>             |
| <span data-ttu-id="2e2e1-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-137">**SetPowerState**</span></span>                                                      | <span data-ttu-id="2e2e1-138">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-138">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="2e2e1-139">**SetScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-139">**SetScrollPosition**</span></span>](setscrollposition-msvm-syntheticmouse.md)     | <span data-ttu-id="2e2e1-140">Define a coordenada z do controle de roda do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-140">Sets the z-coordinate of the wheel control of the pointing device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2e2e1-141">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2e2e1-141">Properties</span></span>

<span data-ttu-id="2e2e1-142">A classe **Msvm \_ SyntheticMouse** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-142">The **Msvm\_SyntheticMouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e2e1-143">**AbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-143">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-144">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-146">Indica se o dispositivo opera em coordenadas absolutas ou relativas.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-146">Indicates whether the device operates on absolute or relative coordinates.</span></span>



| <span data-ttu-id="2e2e1-147">Valor</span><span class="sxs-lookup"><span data-stu-id="2e2e1-147">Value</span></span>                                                                                | <span data-ttu-id="2e2e1-148">Significado</span><span class="sxs-lookup"><span data-stu-id="2e2e1-148">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="2e2e1-149"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-149"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="2e2e1-150">As coordenadas do dispositivo são absolutas.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-150">The device's coordinates are absolute.</span></span><br/> |
| <dl> <span data-ttu-id="2e2e1-151"><dt>**For**</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-151"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="2e2e1-152">As coordenadas do dispositivo são relativas.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-152">The device's coordinates are relative.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2e2e1-153">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-153">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-154">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-156">Qualquer disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="2e2e1-156">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="2e2e1-157">A propriedade de **disponibilidade** denota o status primário e a disponibilidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-157">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="2e2e1-158">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-158">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="2e2e1-159">Valor</span><span class="sxs-lookup"><span data-stu-id="2e2e1-159">Value</span></span>                                                                          | <span data-ttu-id="2e2e1-160">Significado</span><span class="sxs-lookup"><span data-stu-id="2e2e1-160">Meaning</span></span>                   |
|--------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>{6}</dt> </dl> | <span data-ttu-id="2e2e1-161">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2e2e1-161">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2e2e1-162">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-162">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-165">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-165">The primary availability and status of the device.</span></span> <span data-ttu-id="2e2e1-166">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-166">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="2e2e1-167">Valor</span><span class="sxs-lookup"><span data-stu-id="2e2e1-167">Value</span></span>                                                                        | <span data-ttu-id="2e2e1-168">Significado</span><span class="sxs-lookup"><span data-stu-id="2e2e1-168">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="2e2e1-169"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-169"><dt>6</dt></span></span> </dl> | <span data-ttu-id="2e2e1-170">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2e2e1-170">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2e2e1-171">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-171">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-172">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-172">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-174">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="2e2e1-174">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="2e2e1-175">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-176">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-179">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-179">A short description of the object.</span></span> <span data-ttu-id="2e2e1-180">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-181">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-181">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-182">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-184">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-184">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2e2e1-185">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2e2e1-186">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2e2e1-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2e2e1-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2e2e1-194">)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-194">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2e2e1-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-198">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-198">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-199">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2e2e1-200">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-200">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="2e2e1-201">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-202">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-205">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="2e2e1-205">A description of the object.</span></span> <span data-ttu-id="2e2e1-206">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-210">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-210">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2e2e1-211">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2e2e1-212">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2e2e1-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2e2e1-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2e2e1-221">)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-221">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2e2e1-222">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-222">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-225">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-225">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-226">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-226">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="2e2e1-227">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="2e2e1-227">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-229">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-231">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-231">A display name for the object.</span></span> <span data-ttu-id="2e2e1-232">Essa propriedade permite que cada instância defina um nome de exibição além de suas propriedades de chave, dados de identidade e informações de descrição.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-232">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="2e2e1-233">A propriedade [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) da classe **CIM \_ ManagedSystemElement** também é definida como um nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-233">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="2e2e1-234">Mas, muitas vezes, é uma subclasse para ser uma chave.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-234">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="2e2e1-235">Não é razoável que a mesma propriedade possa transmitir a identidade e um nome de exibição, sem inconsistências.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-235">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="2e2e1-236">Onde [**Name**](msvm-keyboard.md) existe e não é uma chave (como para instâncias de LogicalDevice), as mesmas informações podem estar presentes nas propriedades **Name** e **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="2e2e1-236">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="2e2e1-237">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-239">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-241">A configuração de inicialização ou padrão de um administrador para o **enabledstate** de um elemento.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-241">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="2e2e1-242">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-244">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-246">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2e2e1-247">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="2e2e1-248">Valor</span><span class="sxs-lookup"><span data-stu-id="2e2e1-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="2e2e1-249">Significado</span><span class="sxs-lookup"><span data-stu-id="2e2e1-249">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="2e2e1-250"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="2e2e1-251">A máquina virtual convidada dá suporte a um mouse sintético.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-251">The guest virtual machine supports a synthetic mouse.</span></span><br/>         |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="2e2e1-252"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="2e2e1-253">A máquina virtual convidada não dá suporte a um mouse sintético.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-253">The guest virtual machine does not support a synthetic mouse.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2e2e1-254">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-255">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-257">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="2e2e1-258">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-260">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-262">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="2e2e1-263">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-264">**Direção**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-264">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-265">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-265">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-267">A configuração do dispositivo apontador para a operação do lado direito ou esquerdo.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-267">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="2e2e1-268">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-268">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="2e2e1-269">Valor</span><span class="sxs-lookup"><span data-stu-id="2e2e1-269">Value</span></span>                                                                        | <span data-ttu-id="2e2e1-270">Significado</span><span class="sxs-lookup"><span data-stu-id="2e2e1-270">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="2e2e1-271"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-271"><dt>0</dt></span></span> </dl> | <span data-ttu-id="2e2e1-272">Unknown</span><span class="sxs-lookup"><span data-stu-id="2e2e1-272">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="2e2e1-273"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-273"><dt>1</dt></span></span> </dl> | <span data-ttu-id="2e2e1-274">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-274">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="2e2e1-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="2e2e1-276">Operação de mão direita.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-276">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="2e2e1-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="2e2e1-278">Operação da mão esquerda.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-278">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="2e2e1-279">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-279">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-280">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-282">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-282">The current health of the element.</span></span> <span data-ttu-id="2e2e1-283">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-283">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-284">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-284">**HorizontalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-285">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-285">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-287">A coordenada x absoluta do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-287">The absolute x-coordinate of the pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-289">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-291">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="2e2e1-291">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="2e2e1-292">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-294">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-296">A data e a hora em que a máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-296">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="2e2e1-297">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-299">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-301">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-302">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2e2e1-303">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-305">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-307">Indica se o dispositivo está bloqueado, impedindo a entrada ou saída do usuário.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="2e2e1-308">Essa propriedade é herdada [**do \_ userdevice do CIM**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-310">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-312">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="2e2e1-313">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-314">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-314">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-315">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-317">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-317">This property has been deprecated.</span></span> <span data-ttu-id="2e2e1-318">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-319">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-322">Qualificadores: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-322">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-323">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-323">The label by which the object is known.</span></span> <span data-ttu-id="2e2e1-324">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-324">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="2e2e1-325">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-326">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-326">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-327">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-327">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-329">O número de botões no dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-329">The number of buttons on the pointing device.</span></span> <span data-ttu-id="2e2e1-330">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-330">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-331">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-331">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-332">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-334">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="2e2e1-334">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2e2e1-335">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2e2e1-336">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2e2e1-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2e2e1-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2e2e1-356">)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2e2e1-357">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-357">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-358">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-360">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-360">The current status of the element.</span></span> <span data-ttu-id="2e2e1-361">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-362">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-363">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-365">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-365">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="2e2e1-366">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-366">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="2e2e1-367">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-369">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-371">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="2e2e1-372">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-373">**Ponto de apontar**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-373">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-374">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-376">O tipo de dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-376">The type of pointing device.</span></span> <span data-ttu-id="2e2e1-377">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-377">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="2e2e1-378">Valor</span><span class="sxs-lookup"><span data-stu-id="2e2e1-378">Value</span></span>                                                                        | <span data-ttu-id="2e2e1-379">Significado</span><span class="sxs-lookup"><span data-stu-id="2e2e1-379">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="2e2e1-380"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-380"><dt>3</dt></span></span> </dl> | <span data-ttu-id="2e2e1-381">Mouse</span><span class="sxs-lookup"><span data-stu-id="2e2e1-381">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2e2e1-382">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-383">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-385">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-385">The power management capabilities of the device.</span></span> <span data-ttu-id="2e2e1-386">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-388">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-390">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="2e2e1-391">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-392">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-393">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-395">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="2e2e1-396">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-397">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-398">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-400">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-400">Provides high level status information.</span></span> <span data-ttu-id="2e2e1-401">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="2e2e1-402">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2e2e1-403">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2e2e1-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2e2e1-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2e2e1-410">)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2e2e1-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-412">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-414">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-414">The last requested or desired state for the element.</span></span> <span data-ttu-id="2e2e1-415">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="2e2e1-416">Valor</span><span class="sxs-lookup"><span data-stu-id="2e2e1-416">Value</span></span>                                                                         | <span data-ttu-id="2e2e1-417">Significado</span><span class="sxs-lookup"><span data-stu-id="2e2e1-417">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="2e2e1-418"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-418"><dt>12</dt></span></span> </dl> | <span data-ttu-id="2e2e1-419">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="2e2e1-419">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2e2e1-420">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-420">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-421">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-423">A resolução de rastreamento do dispositivo apontador, em contagens por polegada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-423">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="2e2e1-424">Essa propriedade é herdada do [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-424">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-425">**ScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-425">**ScrollPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-426">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-426">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-427">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-428">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="2e2e1-428">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-429">A posição da coordenada z do dispositivo de mouse.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-429">The z-coordinate position of the mouse device.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-430">**Status**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-431">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-433">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-433">The current status of the object.</span></span> <span data-ttu-id="2e2e1-434">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-435">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-435">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-436">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-436">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-438">Cadeias de caracteres que descrevem os vários valores de matriz de [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="2e2e1-438">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="2e2e1-439">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-441">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-443">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-443">The current state of the logical device.</span></span> <span data-ttu-id="2e2e1-444">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-445">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-445">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-446">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-448">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-448">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-449">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-449">The creation class name of the scoping system.</span></span> <span data-ttu-id="2e2e1-450">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-451">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-451">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-452">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-454">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="2e2e1-454">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-455">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-455">The name of the scoping system.</span></span> <span data-ttu-id="2e2e1-456">Esse valor corresponde ao valor da propriedade [**Name**](msvm-computersystem.md) da classe **Msvm \_ ComputerSystem** para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-456">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="2e2e1-457">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-458">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-458">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-459">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-459">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-461">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-461">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2e2e1-462">Se o estado do elemento não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de 0.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-462">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="2e2e1-463">Se uma alteração de estado foi solicitada, mas rejeitada ou ainda não processada, a propriedade não deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-463">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="2e2e1-464">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-466">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-467">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-468">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="2e2e1-469">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-470">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-470">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-471">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-471">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-473">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-473">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2e2e1-474">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-474">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2e2e1-475">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-475">**VerticalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e2e1-476">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-476">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e2e1-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e2e1-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e2e1-478">A coordenada y absoluta do dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-478">The absolute y-coordinate of the pointing device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e2e1-479">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e2e1-479">Remarks</span></span>

<span data-ttu-id="2e2e1-480">O acesso à classe **Msvm \_ SyntheticMouse** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="2e2e1-480">Access to the **Msvm\_SyntheticMouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2e2e1-481">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2e2e1-481">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2e1-482">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e2e1-482">Requirements</span></span>



| <span data-ttu-id="2e2e1-483">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e2e1-483">Requirement</span></span> | <span data-ttu-id="2e2e1-484">Valor</span><span class="sxs-lookup"><span data-stu-id="2e2e1-484">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2e1-485">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e2e1-485">Minimum supported client</span></span><br/> | <span data-ttu-id="2e2e1-486">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2e2e1-486">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2e2e1-487">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e2e1-487">Minimum supported server</span></span><br/> | <span data-ttu-id="2e2e1-488">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2e2e1-488">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e2e1-489">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e2e1-489">Namespace</span></span><br/>                | <span data-ttu-id="2e2e1-490">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2e2e1-490">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2e2e1-491">MOF</span><span class="sxs-lookup"><span data-stu-id="2e2e1-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e2e1-492"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-492"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e2e1-493">DLL</span><span class="sxs-lookup"><span data-stu-id="2e2e1-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e2e1-494"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e1-494"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2e2e1-495">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e2e1-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2e1-496">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-496">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="2e2e1-497">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2e2e1-497">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="2e2e1-498">Classes de entrada</span><span class="sxs-lookup"><span data-stu-id="2e2e1-498">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

