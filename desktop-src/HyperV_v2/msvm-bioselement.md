---
description: Representa o software de nível baixo que é carregado na RAM para configurar e iniciar o sistema.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Classe Msvm_BIOSElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8d36ea50791bf6f1413815583fe1168f564d50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827387"
---
# <a name="msvm_bioselement-class"></a><span data-ttu-id="d66f1-103">\_Classe bioselement Msvm</span><span class="sxs-lookup"><span data-stu-id="d66f1-103">Msvm\_BIOSElement class</span></span>

<span data-ttu-id="d66f1-104">Representa o software de nível baixo que é carregado na RAM para configurar e iniciar o sistema.</span><span class="sxs-lookup"><span data-stu-id="d66f1-104">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span> <span data-ttu-id="d66f1-105">O BIOS não é um dispositivo lógico, portanto, o BIOS virtual não deve ser considerado um dispositivo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d66f1-105">The BIOS is not a logical device, hence the virtual BIOS should not be thought of as a virtual machine device.</span></span> <span data-ttu-id="d66f1-106">Como não é um dispositivo, ele não tem um pool de recursos correspondente.</span><span class="sxs-lookup"><span data-stu-id="d66f1-106">As it is not a device, it does not have a corresponding resource pool.</span></span> <span data-ttu-id="d66f1-107">O objeto BIOS é associado à máquina virtual por meio da Associação [**Msvm \_ SystemBIOS**](msvm-systembios.md) .</span><span class="sxs-lookup"><span data-stu-id="d66f1-107">The BIOS object is associated with the virtual machine through the [**Msvm\_SystemBIOS**](msvm-systembios.md) association.</span></span>

<span data-ttu-id="d66f1-108">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d66f1-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d66f1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d66f1-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a><span data-ttu-id="d66f1-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d66f1-110">Members</span></span>

<span data-ttu-id="d66f1-111">A **classe \_ bioselement Msvm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d66f1-111">The **Msvm\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="d66f1-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d66f1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d66f1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d66f1-113">Properties</span></span>

