---
description: O Win32 \_ PhysicalMemoryArray&\# 160; A classe WMI representa detalhes sobre a memória física do sistema de computador. Isso inclui o número de dispositivos de memória, a capacidade de memória disponível e o tipo de memória&\# 8212; por exemplo, memória do sistema ou de vídeo.
ms.assetid: 6b553230-e1fc-46e6-b13a-02fbbd34034d
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemoryArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryArray
- Win32_PhysicalMemoryArray.IsCompatible
- Win32_PhysicalMemoryArray.Caption
- Win32_PhysicalMemoryArray.CreationClassName
- Win32_PhysicalMemoryArray.Depth
- Win32_PhysicalMemoryArray.Description
- Win32_PhysicalMemoryArray.Height
- Win32_PhysicalMemoryArray.HotSwappable
- Win32_PhysicalMemoryArray.InstallDate
- Win32_PhysicalMemoryArray.Location
- Win32_PhysicalMemoryArray.Manufacturer
- Win32_PhysicalMemoryArray.MaxCapacity
- Win32_PhysicalMemoryArray.MaxCapacityEx
- Win32_PhysicalMemoryArray.MemoryDevices
- Win32_PhysicalMemoryArray.MemoryErrorCorrection
- Win32_PhysicalMemoryArray.Model
- Win32_PhysicalMemoryArray.Name
- Win32_PhysicalMemoryArray.OtherIdentifyingInfo
- Win32_PhysicalMemoryArray.PartNumber
- Win32_PhysicalMemoryArray.PoweredOn
- Win32_PhysicalMemoryArray.Removable
- Win32_PhysicalMemoryArray.Replaceable
- Win32_PhysicalMemoryArray.SerialNumber
- Win32_PhysicalMemoryArray.SKU
- Win32_PhysicalMemoryArray.Status
- Win32_PhysicalMemoryArray.Tag
- Win32_PhysicalMemoryArray.Use
- Win32_PhysicalMemoryArray.Version
- Win32_PhysicalMemoryArray.Weight
- Win32_PhysicalMemoryArray.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8a585b0399f7015113b02ff48dbeb85956c9e62b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920589"
---
# <a name="win32_physicalmemoryarray-class"></a><span data-ttu-id="73040-104">\_Classe Win32 PhysicalMemoryArray</span><span class="sxs-lookup"><span data-stu-id="73040-104">Win32\_PhysicalMemoryArray class</span></span>

<span data-ttu-id="73040-105">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PhysicalMemoryArray do Win32** representa detalhes sobre a memória física do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="73040-105">The **Win32\_PhysicalMemoryArray** [WMI class](../wmisdk/retrieving-a-class.md) represents details about the computer system physical memory.</span></span> <span data-ttu-id="73040-106">Isso inclui o número de dispositivos de memória, a capacidade de memória disponível e o tipo de memória — por exemplo, memória do sistema ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="73040-106">This includes the number of memory devices, memory capacity available, and memory type—for example, system or video memory.</span></span>

<span data-ttu-id="73040-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="73040-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="73040-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="73040-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="73040-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73040-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B99-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemoryArray : CIM_PhysicalPackage
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   Location;
  string   Manufacturer;
  uint32   MaxCapacity;
  uint64   MaxCapacityEx;
  uint16   MemoryDevices;
  uint16   MemoryErrorCorrection;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  uint16   Use;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="73040-110">Membros</span><span class="sxs-lookup"><span data-stu-id="73040-110">Members</span></span>

<span data-ttu-id="73040-111">A classe **Win32 \_ PhysicalMemoryArray** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="73040-111">The **Win32\_PhysicalMemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="73040-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="73040-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="73040-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73040-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="73040-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="73040-114">Methods</span></span>

<span data-ttu-id="73040-115">A classe **Win32 \_ PhysicalMemoryArray** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="73040-115">The **Win32\_PhysicalMemoryArray** class has these methods.</span></span>



| <span data-ttu-id="73040-116">Método</span><span class="sxs-lookup"><span data-stu-id="73040-116">Method</span></span>           | <span data-ttu-id="73040-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="73040-117">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="73040-118">**Iscompatível**</span><span class="sxs-lookup"><span data-stu-id="73040-118">**IsCompatible**</span></span> | <span data-ttu-id="73040-119">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="73040-119">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="73040-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73040-120">Properties</span></span>

