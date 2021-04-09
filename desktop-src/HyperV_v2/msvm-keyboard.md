---
description: Representa um dispositivo de teclado.
ms.assetid: 2a59fe90-12e2-471c-b49e-dfb4f4a31e0c
title: Classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard
- Msvm_Keyboard.SetPowerState
- Msvm_Keyboard.EnableDevice
- Msvm_Keyboard.OnlineDevice
- Msvm_Keyboard.QuiesceDevice
- Msvm_Keyboard.SaveProperties
- Msvm_Keyboard.RestoreProperties
- Msvm_Keyboard.InstanceID
- Msvm_Keyboard.Caption
- Msvm_Keyboard.Description
- Msvm_Keyboard.ElementName
- Msvm_Keyboard.InstallDate
- Msvm_Keyboard.Name
- Msvm_Keyboard.OperationalStatus
- Msvm_Keyboard.StatusDescriptions
- Msvm_Keyboard.Status
- Msvm_Keyboard.HealthState
- Msvm_Keyboard.CommunicationStatus
- Msvm_Keyboard.DetailedStatus
- Msvm_Keyboard.OperatingStatus
- Msvm_Keyboard.PrimaryStatus
- Msvm_Keyboard.EnabledState
- Msvm_Keyboard.OtherEnabledState
- Msvm_Keyboard.RequestedState
- Msvm_Keyboard.EnabledDefault
- Msvm_Keyboard.TimeOfLastStateChange
- Msvm_Keyboard.AvailableRequestedStates
- Msvm_Keyboard.TransitioningToState
- Msvm_Keyboard.SystemCreationClassName
- Msvm_Keyboard.SystemName
- Msvm_Keyboard.CreationClassName
- Msvm_Keyboard.DeviceID
- Msvm_Keyboard.PowerManagementSupported
- Msvm_Keyboard.PowerManagementCapabilities
- Msvm_Keyboard.Availability
- Msvm_Keyboard.StatusInfo
- Msvm_Keyboard.LastErrorCode
- Msvm_Keyboard.ErrorDescription
- Msvm_Keyboard.ErrorCleared
- Msvm_Keyboard.OtherIdentifyingInfo
- Msvm_Keyboard.PowerOnHours
- Msvm_Keyboard.TotalPowerOnHours
- Msvm_Keyboard.IdentifyingDescriptions
- Msvm_Keyboard.AdditionalAvailability
- Msvm_Keyboard.MaxQuiesceTime
- Msvm_Keyboard.IsLocked
- Msvm_Keyboard.Layout
- Msvm_Keyboard.NumberOfFunctionKeys
- Msvm_Keyboard.Password
- Msvm_Keyboard.UnicodeSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37c4faceb9072c1851868eb23c031e715cb6e1c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011000"
---
# <a name="msvm_keyboard-class"></a><span data-ttu-id="40590-103">\_Classe de teclado Msvm</span><span class="sxs-lookup"><span data-stu-id="40590-103">Msvm\_Keyboard class</span></span>

<span data-ttu-id="40590-104">Representa um dispositivo de teclado.</span><span class="sxs-lookup"><span data-stu-id="40590-104">Represents a keyboard device.</span></span> <span data-ttu-id="40590-105">Os teclados são dispositivos lógicos que estão sempre presentes em uma máquina virtual e, portanto, não são alocados por meio de um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="40590-105">Keyboards are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="40590-106">Uma instância está sempre presente em um sistema de computador virtual.</span><span class="sxs-lookup"><span data-stu-id="40590-106">One instance is always present in a virtual computer system.</span></span>