<span data-ttu-id="d66f1-114">A **classe \_ bioselement Msvm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d66f1-114">The **Msvm\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d66f1-115">**BaseBoardSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d66f1-115">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-118">O número de série da placa base na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d66f1-118">The serial number for the base board on the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-119">**BIOSGUID**</span><span class="sxs-lookup"><span data-stu-id="d66f1-119">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-122">O identificador exclusivo para o BIOS.</span><span class="sxs-lookup"><span data-stu-id="d66f1-122">The unique identifier for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-123">**BIOSNumLock**</span><span class="sxs-lookup"><span data-stu-id="d66f1-123">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-124">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d66f1-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-126">O estado habilitado do bloqueio num no BIOS.</span><span class="sxs-lookup"><span data-stu-id="d66f1-126">The enabled state of the Num Lock in the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-127">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d66f1-127">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-130">O número de série do BIOS.</span><span class="sxs-lookup"><span data-stu-id="d66f1-130">The serial number for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-131">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="d66f1-131">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-132">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d66f1-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-134">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="d66f1-134">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-135">A ordem em que os dispositivos serão pesquisados em um setor de inicialização na inicialização.</span><span class="sxs-lookup"><span data-stu-id="d66f1-135">The order in which devices will be searched for a boot sector at startup.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-136">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="d66f1-136">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-139">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d66f1-139">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-140">O identificador interno para esta compilação do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="d66f1-140">The internal identifier for this compilation of software element.</span></span> <span data-ttu-id="d66f1-141">Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como 14.</span><span class="sxs-lookup"><span data-stu-id="d66f1-141">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 14.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-142">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d66f1-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-145">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d66f1-145">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-146">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="d66f1-146">A short description of the object.</span></span> <span data-ttu-id="d66f1-147">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-148">**ChassisAssetTag**</span><span class="sxs-lookup"><span data-stu-id="d66f1-148">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-151">Preenchido automaticamente pelo BIOS quando a máquina virtual é criada.</span><span class="sxs-lookup"><span data-stu-id="d66f1-151">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-152">**ChassisSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d66f1-152">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-155">Preenchido automaticamente pelo BIOS quando a máquina virtual é criada.</span><span class="sxs-lookup"><span data-stu-id="d66f1-155">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-156">**Código de**</span><span class="sxs-lookup"><span data-stu-id="d66f1-156">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-159">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d66f1-159">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-160">O conjunto de códigos usado pelo elemento software.</span><span class="sxs-lookup"><span data-stu-id="d66f1-160">The code set used by the software element.</span></span> <span data-ttu-id="d66f1-161">Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="d66f1-161">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d66f1-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d66f1-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-165">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="d66f1-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d66f1-166">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d66f1-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d66f1-167">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-168">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="d66f1-168">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-171">O idioma selecionado no momento para o BIOS.</span><span class="sxs-lookup"><span data-stu-id="d66f1-171">The currently selected language for the BIOS.</span></span> <span data-ttu-id="d66f1-172">Essa propriedade é herdada de [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como "en \| US \| ISO8859-1".</span><span class="sxs-lookup"><span data-stu-id="d66f1-172">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-173">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d66f1-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-176">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="d66f1-176">A description of the object.</span></span> <span data-ttu-id="d66f1-177">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d66f1-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-179">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d66f1-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-181">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="d66f1-181">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d66f1-182">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d66f1-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d66f1-183">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d66f1-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-187">Um nome de exibição para o elemento.</span><span class="sxs-lookup"><span data-stu-id="d66f1-187">A display name for the element.</span></span> <span data-ttu-id="d66f1-188">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d66f1-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-190">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d66f1-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-192">Especifica a integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="d66f1-192">Specifies the current health of the element.</span></span> <span data-ttu-id="d66f1-193">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="d66f1-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="d66f1-194">Quando ocorrer um erro crítico, verifique o log de eventos para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="d66f1-194">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="d66f1-195">A propriedade **enabledstate** também pode conter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d66f1-195">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="d66f1-196">Por exemplo, quando o espaço em disco está muito baixo, o **HealthState** é definido como 25, a máquina virtual pausa e **enabledstate** é definido como 32768 (em pausa).</span><span class="sxs-lookup"><span data-stu-id="d66f1-196">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="d66f1-197">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="d66f1-198">Valor</span><span class="sxs-lookup"><span data-stu-id="d66f1-198">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="d66f1-199">Significado</span><span class="sxs-lookup"><span data-stu-id="d66f1-199">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="d66f1-200"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-200"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="d66f1-201">A máquina virtual é totalmente funcional e está operando em parâmetros operacionais normais e sem erros.</span><span class="sxs-lookup"><span data-stu-id="d66f1-201">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="d66f1-202"><dt>**Maior falha**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-202"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="d66f1-203">A máquina virtual sofreu uma falha grave.</span><span class="sxs-lookup"><span data-stu-id="d66f1-203">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="d66f1-204">Esse valor é usado quando um ou mais discos que contêm VHDs da máquina virtual estão com pouco espaço em disco e a máquina virtual foi pausada.</span><span class="sxs-lookup"><span data-stu-id="d66f1-204">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="d66f1-205"><dt>**Falha crítica**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-205"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="d66f1-206">O elemento não é funcional e a recuperação pode não ser possível.</span><span class="sxs-lookup"><span data-stu-id="d66f1-206">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="d66f1-207">Isso pode indicar que o processo de trabalho para a máquina virtual (Vmwp.exe) não está respondendo às solicitações de controle ou de informações, ou que um ou mais discos que contêm VHDs para a máquina virtual estão com pouco espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="d66f1-207">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d66f1-208">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="d66f1-208">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-209">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-211">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d66f1-211">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-212">O identificador do fabricante para este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="d66f1-212">The manufacturer's identifier for this software element.</span></span> <span data-ttu-id="d66f1-213">Geralmente, essa será uma SKU (unidade de manutenção de estoque) ou um número de peça.</span><span class="sxs-lookup"><span data-stu-id="d66f1-213">Often this will be a stock keeping unit (SKU) or a part number.</span></span> <span data-ttu-id="d66f1-214">Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="d66f1-214">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d66f1-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-216">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d66f1-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-218">Preenchido automaticamente pelo BIOS quando a máquina virtual é criada.</span><span class="sxs-lookup"><span data-stu-id="d66f1-218">Automatically populated by the BIOS when the virtual machine is created.</span></span> <span data-ttu-id="d66f1-219">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-220">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d66f1-220">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-223">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="d66f1-223">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-224">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="d66f1-224">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d66f1-225">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-226">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="d66f1-226">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-229">Qualificadores: **maxlen** (32)</span><span class="sxs-lookup"><span data-stu-id="d66f1-229">Qualifiers: **MaxLen** (32)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-230">A edição de idioma deste elemento de software.</span><span class="sxs-lookup"><span data-stu-id="d66f1-230">The language edition of this software element.</span></span> <span data-ttu-id="d66f1-231">Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="d66f1-231">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-232">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="d66f1-232">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-233">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-233">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-235">Uma lista de idiomas instaláveis para o BIOS.</span><span class="sxs-lookup"><span data-stu-id="d66f1-235">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="d66f1-236">Essa propriedade é herdada de [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como "en \| US \| ISO8859-1".</span><span class="sxs-lookup"><span data-stu-id="d66f1-236">THIS property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-237">**LoadedEndingAddress**</span><span class="sxs-lookup"><span data-stu-id="d66f1-237">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-238">Tipo de dados: **unit64**</span><span class="sxs-lookup"><span data-stu-id="d66f1-238">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-240">O endereço final da memória que este BIOS ocupa.</span><span class="sxs-lookup"><span data-stu-id="d66f1-240">The ending address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="d66f1-241">Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="d66f1-241">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-242">**LoadedStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="d66f1-242">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-243">Tipo de dados: **unit64**</span><span class="sxs-lookup"><span data-stu-id="d66f1-243">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-245">O endereço inicial da memória que este BIOS ocupa.</span><span class="sxs-lookup"><span data-stu-id="d66f1-245">The starting address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="d66f1-246">Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como 0xE0000.</span><span class="sxs-lookup"><span data-stu-id="d66f1-246">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xE0000.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-247">**LoadUtilityInformation**</span><span class="sxs-lookup"><span data-stu-id="d66f1-247">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-250">Uma cadeia de caracteres que descreve o Utilitário Flash/Load do BIOS que é necessário para atualizar o elemento BIOS.</span><span class="sxs-lookup"><span data-stu-id="d66f1-250">A string that describes the BIOS flash/load utility that is required to update the BIOS element.</span></span> <span data-ttu-id="d66f1-251">A versão e outras informações podem ser indicadas nesta propriedade.</span><span class="sxs-lookup"><span data-stu-id="d66f1-251">Version and other information may be indicated in this property.</span></span> <span data-ttu-id="d66f1-252">Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d66f1-252">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-253">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="d66f1-253">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-254">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-256">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d66f1-256">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-257">O fabricante deste BIOS.</span><span class="sxs-lookup"><span data-stu-id="d66f1-257">The manufacturer of this BIOS.</span></span> <span data-ttu-id="d66f1-258">Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="d66f1-258">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-259">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d66f1-259">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-260">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-262">Qualificadores: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="d66f1-262">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-263">O nome usado para identificar este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="d66f1-263">The name used to identify this software element.</span></span> <span data-ttu-id="d66f1-264">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="d66f1-264">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="d66f1-265">Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como "BIOS".</span><span class="sxs-lookup"><span data-stu-id="d66f1-265">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "BIOS".</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d66f1-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-267">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d66f1-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-269">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="d66f1-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d66f1-270">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d66f1-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d66f1-271">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-272">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d66f1-272">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-273">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d66f1-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-275">Uma matriz que contém os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="d66f1-275">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="d66f1-276">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="d66f1-277">O valor no índice zero (0) é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d66f1-277">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="d66f1-278">Valor</span><span class="sxs-lookup"><span data-stu-id="d66f1-278">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="d66f1-279">Significado</span><span class="sxs-lookup"><span data-stu-id="d66f1-279">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="d66f1-280"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-280"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="d66f1-281">A máquina virtual está funcional e funcionando normalmente.</span><span class="sxs-lookup"><span data-stu-id="d66f1-281">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="d66f1-282"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-282"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="d66f1-283">A máquina virtual só está parcialmente funcional.</span><span class="sxs-lookup"><span data-stu-id="d66f1-283">The virtual machine is only partially functional.</span></span> <span data-ttu-id="d66f1-284">Isso indica que o armazenamento que contém a configuração não está acessível.</span><span class="sxs-lookup"><span data-stu-id="d66f1-284">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="d66f1-285">Uma máquina virtual nesse estado só pode ser desativada ou excluída.</span><span class="sxs-lookup"><span data-stu-id="d66f1-285">A virtual machine in this state may only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="d66f1-286"><dt>**Falha preditiva**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-286"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="d66f1-287">A máquina virtual é funcional, mas pode falhar no futuro.</span><span class="sxs-lookup"><span data-stu-id="d66f1-287">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="d66f1-288">Isso indica que o armazenamento que contém o disco rígido virtual da máquina virtual está com pouco espaço livre.</span><span class="sxs-lookup"><span data-stu-id="d66f1-288">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="d66f1-289">A máquina virtual será pausada se mais espaço em disco não for disponibilizado.</span><span class="sxs-lookup"><span data-stu-id="d66f1-289">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="d66f1-290"><dt>**Parado**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-290"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="d66f1-291">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="d66f1-291">This value is not supported.</span></span> <span data-ttu-id="d66f1-292">Se a máquina virtual for interrompida, a propriedade **enabledstate** terá um valor de 3 (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="d66f1-292">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="d66f1-293"><dt>**No serviço**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-293"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="d66f1-294">A máquina virtual está processando uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="d66f1-294">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="d66f1-295"><dt>15</dt> <dt>**inativos**</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-295"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="d66f1-296">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="d66f1-296">This value is not supported.</span></span> <span data-ttu-id="d66f1-297">Se a máquina virtual for suspensa ou pausada, a propriedade **enabledstate** terá um valor de 32769 (suspenso) ou 32768 (em pausa).</span><span class="sxs-lookup"><span data-stu-id="d66f1-297">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="d66f1-298">O valor no índice one (1) é opcional e contém informações de status secundárias.</span><span class="sxs-lookup"><span data-stu-id="d66f1-298">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="d66f1-299">Um cliente deve usar o status principal do índice zero (0) para determinar se uma nova solicitação pode ser emitida para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d66f1-299">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="d66f1-300">Se **OperationalStatus** \[ 0 \] for 2 (OK), a operação indicada por **OperationalStatus** \[ 1 \] poderá ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="d66f1-300">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="d66f1-301">O valor em **OperationalStatus** \[ 1 \] é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d66f1-301">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="d66f1-302">Valor</span><span class="sxs-lookup"><span data-stu-id="d66f1-302">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="d66f1-303">Significado</span><span class="sxs-lookup"><span data-stu-id="d66f1-303">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="d66f1-304"><dt>**Criando o instantâneo**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-304"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="d66f1-305">Um instantâneo está em processo de criação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d66f1-305">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="d66f1-306"><dt>**Aplicando o instantâneo**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-306"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="d66f1-307">Um instantâneo está no processo de ser aplicado à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d66f1-307">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="d66f1-308"><dt>**Excluindo o instantâneo**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-308"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="d66f1-309">Um instantâneo está no processo de ser excluído da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d66f1-309">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="d66f1-310"><dt>**Aguardando para iniciar**</dt> o <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-310"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="d66f1-311">A máquina virtual será iniciada depois que o atraso de inicialização automática tiver decorrido.</span><span class="sxs-lookup"><span data-stu-id="d66f1-311">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="d66f1-312"><dt>**Mesclando discos**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-312"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="d66f1-313">Os discos rígidos virtuais dos instantâneos excluídos anteriormente estão sendo mesclados.</span><span class="sxs-lookup"><span data-stu-id="d66f1-313">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="d66f1-314"><dt>**Exportando a máquina Virtual**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-314"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="d66f1-315">A máquina virtual está sendo exportada.</span><span class="sxs-lookup"><span data-stu-id="d66f1-315">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="d66f1-316"><dt>**Migrando a máquina Virtual**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-316"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="d66f1-317">A máquina virtual está sendo migrada ao vivo de um computador físico para outro.</span><span class="sxs-lookup"><span data-stu-id="d66f1-317">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="d66f1-318">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="d66f1-318">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-321">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d66f1-321">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-322">O fabricante e o sistema operacional de um elemento de software quando a propriedade **TargetOperatingSystem** tem um valor de 1 (outro), que exige que a propriedade **OtherTargetOS** tenha um valor não **nulo** .</span><span class="sxs-lookup"><span data-stu-id="d66f1-322">The manufacturer and operating system for a software element when the **TargetOperatingSystem** property has a value of 1 (Other), which requires the **OtherTargetOS** property to have a non-**Null** value.</span></span> <span data-ttu-id="d66f1-323">Para todos os outros valores de **TargetOperatingSystem**, a propriedade **OtherTargetOS** deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d66f1-323">For all other values of **TargetOperatingSystem**, the **OtherTargetOS** property must be **Null**.</span></span> <span data-ttu-id="d66f1-324">Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="d66f1-324">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-325">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="d66f1-325">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-326">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d66f1-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-328">Se for true, esse é o BIOS primário do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="d66f1-328">If True, this is the primary BIOS of the computer system.</span></span> <span data-ttu-id="d66f1-329">Essa propriedade é herdada de [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="d66f1-329">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-330">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d66f1-330">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-331">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d66f1-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-333">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="d66f1-333">Provides high level status information.</span></span> <span data-ttu-id="d66f1-334">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer informações de status de integridade detalhadas e de alto nível para o elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="d66f1-334">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="d66f1-335">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="d66f1-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d66f1-336">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-337">**RegistryURIs**</span><span class="sxs-lookup"><span data-stu-id="d66f1-337">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-338">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-340">Uma matriz de cadeias de caracteres que representa o local de publicação do registro de atributo do BIOS ou registros em conformidade com a implementação.</span><span class="sxs-lookup"><span data-stu-id="d66f1-340">An array of strings representing the publication location of the BIOS attribute registry or registries the implementation complies to.</span></span> <span data-ttu-id="d66f1-341">Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-341">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-342">**Liberado**</span><span class="sxs-lookup"><span data-stu-id="d66f1-342">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-343">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d66f1-343">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-345">A data em que o BIOS foi lançado.</span><span class="sxs-lookup"><span data-stu-id="d66f1-345">The date that the BIOS was released.</span></span> <span data-ttu-id="d66f1-346">Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-346">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-347">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d66f1-347">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-348">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-350">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d66f1-350">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-351">O número de série atribuído do BIOS.</span><span class="sxs-lookup"><span data-stu-id="d66f1-351">The assigned serial number of the BIOS.</span></span> <span data-ttu-id="d66f1-352">Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-352">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-353">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="d66f1-353">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-354">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-356">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="d66f1-356">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-357">Um identificador para o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="d66f1-357">An identifier for the software element.</span></span> <span data-ttu-id="d66f1-358">Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como "Microsoft:*GUID* \\ *específico de dispositivo-dados*".</span><span class="sxs-lookup"><span data-stu-id="d66f1-358">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-359">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="d66f1-359">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-360">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d66f1-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-362">O estado do ciclo de vida de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="d66f1-362">The state of a software element's life cycle.</span></span> <span data-ttu-id="d66f1-363">Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como 2 (executável).</span><span class="sxs-lookup"><span data-stu-id="d66f1-363">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 2 (Executable).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-364">**Status**</span><span class="sxs-lookup"><span data-stu-id="d66f1-364">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-365">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-367">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="d66f1-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-368">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d66f1-368">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-369">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-371">Qualificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="d66f1-371">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-372">Uma matriz que contém cadeias de caracteres que descrevem os valores correspondentes da matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d66f1-372">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="d66f1-373">Por exemplo, se 11 (em serviço) for o valor atribuído a **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] poderá conter uma explicação sobre o motivo pelo qual a máquina virtual está processando uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="d66f1-373">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="d66f1-374">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d66f1-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-375">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="d66f1-375">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-376">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d66f1-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-378">O ambiente do sistema operacional do elemento.</span><span class="sxs-lookup"><span data-stu-id="d66f1-378">The element's operating system environment.</span></span> <span data-ttu-id="d66f1-379">Essa propriedade é herdada de [**CIM \_ softwareelement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e é sempre definida como 0 (desconhecido).</span><span class="sxs-lookup"><span data-stu-id="d66f1-379">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 0 (Unknown).</span></span>

</dd> <dt>

<span data-ttu-id="d66f1-380">**Versão**</span><span class="sxs-lookup"><span data-stu-id="d66f1-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d66f1-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d66f1-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d66f1-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d66f1-383">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="d66f1-383">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d66f1-384">A versão do BIOS.</span><span class="sxs-lookup"><span data-stu-id="d66f1-384">The version of the BIOS.</span></span> <span data-ttu-id="d66f1-385">Essa propriedade é herdada do [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)e é sempre definida como "8.02.00".</span><span class="sxs-lookup"><span data-stu-id="d66f1-385">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "8.02.00".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d66f1-386">Comentários</span><span class="sxs-lookup"><span data-stu-id="d66f1-386">Remarks</span></span>

<span data-ttu-id="d66f1-387">O acesso à **classe \_ bioselement Msvm** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="d66f1-387">Access to the **Msvm\_BIOSElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d66f1-388">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d66f1-388">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d66f1-389">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d66f1-389">Requirements</span></span>



| <span data-ttu-id="d66f1-390">Requisito</span><span class="sxs-lookup"><span data-stu-id="d66f1-390">Requirement</span></span> | <span data-ttu-id="d66f1-391">Valor</span><span class="sxs-lookup"><span data-stu-id="d66f1-391">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d66f1-392">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d66f1-392">Minimum supported client</span></span><br/> | <span data-ttu-id="d66f1-393">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d66f1-393">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d66f1-394">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d66f1-394">Minimum supported server</span></span><br/> | <span data-ttu-id="d66f1-395">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d66f1-395">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d66f1-396">Namespace</span><span class="sxs-lookup"><span data-stu-id="d66f1-396">Namespace</span></span><br/>                | <span data-ttu-id="d66f1-397">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d66f1-397">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d66f1-398">MOF</span><span class="sxs-lookup"><span data-stu-id="d66f1-398">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d66f1-399"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-399"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d66f1-400">DLL</span><span class="sxs-lookup"><span data-stu-id="d66f1-400">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d66f1-401"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d66f1-401"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d66f1-402">Confira também</span><span class="sxs-lookup"><span data-stu-id="d66f1-402">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d66f1-403">**CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="d66f1-403">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="d66f1-404">Classes do BIOS</span><span class="sxs-lookup"><span data-stu-id="d66f1-404">BIOS Classes</span></span>](bios-classes.md)
</dt> <dt>

[<span data-ttu-id="d66f1-405">**CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="d66f1-405">**CIM\_BIOSElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