<span data-ttu-id="73040-121">A classe **Win32 \_ PhysicalMemoryArray** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="73040-121">The **Win32\_PhysicalMemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73040-122">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="73040-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-125">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="73040-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="73040-126">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="73040-126">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="73040-127">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-128">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="73040-128">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-131">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="73040-131">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="73040-132">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="73040-132">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="73040-133">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="73040-133">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="73040-134">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-134">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-135">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="73040-135">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-136">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="73040-136">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="73040-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-138">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="73040-138">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="73040-139">Profundidade do pacote físico — em polegadas.</span><span class="sxs-lookup"><span data-stu-id="73040-139">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="73040-140">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="73040-140">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-141">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="73040-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-144">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="73040-144">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="73040-145">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="73040-145">Description of the object.</span></span>

<span data-ttu-id="73040-146">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-147">**Altura**</span><span class="sxs-lookup"><span data-stu-id="73040-147">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-148">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="73040-148">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="73040-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-150">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="73040-150">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="73040-151">Altura do pacote físico — em polegadas.</span><span class="sxs-lookup"><span data-stu-id="73040-151">Height of the physical package—in inches.</span></span>

<span data-ttu-id="73040-152">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="73040-152">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-153">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="73040-153">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-154">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="73040-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73040-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73040-156">Se for **true**, um pacote físico poderá ser trocado de maneira intercambiável (se for possível substituir o elemento por um fisicamente diferente, mas equivalente um, enquanto o pacote recipiente tem energia aplicada a ele, é "ativado").</span><span class="sxs-lookup"><span data-stu-id="73040-156">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it, is "on").</span></span> <span data-ttu-id="73040-157">Por exemplo, um pacote de unidade de disco inserido usando conectores de SCA é removível e pode ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="73040-157">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="73040-158">Todos os pacotes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="73040-158">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="73040-159">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="73040-159">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-160">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="73040-160">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-161">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="73040-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="73040-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-163">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="73040-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="73040-164">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="73040-164">Date and time the object was installed.</span></span> <span data-ttu-id="73040-165">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="73040-165">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="73040-166">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-167">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="73040-167">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-168">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73040-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73040-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-170">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS de \| \| localização 16")</span><span class="sxs-lookup"><span data-stu-id="73040-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="73040-171">Local físico da matriz de memória.</span><span class="sxs-lookup"><span data-stu-id="73040-171">Physical location of the memory array.</span></span>

<span data-ttu-id="73040-172">Esse valor é proveniente do membro **local** da estrutura da **matriz de memória física** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="73040-172">This value comes from the **Location** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="73040-173">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="73040-173">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="73040-174">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="73040-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="73040-175">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="73040-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_board_or_motherboard"></span><span id="system_board_or_motherboard"></span><span id="SYSTEM_BOARD_OR_MOTHERBOARD"></span>

<span data-ttu-id="73040-176">**Placa do sistema ou placa-mãe** (3)</span><span class="sxs-lookup"><span data-stu-id="73040-176">**System board or motherboard** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_add-on_card"></span><span id="isa_add-on_card"></span><span id="ISA_ADD-ON_CARD"></span>

<span data-ttu-id="73040-177">**Placa do complemento ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="73040-177">**ISA add-on card** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_add-on_card"></span><span id="eisa_add-on_card"></span><span id="EISA_ADD-ON_CARD"></span>

<span data-ttu-id="73040-178">**Placa complementar EISA** (5)</span><span class="sxs-lookup"><span data-stu-id="73040-178">**EISA add-on card** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_add-on_card"></span><span id="pci_add-on_card"></span><span id="PCI_ADD-ON_CARD"></span>

<span data-ttu-id="73040-179">**Placa complementar PCI** (6)</span><span class="sxs-lookup"><span data-stu-id="73040-179">**PCI add-on card** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_add-on_card"></span><span id="mca_add-on_card"></span><span id="MCA_ADD-ON_CARD"></span>

<span data-ttu-id="73040-180">**Placa de complemento MCA** (7)</span><span class="sxs-lookup"><span data-stu-id="73040-180">**MCA add-on card** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_add-on_card"></span><span id="pcmcia_add-on_card"></span><span id="PCMCIA_ADD-ON_CARD"></span>

