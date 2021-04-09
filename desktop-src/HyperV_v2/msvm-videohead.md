---
description: Descreve a superfície de desenho primária em um controlador de vídeo.
ms.assetid: 280ABAD0-D91B-4683-9F12-32563D7FE6BF
title: Classe Msvm_VideoHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHead
- Msvm_VideoHead.SetPowerState
- Msvm_VideoHead.EnableDevice
- Msvm_VideoHead.OnlineDevice
- Msvm_VideoHead.QuiesceDevice
- Msvm_VideoHead.SaveProperties
- Msvm_VideoHead.RestoreProperties
- Msvm_VideoHead.InstanceID
- Msvm_VideoHead.Caption
- Msvm_VideoHead.Description
- Msvm_VideoHead.ElementName
- Msvm_VideoHead.InstallDate
- Msvm_VideoHead.Name
- Msvm_VideoHead.OperationalStatus
- Msvm_VideoHead.StatusDescriptions
- Msvm_VideoHead.Status
- Msvm_VideoHead.HealthState
- Msvm_VideoHead.CommunicationStatus
- Msvm_VideoHead.DetailedStatus
- Msvm_VideoHead.OperatingStatus
- Msvm_VideoHead.PrimaryStatus
- Msvm_VideoHead.EnabledState
- Msvm_VideoHead.OtherEnabledState
- Msvm_VideoHead.RequestedState
- Msvm_VideoHead.EnabledDefault
- Msvm_VideoHead.TimeOfLastStateChange
- Msvm_VideoHead.AvailableRequestedStates
- Msvm_VideoHead.TransitioningToState
- Msvm_VideoHead.SystemCreationClassName
- Msvm_VideoHead.SystemName
- Msvm_VideoHead.CreationClassName
- Msvm_VideoHead.DeviceID
- Msvm_VideoHead.PowerManagementSupported
- Msvm_VideoHead.PowerManagementCapabilities
- Msvm_VideoHead.Availability
- Msvm_VideoHead.StatusInfo
- Msvm_VideoHead.LastErrorCode
- Msvm_VideoHead.ErrorDescription
- Msvm_VideoHead.ErrorCleared
- Msvm_VideoHead.OtherIdentifyingInfo
- Msvm_VideoHead.PowerOnHours
- Msvm_VideoHead.TotalPowerOnHours
- Msvm_VideoHead.IdentifyingDescriptions
- Msvm_VideoHead.AdditionalAvailability
- Msvm_VideoHead.MaxQuiesceTime
- Msvm_VideoHead.CurrentBitsPerPixel
- Msvm_VideoHead.CurrentHorizontalResolution
- Msvm_VideoHead.CurrentVerticalResolution
- Msvm_VideoHead.MaxRefreshRate
- Msvm_VideoHead.MinRefreshRate
- Msvm_VideoHead.CurrentRefreshRate
- Msvm_VideoHead.CurrentScanMode
- Msvm_VideoHead.OtherCurrentScanMode
- Msvm_VideoHead.CurrentNumberOfRows
- Msvm_VideoHead.CurrentNumberOfColumns
- Msvm_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f40e0386fe42177484fc07296a2f4567f1ee47a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090956"
---
# <a name="msvm_videohead-class"></a><span data-ttu-id="04a55-103">\_Classe Msvm VideoHead</span><span class="sxs-lookup"><span data-stu-id="04a55-103">Msvm\_VideoHead class</span></span>

<span data-ttu-id="04a55-104">Descreve a superfície de desenho primária em um controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="04a55-104">Describes the primary drawing surface on a display controller.</span></span>