<span data-ttu-id="40590-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="40590-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="40590-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40590-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Keyboard : CIM_UserDevice
{
  string   InstanceID;
  string   Caption = "Keyboard";
  string   Description = "Microsoft Virtual Keyboard";
  string   ElementName = "Keyboard";
  datetime InstallDate;
  string   Name = "Keyboard";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_Keyboard";
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
  boolean  IsLocked = False;
  string   Layout = "00000409";
  uint16   NumberOfFunctionKeys = 12;
  uint16   Password = 5;
  boolean  UnicodeSupported;
};
```

## <a name="members"></a><span data-ttu-id="40590-109">Membros</span><span class="sxs-lookup"><span data-stu-id="40590-109">Members</span></span>

<span data-ttu-id="40590-110">A classe de **\_ teclado Msvm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="40590-110">The **Msvm\_Keyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="40590-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="40590-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="40590-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="40590-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="40590-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="40590-113">Methods</span></span>

<span data-ttu-id="40590-114">A classe de **\_ teclado Msvm** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="40590-114">The **Msvm\_Keyboard** class has these methods.</span></span>



| <span data-ttu-id="40590-115">Método</span><span class="sxs-lookup"><span data-stu-id="40590-115">Method</span></span>                                                         | <span data-ttu-id="40590-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="40590-116">Description</span></span>                                                   |
|:---------------------------------------------------------------|:--------------------------------------------------------------|
| <span data-ttu-id="40590-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="40590-117">**EnableDevice**</span></span>                                               | <span data-ttu-id="40590-118">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="40590-118">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="40590-119">**Iskeypressd**</span><span class="sxs-lookup"><span data-stu-id="40590-119">**IsKeyPressed**</span></span>](iskeypressed-msvm-keyboard.md)             | <span data-ttu-id="40590-120">Recupera o estado de chave de uma chave.</span><span class="sxs-lookup"><span data-stu-id="40590-120">Retrieves the key state of a key.</span></span><br/>                  |
| <span data-ttu-id="40590-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="40590-121">**OnlineDevice**</span></span>                                               | <span data-ttu-id="40590-122">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="40590-122">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="40590-123">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="40590-123">**PressKey**</span></span>](presskey-msvm-keyboard.md)                     | <span data-ttu-id="40590-124">Simula um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="40590-124">Simulates a key press.</span></span><br/>                             |
| <span data-ttu-id="40590-125">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="40590-125">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="40590-126">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="40590-126">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="40590-127">**ReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="40590-127">**ReleaseKey**</span></span>](releasekey-msvm-keyboard.md)                 | <span data-ttu-id="40590-128">Simula uma versão de chave.</span><span class="sxs-lookup"><span data-stu-id="40590-128">Simulates a key release.</span></span><br/>                           |
| [<span data-ttu-id="40590-129">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="40590-129">**RequestStateChange**</span></span>](msvm-keyboard-requeststatechange.md) | <span data-ttu-id="40590-130">Solicita que o estado do elemento seja alterado.</span><span class="sxs-lookup"><span data-stu-id="40590-130">Requests that the state of the element be changed.</span></span><br/> |
| [<span data-ttu-id="40590-131">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="40590-131">**Reset**</span></span>](msvm-keyboard-reset.md)                           | <span data-ttu-id="40590-132">Redefine o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="40590-132">Resets the virtual keyboard.</span></span><br/>                       |
| <span data-ttu-id="40590-133">**Restaurarproperties**</span><span class="sxs-lookup"><span data-stu-id="40590-133">**RestoreProperties**</span></span>                                          | <span data-ttu-id="40590-134">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="40590-134">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="40590-135">**Salvarproperties**</span><span class="sxs-lookup"><span data-stu-id="40590-135">**SaveProperties**</span></span>                                             | <span data-ttu-id="40590-136">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="40590-136">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="40590-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="40590-137">**SetPowerState**</span></span>                                              | <span data-ttu-id="40590-138">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="40590-138">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="40590-139">**TypeCtrlAltDel**</span><span class="sxs-lookup"><span data-stu-id="40590-139">**TypeCtrlAltDel**</span></span>](typectrlaltdel-msvm-keyboard.md)         | <span data-ttu-id="40590-140">Simula uma sequência de teclas Ctrl + Alt + Del.</span><span class="sxs-lookup"><span data-stu-id="40590-140">Simulates a Ctrl+Alt+Del key sequence.</span></span><br/>             |
| [<span data-ttu-id="40590-141">**TypeKey**</span><span class="sxs-lookup"><span data-stu-id="40590-141">**TypeKey**</span></span>](typekey-msvm-keyboard.md)                       | <span data-ttu-id="40590-142">Simula uma sequência de teclas de liberação de prensa.</span><span class="sxs-lookup"><span data-stu-id="40590-142">Simulates a press-release key sequence.</span></span><br/>            |
| [<span data-ttu-id="40590-143">**TypeScancodes**</span><span class="sxs-lookup"><span data-stu-id="40590-143">**TypeScancodes**</span></span>](msvm-keyboard-typescancodes.md)           | <span data-ttu-id="40590-144">Simula uma sequência de chaves usando códigos de verificação.</span><span class="sxs-lookup"><span data-stu-id="40590-144">Simulates a key sequence using scan codes.</span></span><br/>         |
| [<span data-ttu-id="40590-145">**TypeText**</span><span class="sxs-lookup"><span data-stu-id="40590-145">**TypeText**</span></span>](typetext-msvm-keyboard.md)                     | <span data-ttu-id="40590-146">Simula uma série de caracteres digitados.</span><span class="sxs-lookup"><span data-stu-id="40590-146">Simulates a series of typed characters.</span></span><br/>            |



 

### <a name="properties"></a><span data-ttu-id="40590-147">Propriedades</span><span class="sxs-lookup"><span data-stu-id="40590-147">Properties</span></span>

<span data-ttu-id="40590-148">A classe de **\_ teclado Msvm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="40590-148">The **Msvm\_Keyboard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40590-149">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="40590-149">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-150">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="40590-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-152">Qualquer disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="40590-152">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="40590-153">A propriedade de **disponibilidade** denota o status primário e a disponibilidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40590-153">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="40590-154">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="40590-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="40590-155">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="40590-155">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-156">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-158">A disponibilidade e o status principais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40590-158">The primary availability and status of the device.</span></span> <span data-ttu-id="40590-159">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="40590-159">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="40590-160">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="40590-160">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-161">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="40590-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-163">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="40590-163">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="40590-164">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="40590-164">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="40590-165">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="40590-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40590-168">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="40590-168">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="40590-169">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="40590-169">A short description of the object.</span></span> <span data-ttu-id="40590-170">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="40590-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="40590-171">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="40590-171">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-172">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-174">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="40590-174">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="40590-175">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="40590-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="40590-176">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="40590-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="40590-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="40590-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="40590-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="40590-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="40590-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="40590-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="40590-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="40590-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="40590-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="40590-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="40590-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="40590-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="40590-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="40590-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="40590-184">)</span><span class="sxs-lookup"><span data-stu-id="40590-184">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40590-185">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="40590-185">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40590-188">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="40590-188">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="40590-189">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="40590-189">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="40590-190">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="40590-190">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="40590-191">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="40590-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="40590-192">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="40590-192">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-195">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="40590-195">A description of the object.</span></span> <span data-ttu-id="40590-196">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="40590-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="40590-197">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="40590-197">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-198">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-200">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="40590-200">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="40590-201">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="40590-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="40590-202">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="40590-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="40590-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="40590-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="40590-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="40590-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="40590-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="40590-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="40590-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="40590-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="40590-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="40590-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="40590-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="40590-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="40590-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="40590-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="40590-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="40590-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="40590-211">)</span><span class="sxs-lookup"><span data-stu-id="40590-211">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40590-212">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="40590-212">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-215">Um endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="40590-215">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="40590-216">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é sempre definida como "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="40590-216">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="40590-217">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="40590-217">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-218">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-220">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="40590-220">A display name for the object.</span></span> <span data-ttu-id="40590-221">Essa propriedade permite que cada instância defina um nome de exibição além de suas propriedades de chave, dados de identidade e informações de descrição.</span><span class="sxs-lookup"><span data-stu-id="40590-221">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="40590-222">A propriedade [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) da classe **CIM \_ ManagedSystemElement** também é definida como um nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="40590-222">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="40590-223">Mas, muitas vezes, é uma subclasse para ser uma chave.</span><span class="sxs-lookup"><span data-stu-id="40590-223">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="40590-224">Não é razoável que a mesma propriedade possa transmitir a identidade e um nome de exibição, sem inconsistências.</span><span class="sxs-lookup"><span data-stu-id="40590-224">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="40590-225">Onde **Name** existe e não é uma chave (como para instâncias de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), as mesmas informações podem estar presentes nas propriedades **Name** e **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="40590-225">Where **Name** exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="40590-226">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="40590-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="40590-227">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="40590-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-228">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-230">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="40590-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="40590-231">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="40590-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="40590-232">Valor</span><span class="sxs-lookup"><span data-stu-id="40590-232">Value</span></span>                                                                        | <span data-ttu-id="40590-233">Significado</span><span class="sxs-lookup"><span data-stu-id="40590-233">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="40590-234"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="40590-234"><dt>2</dt></span></span> </dl> | <span data-ttu-id="40590-235">habilitado</span><span class="sxs-lookup"><span data-stu-id="40590-235">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="40590-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="40590-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-237">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-239">Indica os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="40590-239">Indicates the enabled and disabled states of an element.</span></span> <span data-ttu-id="40590-240">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="40590-240">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="40590-241">Por exemplo, desligar (valor = 4) e iniciar (valor = 10) são estados transitórios entre habilitado e desabilitado.</span><span class="sxs-lookup"><span data-stu-id="40590-241">For example, shutting down (value=4) and starting (value=10) are transient states between enabled and disabled.</span></span>



| <span data-ttu-id="40590-242">Valor</span><span class="sxs-lookup"><span data-stu-id="40590-242">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="40590-243">Significado</span><span class="sxs-lookup"><span data-stu-id="40590-243">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="40590-244"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="40590-244"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="40590-245">Unknown</span><span class="sxs-lookup"><span data-stu-id="40590-245">Unknown</span></span><br/>                                                                                                                                                                                              |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="40590-246"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="40590-246"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="40590-247">Outro</span><span class="sxs-lookup"><span data-stu-id="40590-247">Other</span></span><br/>                                                                                                                                                                                                |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="40590-248"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="40590-248"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="40590-249">O elemento é ou pode estar executando comandos, processará qualquer comando na fila e enfileirará novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="40590-249">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="40590-250"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="40590-250"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="40590-251">O elemento não executará comandos e descartará as novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="40590-251">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="40590-252"><dt>**Desligando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="40590-252"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="40590-253">O elemento está no processo de ir para um estado desabilitado.</span><span class="sxs-lookup"><span data-stu-id="40590-253">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="40590-254"><dt>**Não aplicável**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="40590-254"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="40590-255">O elemento não dá suporte a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="40590-255">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="40590-256"><dt>**Habilitado, mas offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="40590-256"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="40590-257">O elemento pode estar concluindo comandos e descartará novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="40590-257">The element might be completing commands and will drop any new requests.</span></span><br/>                                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="40590-258"><dt>**No teste**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="40590-258"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="40590-259">O elemento está em um estado de teste.</span><span class="sxs-lookup"><span data-stu-id="40590-259">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="40590-260"><dt>**Adiado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="40590-260"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="40590-261">O elemento pode estar concluindo comandos, mas colocará todas as novas solicitações na fila.</span><span class="sxs-lookup"><span data-stu-id="40590-261">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="40590-262"><dt>**Desativar**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="40590-262"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="40590-263">O elemento está habilitado, mas em um modo restrito.</span><span class="sxs-lookup"><span data-stu-id="40590-263">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="40590-264">O comportamento do elemento é semelhante ao estado habilitado (2), mas processa apenas um conjunto restrito de comandos.</span><span class="sxs-lookup"><span data-stu-id="40590-264">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="40590-265">Todas as outras solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="40590-265">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="40590-266"><dt>**Iniciando**</dt> em <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="40590-266"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="40590-267">O elemento está no processo de ir para um estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="40590-267">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="40590-268">Novas solicitações são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="40590-268">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="40590-269"><dt>**DMTF reservado**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="40590-269"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="40590-270">Esse valor é reservado.</span><span class="sxs-lookup"><span data-stu-id="40590-270">This value is reserved.</span></span><br/>                                                                                                                                                                              |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="40590-271"><dt>**Fornecedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="40590-271"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="40590-272">Esse valor é reservado.</span><span class="sxs-lookup"><span data-stu-id="40590-272">This value is reserved.</span></span><br/>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="40590-273">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="40590-273">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-274">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="40590-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40590-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-276">Indica se o erro relatado em **LastErrorCode** agora está limpo.</span><span class="sxs-lookup"><span data-stu-id="40590-276">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="40590-277">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="40590-277">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="40590-278">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="40590-278">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-281">Uma cadeia de caracteres que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="40590-281">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="40590-282">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="40590-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="40590-283">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="40590-283">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-284">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-286">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="40590-286">The current health of the element.</span></span> <span data-ttu-id="40590-287">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="40590-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="40590-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="40590-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-289">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="40590-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-291">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="40590-291">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="40590-292">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="40590-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="40590-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="40590-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-294">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="40590-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="40590-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-296">A data e a hora em que a máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="40590-296">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="40590-297">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="40590-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="40590-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="40590-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-299">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40590-301">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="40590-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="40590-302">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="40590-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="40590-303">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="40590-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="40590-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="40590-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-305">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="40590-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40590-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-307">Indica se o dispositivo está bloqueado, impedindo a entrada ou saída do usuário.</span><span class="sxs-lookup"><span data-stu-id="40590-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="40590-308">Essa propriedade é herdada [**do \_ userdevice do CIM**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="40590-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="40590-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="40590-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-310">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40590-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40590-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-312">O último código de erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="40590-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="40590-313">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="40590-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="40590-314">**Layout**</span><span class="sxs-lookup"><span data-stu-id="40590-314">**Layout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-315">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-317">Uma cadeia de caracteres que indica o formato e o layout do teclado.</span><span class="sxs-lookup"><span data-stu-id="40590-317">A string indicating the format and layout of the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="40590-318">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="40590-318">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-319">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="40590-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="40590-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-321">Essa propriedade foi substituída.</span><span class="sxs-lookup"><span data-stu-id="40590-321">This property has been deprecated.</span></span> <span data-ttu-id="40590-322">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="40590-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="40590-323">**Nome**</span><span class="sxs-lookup"><span data-stu-id="40590-323">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40590-326">Qualificadores: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="40590-326">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="40590-327">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="40590-327">The label by which the object is known.</span></span> <span data-ttu-id="40590-328">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="40590-328">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="40590-329">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="40590-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="40590-330">**NumberOfFunctionKeys**</span><span class="sxs-lookup"><span data-stu-id="40590-330">**NumberOfFunctionKeys**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-331">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-333">O número de teclas de função no teclado.</span><span class="sxs-lookup"><span data-stu-id="40590-333">The number of function keys on the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="40590-334">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="40590-334">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-335">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-337">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="40590-337">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="40590-338">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="40590-338">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="40590-339">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="40590-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="40590-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="40590-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="40590-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="40590-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="40590-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="40590-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="40590-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="40590-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="40590-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="40590-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="40590-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="40590-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="40590-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="40590-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="40590-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="40590-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="40590-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="40590-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="40590-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="40590-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="40590-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="40590-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="40590-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="40590-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="40590-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="40590-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="40590-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="40590-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="40590-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="40590-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="40590-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="40590-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="40590-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="40590-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="40590-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="40590-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="40590-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="40590-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="40590-359">)</span><span class="sxs-lookup"><span data-stu-id="40590-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40590-360">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="40590-360">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-361">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="40590-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-363">O status atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="40590-363">The current status of the element.</span></span> <span data-ttu-id="40590-364">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="40590-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="40590-365">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="40590-365">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-366">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-368">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="40590-368">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="40590-369">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="40590-369">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="40590-370">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="40590-370">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="40590-371">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="40590-371">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-372">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-372">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="40590-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-374">Quaisquer dados adicionais, além das informações de ID do dispositivo, que podem ser usadas para identificar um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="40590-374">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="40590-375">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="40590-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="40590-376">**Senha**</span><span class="sxs-lookup"><span data-stu-id="40590-376">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-377">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-379">Indica se uma senha de nível de hardware está habilitada no teclado, impedindo a entrada local.</span><span class="sxs-lookup"><span data-stu-id="40590-379">Indicates whether a hardware-level password is enabled at the keyboard, preventing local input.</span></span>

<dt>

<span data-ttu-id="40590-380">5</span><span class="sxs-lookup"><span data-stu-id="40590-380">5</span></span>
</dt> <dd>

<span data-ttu-id="40590-381">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="40590-381">Not implemented.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40590-382">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="40590-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-383">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="40590-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-385">Os recursos de gerenciamento de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40590-385">The power management capabilities of the device.</span></span> <span data-ttu-id="40590-386">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="40590-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="40590-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="40590-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-388">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="40590-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40590-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-390">Indica se o dispositivo pode ser gerenciado por energia.</span><span class="sxs-lookup"><span data-stu-id="40590-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="40590-391">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="40590-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="40590-392">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="40590-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-393">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="40590-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="40590-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-395">O número de horas consecutivas em que este dispositivo foi ligado desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="40590-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="40590-396">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="40590-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="40590-397">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="40590-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-398">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-400">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="40590-400">Provides high level status information.</span></span> <span data-ttu-id="40590-401">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="40590-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="40590-402">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="40590-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="40590-403">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="40590-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="40590-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="40590-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="40590-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="40590-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="40590-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="40590-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="40590-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="40590-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="40590-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="40590-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="40590-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="40590-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="40590-410">)</span><span class="sxs-lookup"><span data-stu-id="40590-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40590-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="40590-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-412">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-414">O último estado solicitado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="40590-414">The last requested state for the element.</span></span>



| <span data-ttu-id="40590-415">Valor</span><span class="sxs-lookup"><span data-stu-id="40590-415">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="40590-416">Significado</span><span class="sxs-lookup"><span data-stu-id="40590-416">Meaning</span></span>                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="40590-417"><dt>**Não aplicável**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="40590-417"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="40590-418">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="40590-418">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="40590-419">**Status**</span><span class="sxs-lookup"><span data-stu-id="40590-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-420">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-422">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="40590-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="40590-423">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="40590-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-424">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="40590-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-426">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="40590-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="40590-427">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "OK".</span><span class="sxs-lookup"><span data-stu-id="40590-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="40590-428">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="40590-428">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-429">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-431">O estado atual do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="40590-431">The current state of the logical device.</span></span> <span data-ttu-id="40590-432">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="40590-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="40590-433">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="40590-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40590-436">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="40590-436">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="40590-437">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="40590-437">The scoping system's creation class name.</span></span> <span data-ttu-id="40590-438">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)e é definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="40590-438">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="40590-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="40590-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-440">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="40590-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40590-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40590-442">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="40590-442">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="40590-443">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="40590-443">The scoping system's name.</span></span> <span data-ttu-id="40590-444">Esse valor corresponde ao valor da propriedade **Name** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) para a máquina virtual de escopo.</span><span class="sxs-lookup"><span data-stu-id="40590-444">This value corresponds to the value of the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for the scoping virtual machine.</span></span> <span data-ttu-id="40590-445">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="40590-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="40590-446">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="40590-446">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-447">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="40590-447">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="40590-448">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-449">A data e a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="40590-449">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="40590-450">Se o estado do elemento não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo de 0.</span><span class="sxs-lookup"><span data-stu-id="40590-450">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="40590-451">Se uma alteração de estado foi solicitada, mas rejeitada ou ainda não processada, a propriedade não deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="40590-451">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="40590-452">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="40590-452">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="40590-453">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="40590-453">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-454">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="40590-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="40590-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-456">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="40590-456">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="40590-457">Essa propriedade é herdada [**do \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="40590-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="40590-458">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="40590-458">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-459">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40590-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40590-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-461">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="40590-461">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="40590-462">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="40590-462">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="40590-463">**UnicodeSupported**</span><span class="sxs-lookup"><span data-stu-id="40590-463">**UnicodeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40590-464">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="40590-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40590-465">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="40590-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40590-466">Indica se o teclado virtual dá suporte a caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="40590-466">Indicates if the virtual keyboard supports Unicode characters.</span></span> <span data-ttu-id="40590-467">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="40590-467">This can be one of the following values.</span></span>



| <span data-ttu-id="40590-468">Valor</span><span class="sxs-lookup"><span data-stu-id="40590-468">Value</span></span>                                                                            | <span data-ttu-id="40590-469">Significado</span><span class="sxs-lookup"><span data-stu-id="40590-469">Meaning</span></span>                                                              |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="40590-470"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="40590-470"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="40590-471">O teclado virtual dá suporte a caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="40590-471">The virtual keyboard supports Unicode characters.</span></span><br/>         |
| <dl> <span data-ttu-id="40590-472"><dt>Falso</dt></span><span class="sxs-lookup"><span data-stu-id="40590-472"><dt>False</dt></span></span> </dl> | <span data-ttu-id="40590-473">O teclado virtual não oferece suporte a caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="40590-473">The virtual keyboard does not support Unicode characters.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40590-474">Comentários</span><span class="sxs-lookup"><span data-stu-id="40590-474">Remarks</span></span>

<span data-ttu-id="40590-475">O acesso à classe de **\_ teclado Msvm** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="40590-475">Access to the **Msvm\_Keyboard** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="40590-476">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="40590-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="40590-477">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40590-477">Requirements</span></span>



| <span data-ttu-id="40590-478">Requisito</span><span class="sxs-lookup"><span data-stu-id="40590-478">Requirement</span></span> | <span data-ttu-id="40590-479">Valor</span><span class="sxs-lookup"><span data-stu-id="40590-479">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40590-480">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40590-480">Minimum supported client</span></span><br/> | <span data-ttu-id="40590-481">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="40590-481">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="40590-482">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40590-482">Minimum supported server</span></span><br/> | <span data-ttu-id="40590-483">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="40590-483">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40590-484">Namespace</span><span class="sxs-lookup"><span data-stu-id="40590-484">Namespace</span></span><br/>                | <span data-ttu-id="40590-485">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="40590-485">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="40590-486">MOF</span><span class="sxs-lookup"><span data-stu-id="40590-486">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40590-487"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40590-487"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="40590-488">DLL</span><span class="sxs-lookup"><span data-stu-id="40590-488">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40590-489"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="40590-489"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="40590-490">Confira também</span><span class="sxs-lookup"><span data-stu-id="40590-490">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40590-491">**Userdevice do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="40590-491">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dt>

[<span data-ttu-id="40590-492">**Userdevice do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="40590-492">**CIM\_UserDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-userdevice)
</dt> <dt>

[<span data-ttu-id="40590-493">Classes de entrada</span><span class="sxs-lookup"><span data-stu-id="40590-493">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