<span data-ttu-id="73040-181">**Placa complementar PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="73040-181">**PCMCIA add-on card** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_add-on_card"></span><span id="proprietary_add-on_card"></span><span id="PROPRIETARY_ADD-ON_CARD"></span>

<span data-ttu-id="73040-182">**Placa complementar proprietária** (9)</span><span class="sxs-lookup"><span data-stu-id="73040-182">**Proprietary add-on card** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="73040-183">**NuBus** (10)</span><span class="sxs-lookup"><span data-stu-id="73040-183">**NuBus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C20_add-on_card"></span><span id="pc-98_c20_add-on_card"></span><span id="PC-98_C20_ADD-ON_CARD"></span>

<span data-ttu-id="73040-184">**Cartão de complemento do PC-98/C20** (11)</span><span class="sxs-lookup"><span data-stu-id="73040-184">**PC-98/C20 add-on card** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C24_add-on_card"></span><span id="pc-98_c24_add-on_card"></span><span id="PC-98_C24_ADD-ON_CARD"></span>

<span data-ttu-id="73040-185">**Cartão de complemento do PC-98/C24** (12)</span><span class="sxs-lookup"><span data-stu-id="73040-185">**PC-98/C24 add-on card** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_E_add-on_card"></span><span id="pc-98_e_add-on_card"></span><span id="PC-98_E_ADD-ON_CARD"></span>

<span data-ttu-id="73040-186">**Cartão de complemento do PC-98/E** (13)</span><span class="sxs-lookup"><span data-stu-id="73040-186">**PC-98/E add-on card** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_Local_bus_add-on_card"></span><span id="pc-98_local_bus_add-on_card"></span><span id="PC-98_LOCAL_BUS_ADD-ON_CARD"></span>