<span data-ttu-id="04a55-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="04a55-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="04a55-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04a55-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHead : CIM_VideoHead
{
  string   InstanceID;
  string   Caption = "Video Head";
  string   Description = "Microsoft Virtual Video Head";
  string   ElementName = "Video Head";
  datetime InstallDate;
  string   Name = "Video Head";
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_VideoHead";
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint32   CurrentVerticalResolution;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  string   OtherCurrentScanMode;
  uint32   CurrentNumberOfRows;
  uint32   CurrentNumberOfColumns;
  uint64   CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="04a55-107">Membros</span><span class="sxs-lookup"><span data-stu-id="04a55-107">Members</span></span>

<span data-ttu-id="04a55-108">A classe **Msvm \_ VideoHead** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="04a55-108">The **Msvm\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="04a55-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="04a55-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="04a55-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="04a55-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="04a55-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="04a55-111">Methods</span></span>

<span data-ttu-id="04a55-112">A classe **Msvm \_ VideoHead** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="04a55-112">The **Msvm\_VideoHead** class has these methods.</span></span>



| <span data-ttu-id="04a55-113">Método</span><span class="sxs-lookup"><span data-stu-id="04a55-113">Method</span></span>                                                          | <span data-ttu-id="04a55-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="04a55-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="04a55-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="04a55-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="04a55-116">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="04a55-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="04a55-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="04a55-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="04a55-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="04a55-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="04a55-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="04a55-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="04a55-120">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="04a55-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="04a55-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="04a55-121">**RequestStateChange**</span></span>](msvm-videohead-requeststatechange.md) | <span data-ttu-id="04a55-122">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="04a55-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="04a55-123">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="04a55-123">**Reset**</span></span>](msvm-videohead-reset.md)                           | <span data-ttu-id="04a55-124">Redefine o dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="04a55-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="04a55-125">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="04a55-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="04a55-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="04a55-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="04a55-127">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="04a55-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="04a55-128">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="04a55-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="04a55-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="04a55-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="04a55-130">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="04a55-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="04a55-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="04a55-131">Properties</span></span>