<span data-ttu-id="73040-187">**Placa complementar do barramento local do PC-98/** (14)</span><span class="sxs-lookup"><span data-stu-id="73040-187">**PC-98/Local bus add-on card** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="73040-188">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="73040-188">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-191">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="73040-191">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="73040-192">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="73040-192">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="73040-193">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-193">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-194">**MaxCapacity**</span><span class="sxs-lookup"><span data-stu-id="73040-194">**MaxCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-195">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73040-195">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73040-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-197">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo de SMBIOS 16 \| capacidade máxima")</span><span class="sxs-lookup"><span data-stu-id="73040-197">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Maximum Capacity")</span></span>
</dt> </dl>

<span data-ttu-id="73040-198">Em vez disso, use a propriedade **MaxCapacityEx** .</span><span class="sxs-lookup"><span data-stu-id="73040-198">Use the **MaxCapacityEx** property instead.</span></span>

<span data-ttu-id="73040-199">Esse valor é proveniente do membro de **capacidade máxima** da estrutura da **matriz de memória física** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="73040-199">This value comes from the **Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="73040-200">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Tamanho máximo da memória (em bytes) instalável para essa matriz de memória específica.</span><span class="sxs-lookup"><span data-stu-id="73040-200">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** Maximum memory size (in bytes) installable for this particular memory array.</span></span> <span data-ttu-id="73040-201">Se o tamanho for desconhecido, a propriedade receberá um valor de 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="73040-201">If the size is unknown, the property is given a value of 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="73040-202">**MaxCapacityEx**</span><span class="sxs-lookup"><span data-stu-id="73040-202">**MaxCapacityEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-203">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73040-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73040-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-205">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo SMBIOS 16 \| capacidade máxima estendida"), [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="73040-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Extended Maximum Capacity"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="73040-206">Tamanho máximo da memória (em quilobytes) instalável para essa matriz de memória específica.</span><span class="sxs-lookup"><span data-stu-id="73040-206">Maximum memory size (in kilobytes) installable for this particular memory array.</span></span> <span data-ttu-id="73040-207">Se o tamanho for desconhecido, a propriedade receberá um valor de 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="73040-207">If the size is unknown, the property is given a value of 0 (zero).</span></span>

<span data-ttu-id="73040-208">Esse valor é proveniente do membro de **capacidade máxima estendida** da estrutura da **matriz de memória física** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="73040-208">This value comes from the **Extended Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="73040-209">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="73040-209">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="73040-210">**MemoryDevices**</span><span class="sxs-lookup"><span data-stu-id="73040-210">**MemoryDevices**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-211">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73040-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73040-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-213">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo de SMBIOS 16 \| número de dispositivos de memória")</span><span class="sxs-lookup"><span data-stu-id="73040-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Number of Memory Devices")</span></span>
</dt> </dl>

<span data-ttu-id="73040-214">Número de Slots físicos ou soquetes disponíveis nesta matriz de memória.</span><span class="sxs-lookup"><span data-stu-id="73040-214">Number of physical slots or sockets available in this memory array.</span></span>

<span data-ttu-id="73040-215">Esse valor é proveniente do membro de **número de dispositivos de memória** da estrutura da **matriz de memória física** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="73040-215">This value comes from the **Number of Memory Devices** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="73040-216">**MemoryErrorCorrection**</span><span class="sxs-lookup"><span data-stu-id="73040-216">**MemoryErrorCorrection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-217">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73040-217">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73040-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-219">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| correção de erro de memória do tipo SMBIOS \| ")</span><span class="sxs-lookup"><span data-stu-id="73040-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="73040-220">Tipo de correção de erro usada pela matriz de memória.</span><span class="sxs-lookup"><span data-stu-id="73040-220">Type of error correction used by the memory array.</span></span>

<span data-ttu-id="73040-221">Esse valor é proveniente do membro de **correção de erro de memória** da estrutura da matriz de **memória física** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="73040-221">This value comes from the **Memory Error Correction** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="73040-222">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="73040-222">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="73040-223">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="73040-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="73040-224">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="73040-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="73040-225">**Nenhum** (3)</span><span class="sxs-lookup"><span data-stu-id="73040-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="73040-226">**Paridade** (4)</span><span class="sxs-lookup"><span data-stu-id="73040-226">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="73040-227">**ECC de bit único** (5)</span><span class="sxs-lookup"><span data-stu-id="73040-227">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="73040-228">**ECC de vários bits** (6)</span><span class="sxs-lookup"><span data-stu-id="73040-228">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="73040-229">**CRC** (7)</span><span class="sxs-lookup"><span data-stu-id="73040-229">**CRC** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="73040-230">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="73040-230">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-233">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="73040-233">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="73040-234">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="73040-234">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="73040-235">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-236">**Nome**</span><span class="sxs-lookup"><span data-stu-id="73040-236">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-239">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="73040-239">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="73040-240">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="73040-240">Label by which the object is known.</span></span> <span data-ttu-id="73040-241">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="73040-241">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="73040-242">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-243">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="73040-243">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-244">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73040-246">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="73040-246">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="73040-247">Um exemplo são os dados de código de barras associados a um elemento que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="73040-247">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="73040-248">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo ou puderem ser usados como uma chave de elemento, essa propriedade será **NULL** e os dados de código de barras usados como a chave de classe, na propriedade Tag.</span><span class="sxs-lookup"><span data-stu-id="73040-248">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="73040-249">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-249">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-250">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="73040-250">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-253">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="73040-253">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="73040-254">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="73040-254">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="73040-255">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-255">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-256">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="73040-256">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-257">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="73040-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73040-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73040-259">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="73040-259">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="73040-260">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-260">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-261">**Removível**</span><span class="sxs-lookup"><span data-stu-id="73040-261">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-262">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="73040-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73040-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73040-264">Se for **true**, um pacote físico será removível (se for projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem encontrar a função do empacotamento geral).</span><span class="sxs-lookup"><span data-stu-id="73040-264">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="73040-265">Um pacote ainda poderá ser removível se a energia precisar ser "desativada" para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="73040-265">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="73040-266">Se a energia puder ser "ativada" e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="73040-266">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="73040-267">Por exemplo, uma bateria extra em um laptop é removível, assim como um pacote de unidade de disco inserido usando conectores SCA.</span><span class="sxs-lookup"><span data-stu-id="73040-267">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="73040-268">No entanto, o último pode ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="73040-268">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="73040-269">A tela de um laptop não é removível, nem uma fonte de alimentação não redundante.</span><span class="sxs-lookup"><span data-stu-id="73040-269">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="73040-270">A remoção desses componentes afetaria a função do empacotamento geral ou é impossível devido à forte integração do pacote.</span><span class="sxs-lookup"><span data-stu-id="73040-270">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="73040-271">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="73040-271">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-272">**Peças**</span><span class="sxs-lookup"><span data-stu-id="73040-272">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-273">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="73040-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73040-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73040-275">Se **for true**, esse componente de mídia física poderá ser substituído por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="73040-275">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="73040-276">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="73040-276">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="73040-277">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="73040-277">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="73040-278">Outro exemplo é um pacote de fornecimento de energia montado em trilhos deslizantes.</span><span class="sxs-lookup"><span data-stu-id="73040-278">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="73040-279">Todos os pacotes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="73040-279">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="73040-280">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="73040-280">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-281">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="73040-281">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-284">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="73040-284">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="73040-285">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="73040-285">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="73040-286">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-287">**SKU**</span><span class="sxs-lookup"><span data-stu-id="73040-287">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-290">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="73040-290">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="73040-291">Número de unidade manutenção para o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="73040-291">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="73040-292">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-293">**Status**</span><span class="sxs-lookup"><span data-stu-id="73040-293">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-294">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-296">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="73040-296">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="73040-297">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="73040-297">Current status of the object.</span></span> <span data-ttu-id="73040-298">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="73040-298">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="73040-299">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="73040-299">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="73040-300">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="73040-300">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="73040-301">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="73040-301">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="73040-302">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="73040-302">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="73040-303">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="73040-304">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="73040-304">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="73040-305">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="73040-305">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="73040-306">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="73040-306">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="73040-307">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="73040-307">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="73040-308">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="73040-308">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="73040-309">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="73040-309">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="73040-310">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="73040-310">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="73040-311">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="73040-311">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="73040-312">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="73040-312">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="73040-313">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="73040-313">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="73040-314">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="73040-314">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="73040-315">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="73040-315">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="73040-316">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="73040-316">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="73040-317">**Tag**</span><span class="sxs-lookup"><span data-stu-id="73040-317">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-318">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-320">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="73040-320">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="73040-321">Identificador exclusivo da matriz de memória física.</span><span class="sxs-lookup"><span data-stu-id="73040-321">Unique identifier of the physical memory array.</span></span>

<span data-ttu-id="73040-322">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-322">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="73040-323">Exemplo: "matriz de memória física 1"</span><span class="sxs-lookup"><span data-stu-id="73040-323">Example: "Physical Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="73040-324">**Uso**</span><span class="sxs-lookup"><span data-stu-id="73040-324">**Use**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-325">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73040-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73040-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-327">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 16 \| uso")</span><span class="sxs-lookup"><span data-stu-id="73040-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Use")</span></span>
</dt> </dl>

<span data-ttu-id="73040-328">Como a memória é usada no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="73040-328">How memory is used in the computer system.</span></span>

<span data-ttu-id="73040-329">Esse valor é proveniente do membro de **uso** da estrutura de **matriz de memória física** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="73040-329">This value comes from the **Use** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="73040-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="73040-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="73040-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="73040-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="73040-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="73040-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>

<span data-ttu-id="73040-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**Memória do sistema** (3)</span><span class="sxs-lookup"><span data-stu-id="73040-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**System memory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>

<span data-ttu-id="73040-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Memória de vídeo** (4)</span><span class="sxs-lookup"><span data-stu-id="73040-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Video memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>

<span data-ttu-id="73040-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Memória flash** (5)</span><span class="sxs-lookup"><span data-stu-id="73040-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Flash memory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>

<span data-ttu-id="73040-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**RAM não volátil** (6)</span><span class="sxs-lookup"><span data-stu-id="73040-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**Non-volatile RAM** (6)</span></span>


</dt> <dd>

<span data-ttu-id="73040-337">RAM não volátil</span><span class="sxs-lookup"><span data-stu-id="73040-337">Nonvolatile RAM</span></span>

</dd> <dt>

<span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>

<span data-ttu-id="73040-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Memória de cache** (7)</span><span class="sxs-lookup"><span data-stu-id="73040-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Cache memory** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="73040-339">**Versão**</span><span class="sxs-lookup"><span data-stu-id="73040-339">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73040-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73040-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-342">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="73040-342">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="73040-343">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="73040-343">Version of the physical element.</span></span>

<span data-ttu-id="73040-344">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="73040-344">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-345">**Weight**</span><span class="sxs-lookup"><span data-stu-id="73040-345">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-346">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="73040-346">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="73040-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-348">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("libras")</span><span class="sxs-lookup"><span data-stu-id="73040-348">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="73040-349">Peso do pacote físico em libras.</span><span class="sxs-lookup"><span data-stu-id="73040-349">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="73040-350">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="73040-350">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="73040-351">**Largura**</span><span class="sxs-lookup"><span data-stu-id="73040-351">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73040-352">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="73040-352">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="73040-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73040-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73040-354">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="73040-354">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="73040-355">Largura do pacote físico em polegadas.</span><span class="sxs-lookup"><span data-stu-id="73040-355">Width of the physical package in inches.</span></span>

<span data-ttu-id="73040-356">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="73040-356">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73040-357">Comentários</span><span class="sxs-lookup"><span data-stu-id="73040-357">Remarks</span></span>

<span data-ttu-id="73040-358">A classe **Win32 \_ PhysicalMemoryArray** é derivada de [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="73040-358">The **Win32\_PhysicalMemoryArray** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

## <a name="examples"></a><span data-ttu-id="73040-359">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73040-359">Examples</span></span>

<span data-ttu-id="73040-360">O exemplo do PowerShell a seguir recupera o número de Slots de memória e a quantidade de memória instalada em um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="73040-360">The following PowerShell sample retrieves the number of memory slots and the amount of memory installed on a target computer.</span></span>


```PowerShell
$strComputer = Read-Host "Enter Computer Name"
 $colSlots = Get-WmiObject -Class "win32_PhysicalMemoryArray" -namespace "root\CIMV2" `
 -computerName $strComputer
 $colRAM = Get-WmiObject -Class "win32_PhysicalMemory" -namespace "root\CIMV2" `
 -computerName $strComputer

Foreach ($objSlot In $colSlots){
      "Total Number of DIMM Slots: " + $objSlot.MemoryDevices
 }
 Foreach ($objRAM In $colRAM) {
      "Memory Installed: " + $objRAM.DeviceLocator
      "Memory Size: " + ($objRAM.Capacity / 1GB) + " GB"
 }
```



<span data-ttu-id="73040-361">O exemplo de código VBScript a seguir retorna informações sobre a memória física instalada em um computador.</span><span class="sxs-lookup"><span data-stu-id="73040-361">The following VBScript code sample returns information about the physical memory installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_PhysicalMemoryArray") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Maximum Capacity: " & objItem.MaxCapacity 
    Wscript.Echo "Memory Devices: " & objItem.MemoryDevices 
    Wscript.Echo "Memory Error Correction: " & objItem.MemoryErrorCorrection 
Next 
```



## <a name="requirements"></a><span data-ttu-id="73040-362">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73040-362">Requirements</span></span>



| <span data-ttu-id="73040-363">Requisito</span><span class="sxs-lookup"><span data-stu-id="73040-363">Requirement</span></span> | <span data-ttu-id="73040-364">Valor</span><span class="sxs-lookup"><span data-stu-id="73040-364">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73040-365">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73040-365">Minimum supported client</span></span><br/> | <span data-ttu-id="73040-366">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73040-366">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73040-367">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73040-367">Minimum supported server</span></span><br/> | <span data-ttu-id="73040-368">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73040-368">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73040-369">Namespace</span><span class="sxs-lookup"><span data-stu-id="73040-369">Namespace</span></span><br/>                | <span data-ttu-id="73040-370">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="73040-370">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="73040-371">MOF</span><span class="sxs-lookup"><span data-stu-id="73040-371">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73040-372"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73040-372"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="73040-373">DLL</span><span class="sxs-lookup"><span data-stu-id="73040-373">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73040-374"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73040-374"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73040-375">Confira também</span><span class="sxs-lookup"><span data-stu-id="73040-375">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73040-376">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="73040-376">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="73040-377">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="73040-377">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="73040-378">**\_MemoryArrayLocation Win32**</span><span class="sxs-lookup"><span data-stu-id="73040-378">**Win32\_MemoryArrayLocation**</span></span>](win32-memoryarraylocation.md)
</dt> </dl>

 

 