<span data-ttu-id="04a55-132">A classe **Msvm \_ VideoHead** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="04a55-132">The **Msvm\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04a55-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="04a55-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-134">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="04a55-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-136">Qualquer disponibilidade e status adicionais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04a55-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="04a55-137">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como 6 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="04a55-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-138">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="04a55-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-141">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04a55-141">The primary availability and status of the device.</span></span> <span data-ttu-id="04a55-142">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="04a55-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="04a55-143">Valor</span><span class="sxs-lookup"><span data-stu-id="04a55-143">Value</span></span>                                                                        | <span data-ttu-id="04a55-144">Significado</span><span class="sxs-lookup"><span data-stu-id="04a55-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="04a55-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="04a55-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="04a55-146">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="04a55-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="04a55-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="04a55-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-148">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="04a55-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-150">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="04a55-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="04a55-151">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="04a55-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-152">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="04a55-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-155">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="04a55-155">A short description of the object.</span></span> <span data-ttu-id="04a55-156">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="04a55-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-158">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-160">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="04a55-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="04a55-161">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="04a55-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="04a55-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="04a55-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="04a55-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="04a55-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="04a55-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="04a55-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="04a55-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="04a55-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="04a55-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="04a55-170">)</span><span class="sxs-lookup"><span data-stu-id="04a55-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="04a55-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="04a55-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-172">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-174">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="04a55-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="04a55-175">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="04a55-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-176">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="04a55-176">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-177">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04a55-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04a55-179">Qualificadores: **unidades** ("bits")</span><span class="sxs-lookup"><span data-stu-id="04a55-179">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="04a55-180">O número de bits usados para exibir cada pixel.</span><span class="sxs-lookup"><span data-stu-id="04a55-180">The number of bits used to display each pixel.</span></span> <span data-ttu-id="04a55-181">Essa propriedade é herdada do [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-181">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-182">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="04a55-182">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-183">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04a55-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04a55-185">Qualificadores: **unidades** ("pixels")</span><span class="sxs-lookup"><span data-stu-id="04a55-185">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="04a55-186">O número atual de pixels horizontais.</span><span class="sxs-lookup"><span data-stu-id="04a55-186">The current number of horizontal pixels.</span></span> <span data-ttu-id="04a55-187">Essa propriedade é herdada do [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-187">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-188">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="04a55-188">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-189">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="04a55-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-191">O número de cores com suporte nas resoluções atuais.</span><span class="sxs-lookup"><span data-stu-id="04a55-191">The number of colors supported at the current resolutions.</span></span> <span data-ttu-id="04a55-192">Essa propriedade é herdada do [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-192">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-193">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="04a55-193">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-194">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04a55-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-196">Se estiver no modo de caractere, o número de colunas para esse controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="04a55-196">If in character mode, the number of columns for this display controller.</span></span> <span data-ttu-id="04a55-197">Caso contrário, será 0.</span><span class="sxs-lookup"><span data-stu-id="04a55-197">Otherwise, 0.</span></span> <span data-ttu-id="04a55-198">Essa propriedade é herdada do [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-198">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-199">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="04a55-199">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-200">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04a55-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-202">Se estiver no modo de caractere, o número de linhas para este controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="04a55-202">If in character mode, the number of rows for this video controller.</span></span> <span data-ttu-id="04a55-203">Caso contrário, será 0.</span><span class="sxs-lookup"><span data-stu-id="04a55-203">Otherwise, 0.</span></span> <span data-ttu-id="04a55-204">Essa propriedade é herdada do [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-204">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-205">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="04a55-205">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-206">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04a55-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04a55-208">Qualificadores: **unidades** ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="04a55-208">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="04a55-209">A taxa de atualização atual, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="04a55-209">The current refresh rate, in hertz.</span></span> <span data-ttu-id="04a55-210">Essa propriedade é herdada do [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-210">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-211">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="04a55-211">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-212">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-214">O modo de verificação atual.</span><span class="sxs-lookup"><span data-stu-id="04a55-214">The current scan mode.</span></span> <span data-ttu-id="04a55-215">Essa propriedade é herdada do [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-215">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="04a55-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="04a55-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="04a55-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="04a55-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Operação não entrelaçada** (3)</span><span class="sxs-lookup"><span data-stu-id="04a55-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (3)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Operação entrelaçada** (4)</span><span class="sxs-lookup"><span data-stu-id="04a55-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="04a55-221">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="04a55-221">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-222">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04a55-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04a55-224">Qualificadores: **unidades** ("pixels")</span><span class="sxs-lookup"><span data-stu-id="04a55-224">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="04a55-225">O número atual de pixels verticais.</span><span class="sxs-lookup"><span data-stu-id="04a55-225">The current number of vertical pixels.</span></span> <span data-ttu-id="04a55-226">Essa propriedade é herdada do [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-226">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-227">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="04a55-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-230">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="04a55-230">A description of the object.</span></span> <span data-ttu-id="04a55-231">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-232">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="04a55-232">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-233">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-235">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="04a55-235">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="04a55-236">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="04a55-236">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="04a55-237">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="04a55-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="04a55-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="04a55-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="04a55-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="04a55-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="04a55-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="04a55-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="04a55-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="04a55-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="04a55-246">)</span><span class="sxs-lookup"><span data-stu-id="04a55-246">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="04a55-247">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="04a55-247">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-250">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como "Microsoft:*GUID* \\ Head \\ *index*".</span><span class="sxs-lookup"><span data-stu-id="04a55-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\Head\\*Index*".</span></span>

</dd> <dt>

<span data-ttu-id="04a55-251">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="04a55-251">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-254">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="04a55-254">A display name for the object.</span></span> <span data-ttu-id="04a55-255">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-256">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="04a55-256">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-257">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-259">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="04a55-259">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="04a55-260">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="04a55-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="04a55-261">Valor</span><span class="sxs-lookup"><span data-stu-id="04a55-261">Value</span></span>                                                                        | <span data-ttu-id="04a55-262">Significado</span><span class="sxs-lookup"><span data-stu-id="04a55-262">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="04a55-263"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="04a55-263"><dt>2</dt></span></span> </dl> | <span data-ttu-id="04a55-264">habilitado</span><span class="sxs-lookup"><span data-stu-id="04a55-264">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="04a55-265"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="04a55-265"><dt>3</dt></span></span> </dl> | <span data-ttu-id="04a55-266">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="04a55-266">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="04a55-267">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="04a55-267">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-268">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-270">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="04a55-270">The enabled and disabled states of an element.</span></span> <span data-ttu-id="04a55-271">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="04a55-271">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="04a55-272">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-272">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="04a55-273">Valor</span><span class="sxs-lookup"><span data-stu-id="04a55-273">Value</span></span>                                                                        | <span data-ttu-id="04a55-274">Significado</span><span class="sxs-lookup"><span data-stu-id="04a55-274">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="04a55-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="04a55-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="04a55-276">habilitado</span><span class="sxs-lookup"><span data-stu-id="04a55-276">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="04a55-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="04a55-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="04a55-278">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="04a55-278">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="04a55-279">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="04a55-279">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-280">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="04a55-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-282">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="04a55-282">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="04a55-283">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="04a55-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-284">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="04a55-284">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-285">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-287">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="04a55-287">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="04a55-288">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="04a55-288">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-289">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="04a55-289">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-290">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-292">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="04a55-292">The current health of the element.</span></span> <span data-ttu-id="04a55-293">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="04a55-293">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="04a55-294">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="04a55-294">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="04a55-295">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="04a55-296">Valor</span><span class="sxs-lookup"><span data-stu-id="04a55-296">Value</span></span>                                                                        | <span data-ttu-id="04a55-297">Significado</span><span class="sxs-lookup"><span data-stu-id="04a55-297">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="04a55-298"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="04a55-298"><dt>5</dt></span></span> </dl> | <span data-ttu-id="04a55-299">OK</span><span class="sxs-lookup"><span data-stu-id="04a55-299">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="04a55-300">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="04a55-300">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-301">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-301">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="04a55-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-303">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz de propriedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="04a55-303">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="04a55-304">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="04a55-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="04a55-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-306">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="04a55-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-308">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="04a55-308">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="04a55-309">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-310">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="04a55-310">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-311">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04a55-313">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="04a55-313">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="04a55-314">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="04a55-314">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="04a55-315">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-315">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-316">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="04a55-316">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-317">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04a55-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-319">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="04a55-319">The last error code reported by the logical device.</span></span> <span data-ttu-id="04a55-320">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="04a55-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-321">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="04a55-321">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-322">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="04a55-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-324">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="04a55-324">This property has been deprecated.</span></span> <span data-ttu-id="04a55-325">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="04a55-325">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-326">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="04a55-326">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-327">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04a55-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04a55-329">Qualificadores: **unidades** ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="04a55-329">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="04a55-330">A taxa de atualização máxima do controlador de vídeo, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="04a55-330">The maximum refresh rate of the display controller, in hertz.</span></span> <span data-ttu-id="04a55-331">Essa propriedade é herdada do [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-331">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-332">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="04a55-332">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-333">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04a55-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04a55-335">Qualificadores: **unidades** ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="04a55-335">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="04a55-336">A taxa de atualização mínima do controlador de vídeo, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="04a55-336">The minimum refresh rate of the video controller, in hertz.</span></span> <span data-ttu-id="04a55-337">Essa propriedade é herdada do [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-337">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-338">**Nome**</span><span class="sxs-lookup"><span data-stu-id="04a55-338">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-339">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-341">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="04a55-341">The label by which the object is known.</span></span> <span data-ttu-id="04a55-342">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é a mesma que a propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="04a55-342">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-343">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="04a55-343">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-344">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-346">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="04a55-346">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="04a55-347">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="04a55-347">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="04a55-348">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="04a55-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="04a55-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="04a55-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="04a55-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="04a55-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="04a55-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="04a55-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="04a55-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="04a55-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="04a55-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="04a55-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="04a55-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="04a55-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="04a55-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="04a55-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="04a55-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="04a55-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="04a55-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="04a55-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="04a55-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="04a55-368">)</span><span class="sxs-lookup"><span data-stu-id="04a55-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="04a55-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="04a55-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-370">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="04a55-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-372">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="04a55-372">The current statuses of the object.</span></span> <span data-ttu-id="04a55-373">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-374">**OtherCurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="04a55-374">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-375">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-377">O modo de verificação atual quando a propriedade **CurrentScanMode** da instância é 1 (outra).</span><span class="sxs-lookup"><span data-stu-id="04a55-377">The current scan mode when the instance's **CurrentScanMode** property is 1 (Other).</span></span> <span data-ttu-id="04a55-378">Essa propriedade é herdada de [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)) e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="04a55-378">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-379">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="04a55-379">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-380">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-382">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="04a55-382">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="04a55-383">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="04a55-383">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="04a55-384">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="04a55-384">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-385">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="04a55-385">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-386">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="04a55-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-388">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="04a55-388">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="04a55-389">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="04a55-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-390">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="04a55-390">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-391">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="04a55-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-393">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04a55-393">The power management capabilities of the device.</span></span> <span data-ttu-id="04a55-394">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="04a55-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="04a55-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-396">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="04a55-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-398">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="04a55-398">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="04a55-399">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="04a55-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-400">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="04a55-400">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-401">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="04a55-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-403">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="04a55-403">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="04a55-404">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="04a55-404">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-405">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="04a55-405">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-406">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-408">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="04a55-408">Provides high level status information.</span></span> <span data-ttu-id="04a55-409">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="04a55-409">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="04a55-410">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="04a55-410">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="04a55-411">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="04a55-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="04a55-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-413"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="04a55-413"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="04a55-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="04a55-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="04a55-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="04a55-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="04a55-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="04a55-418">)</span><span class="sxs-lookup"><span data-stu-id="04a55-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="04a55-419">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="04a55-419">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-420">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-422">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="04a55-422">The last requested or desired state for the element.</span></span> <span data-ttu-id="04a55-423">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="04a55-423">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="04a55-424">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-424">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="04a55-425">Valor</span><span class="sxs-lookup"><span data-stu-id="04a55-425">Value</span></span>                                                                         | <span data-ttu-id="04a55-426">Significado</span><span class="sxs-lookup"><span data-stu-id="04a55-426">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="04a55-427"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="04a55-427"><dt>12</dt></span></span> </dl> | <span data-ttu-id="04a55-428">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="04a55-428">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="04a55-429">**Status**</span><span class="sxs-lookup"><span data-stu-id="04a55-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-430">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-432">Uma cadeia de caracteres que especifica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="04a55-432">A string that specifies the current status of the object.</span></span> <span data-ttu-id="04a55-433">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="04a55-433">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-434">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="04a55-434">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-435">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="04a55-436">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-437">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="04a55-437">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="04a55-438">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="04a55-438">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-439">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="04a55-439">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-440">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-442">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="04a55-442">The current state of the logical device.</span></span> <span data-ttu-id="04a55-443">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="04a55-443">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-444">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="04a55-444">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-445">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-447">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="04a55-447">The scoping system's creation class name.</span></span> <span data-ttu-id="04a55-448">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="04a55-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-449">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="04a55-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-450">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04a55-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-452">O identificador exclusivo para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="04a55-452">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="04a55-453">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="04a55-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="04a55-454">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="04a55-454">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-455">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="04a55-455">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-456">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-457">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="04a55-457">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="04a55-458">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="04a55-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-459">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="04a55-459">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-460">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="04a55-460">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-461">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-462">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="04a55-462">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="04a55-463">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="04a55-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="04a55-464">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="04a55-464">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04a55-465">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04a55-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04a55-466">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04a55-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04a55-467">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="04a55-467">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="04a55-468">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04a55-468">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="04a55-469">Valor</span><span class="sxs-lookup"><span data-stu-id="04a55-469">Value</span></span>                                                                         | <span data-ttu-id="04a55-470">Significado</span><span class="sxs-lookup"><span data-stu-id="04a55-470">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="04a55-471"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="04a55-471"><dt>12</dt></span></span> </dl> | <span data-ttu-id="04a55-472">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="04a55-472">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04a55-473">Comentários</span><span class="sxs-lookup"><span data-stu-id="04a55-473">Remarks</span></span>

<span data-ttu-id="04a55-474">O acesso à classe **Msvm \_ VideoHead** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="04a55-474">Access to the **Msvm\_VideoHead** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="04a55-475">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="04a55-475">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="04a55-476">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04a55-476">Requirements</span></span>



| <span data-ttu-id="04a55-477">Requisito</span><span class="sxs-lookup"><span data-stu-id="04a55-477">Requirement</span></span> | <span data-ttu-id="04a55-478">Valor</span><span class="sxs-lookup"><span data-stu-id="04a55-478">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04a55-479">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04a55-479">Minimum supported client</span></span><br/> | <span data-ttu-id="04a55-480">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="04a55-480">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="04a55-481">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04a55-481">Minimum supported server</span></span><br/> | <span data-ttu-id="04a55-482">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="04a55-482">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04a55-483">Namespace</span><span class="sxs-lookup"><span data-stu-id="04a55-483">Namespace</span></span><br/>                | <span data-ttu-id="04a55-484">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="04a55-484">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="04a55-485">MOF</span><span class="sxs-lookup"><span data-stu-id="04a55-485">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04a55-486"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04a55-486"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04a55-487">DLL</span><span class="sxs-lookup"><span data-stu-id="04a55-487">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04a55-488"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04a55-488"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="04a55-489">Confira também</span><span class="sxs-lookup"><span data-stu-id="04a55-489">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a55-490">**\_VIDEOHEAD CIM**</span><span class="sxs-lookup"><span data-stu-id="04a55-490">**CIM\_VideoHead**</span></span>](cim-videohead.md)
</dt> <dt>

<span data-ttu-id="04a55-491">[**\_VIDEOHEAD CIM**](/previous-versions//cc136948(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="04a55-491">[**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="04a55-492">Classes de vídeo</span><span class="sxs-lookup"><span data-stu-id="04a55-492">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

