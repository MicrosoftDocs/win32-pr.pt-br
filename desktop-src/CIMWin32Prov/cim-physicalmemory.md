---
description: A \_ classe CIM PhysicalMemory representa dispositivos de memória de nível baixo, como Simms, DIMMs, chips de memória bruta e assim por diante.
ms.assetid: a25c5f00-cd85-42e6-9b26-8e9380b3c73b
ms.tgt_platform: multiple
title: Classe CIM_PhysicalMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMemory
- CIM_PhysicalMemory.BankLabel
- CIM_PhysicalMemory.Capacity
- CIM_PhysicalMemory.Caption
- CIM_PhysicalMemory.CreationClassName
- CIM_PhysicalMemory.DataWidth
- CIM_PhysicalMemory.Description
- CIM_PhysicalMemory.FormFactor
- CIM_PhysicalMemory.HotSwappable
- CIM_PhysicalMemory.InstallDate
- CIM_PhysicalMemory.InterleavePosition
- CIM_PhysicalMemory.Manufacturer
- CIM_PhysicalMemory.MemoryType
- CIM_PhysicalMemory.Model
- CIM_PhysicalMemory.Name
- CIM_PhysicalMemory.OtherIdentifyingInfo
- CIM_PhysicalMemory.PartNumber
- CIM_PhysicalMemory.PositionInRow
- CIM_PhysicalMemory.PoweredOn
- CIM_PhysicalMemory.Removable
- CIM_PhysicalMemory.Replaceable
- CIM_PhysicalMemory.SerialNumber
- CIM_PhysicalMemory.SKU
- CIM_PhysicalMemory.Speed
- CIM_PhysicalMemory.Status
- CIM_PhysicalMemory.Tag
- CIM_PhysicalMemory.TotalWidth
- CIM_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bd46ebde99ae6c6d9e28975d67563424619db84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826597"
---
# <a name="cim_physicalmemory-class"></a><span data-ttu-id="5b60a-103">\_Classe CIM PhysicalMemory</span><span class="sxs-lookup"><span data-stu-id="5b60a-103">CIM\_PhysicalMemory class</span></span>

<span data-ttu-id="5b60a-104">A classe **CIM \_ PhysicalMemory** representa dispositivos de memória de nível baixo, como Simms, DIMMs, chips de memória bruta e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5b60a-104">The **CIM\_PhysicalMemory** class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b60a-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="5b60a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5b60a-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5b60a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5b60a-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5b60a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5b60a-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5b60a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b60a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b60a-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMemory : CIM_Chip
{
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint16   MemoryType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="5b60a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="5b60a-110">Members</span></span>

<span data-ttu-id="5b60a-111">A classe **CIM \_ PhysicalMemory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5b60a-111">The **CIM\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="5b60a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b60a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b60a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5b60a-113">Properties</span></span>

<span data-ttu-id="5b60a-114">A classe **CIM \_ PhysicalMemory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5b60a-114">The **CIM\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b60a-115">**BankLabel**</span><span class="sxs-lookup"><span data-stu-id="5b60a-115">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,4 ")</span><span class="sxs-lookup"><span data-stu-id="5b60a-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-119">Rotulado banco no qual a memória está localizada.</span><span class="sxs-lookup"><span data-stu-id="5b60a-119">Labeled bank in which the memory is located.</span></span> <span data-ttu-id="5b60a-120">Por exemplo, "Bank 0" ou "Bank A".</span><span class="sxs-lookup"><span data-stu-id="5b60a-120">For example, "Bank 0" or "Bank A".</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-121">**Capacidade**</span><span class="sxs-lookup"><span data-stu-id="5b60a-121">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-122">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5b60a-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-124">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="5b60a-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-125">Capacidade total da memória física, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5b60a-125">Total capacity of the physical memory, in bytes.</span></span>

<span data-ttu-id="5b60a-126">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5b60a-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-127">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5b60a-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-130">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5b60a-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-131">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b60a-131">Short textual description of the object.</span></span>

<span data-ttu-id="5b60a-132">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5b60a-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-136">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5b60a-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-137">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5b60a-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5b60a-138">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5b60a-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5b60a-139">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-139">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-140">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="5b60a-140">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-141">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b60a-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-143">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="5b60a-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-144">Largura de dados da memória física, em bits.</span><span class="sxs-lookup"><span data-stu-id="5b60a-144">Data width of the physical memory, in bits.</span></span> <span data-ttu-id="5b60a-145">Uma largura de dados de 0 (zero) e uma largura total de 8, indica que a memória é usada unicamente para fornecer bits de correção de erro.</span><span class="sxs-lookup"><span data-stu-id="5b60a-145">A data width of 0 (zero) , and a total width of 8, indicates that the memory is solely used to provide error correction bits.</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-146">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5b60a-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-149">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="5b60a-149">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-150">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b60a-150">Textual description of the object.</span></span>

<span data-ttu-id="5b60a-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-152">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="5b60a-152">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-153">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b60a-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-155">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,6 ")</span><span class="sxs-lookup"><span data-stu-id="5b60a-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-156">Fator forma de implementação para o chip.</span><span class="sxs-lookup"><span data-stu-id="5b60a-156">Implementation form factor for the chip.</span></span> <span data-ttu-id="5b60a-157">Por exemplo, valores como SIMM, TSOP ou PGA podem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="5b60a-157">For example, values such as SIMM, TSOP, or PGA can be specified.</span></span>

<span data-ttu-id="5b60a-158">Essa propriedade é herdada [**do \_ chip CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-158">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>

<span data-ttu-id="5b60a-159">0</span><span class="sxs-lookup"><span data-stu-id="5b60a-159">0</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-160">Unknown</span><span class="sxs-lookup"><span data-stu-id="5b60a-160">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-161">1</span><span class="sxs-lookup"><span data-stu-id="5b60a-161">1</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-162">Outro</span><span class="sxs-lookup"><span data-stu-id="5b60a-162">Other</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-163">2</span><span class="sxs-lookup"><span data-stu-id="5b60a-163">2</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-164">SIP</span><span class="sxs-lookup"><span data-stu-id="5b60a-164">SIP</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-165">3</span><span class="sxs-lookup"><span data-stu-id="5b60a-165">3</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-166">DIP</span><span class="sxs-lookup"><span data-stu-id="5b60a-166">DIP</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-167">4</span><span class="sxs-lookup"><span data-stu-id="5b60a-167">4</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-168">ZIP</span><span class="sxs-lookup"><span data-stu-id="5b60a-168">ZIP</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-169">5</span><span class="sxs-lookup"><span data-stu-id="5b60a-169">5</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-170">SOJ</span><span class="sxs-lookup"><span data-stu-id="5b60a-170">SOJ</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-171">6</span><span class="sxs-lookup"><span data-stu-id="5b60a-171">6</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-172">Proprietário</span><span class="sxs-lookup"><span data-stu-id="5b60a-172">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-173">7</span><span class="sxs-lookup"><span data-stu-id="5b60a-173">7</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-174">SIMM</span><span class="sxs-lookup"><span data-stu-id="5b60a-174">SIMM</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-175">8</span><span class="sxs-lookup"><span data-stu-id="5b60a-175">8</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-176">ACTIVA</span><span class="sxs-lookup"><span data-stu-id="5b60a-176">DIMM</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-177">9</span><span class="sxs-lookup"><span data-stu-id="5b60a-177">9</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-178">TSOP</span><span class="sxs-lookup"><span data-stu-id="5b60a-178">TSOP</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-179">10</span><span class="sxs-lookup"><span data-stu-id="5b60a-179">10</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-180">PGA</span><span class="sxs-lookup"><span data-stu-id="5b60a-180">PGA</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-181">11</span><span class="sxs-lookup"><span data-stu-id="5b60a-181">11</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-182">DIMM</span><span class="sxs-lookup"><span data-stu-id="5b60a-182">RIMM</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-183">12</span><span class="sxs-lookup"><span data-stu-id="5b60a-183">12</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-184">SODIMM</span><span class="sxs-lookup"><span data-stu-id="5b60a-184">SODIMM</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-185">13</span><span class="sxs-lookup"><span data-stu-id="5b60a-185">13</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-186">SRIMM</span><span class="sxs-lookup"><span data-stu-id="5b60a-186">SRIMM</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-187">14</span><span class="sxs-lookup"><span data-stu-id="5b60a-187">14</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-188">SMD</span><span class="sxs-lookup"><span data-stu-id="5b60a-188">SMD</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-189">15</span><span class="sxs-lookup"><span data-stu-id="5b60a-189">15</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-190">SSMP</span><span class="sxs-lookup"><span data-stu-id="5b60a-190">SSMP</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-191">16</span><span class="sxs-lookup"><span data-stu-id="5b60a-191">16</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-192">QFP</span><span class="sxs-lookup"><span data-stu-id="5b60a-192">QFP</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-193">17</span><span class="sxs-lookup"><span data-stu-id="5b60a-193">17</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-194">TQFP</span><span class="sxs-lookup"><span data-stu-id="5b60a-194">TQFP</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-195">18</span><span class="sxs-lookup"><span data-stu-id="5b60a-195">18</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-196">SOIC</span><span class="sxs-lookup"><span data-stu-id="5b60a-196">SOIC</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-197">19</span><span class="sxs-lookup"><span data-stu-id="5b60a-197">19</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-198">LCCS</span><span class="sxs-lookup"><span data-stu-id="5b60a-198">LCC</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-199">20</span><span class="sxs-lookup"><span data-stu-id="5b60a-199">20</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-200">PLCC</span><span class="sxs-lookup"><span data-stu-id="5b60a-200">PLCC</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-201">21</span><span class="sxs-lookup"><span data-stu-id="5b60a-201">21</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-202">BGA</span><span class="sxs-lookup"><span data-stu-id="5b60a-202">BGA</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-203">22</span><span class="sxs-lookup"><span data-stu-id="5b60a-203">22</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-204">FPBGA</span><span class="sxs-lookup"><span data-stu-id="5b60a-204">FPBGA</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-205">23</span><span class="sxs-lookup"><span data-stu-id="5b60a-205">23</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-206">LGA</span><span class="sxs-lookup"><span data-stu-id="5b60a-206">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5b60a-207">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="5b60a-207">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-208">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5b60a-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-210">Se **for true**, o pacote poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="5b60a-210">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="5b60a-211">Um pacote físico pode ser intercambiável se o elemento puder ser substituído por um fisicamente diferente (mas equivalente) um enquanto o pacote que o contém está ativado.</span><span class="sxs-lookup"><span data-stu-id="5b60a-211">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="5b60a-212">Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="5b60a-212">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="5b60a-213">Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="5b60a-213">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="5b60a-214">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-214">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5b60a-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-216">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5b60a-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-218">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5b60a-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-219">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5b60a-219">Date and time the object was installed.</span></span> <span data-ttu-id="5b60a-220">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5b60a-220">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5b60a-221">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-222">**InterleavePosition**</span><span class="sxs-lookup"><span data-stu-id="5b60a-222">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-223">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b60a-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-225">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Endereços mapeados do dispositivo de memória DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="5b60a-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-226">Posição da memória física em uma intercalação.</span><span class="sxs-lookup"><span data-stu-id="5b60a-226">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="5b60a-227">Um valor de 0 indica não intercalado, 1 indica a primeira posição, 2 indica a segunda posição e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5b60a-227">A value of 0 indicates non-interleaved, 1 indicates the first position, 2 indicates the second position, and so on.</span></span> <span data-ttu-id="5b60a-228">Por exemplo, em uma intercalação 2:1, um valor de 1 indica que a memória está na posição par.</span><span class="sxs-lookup"><span data-stu-id="5b60a-228">For example, in a 2:1 interleave, a value of 1 indicates that the memory is in the even position.</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-229">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="5b60a-229">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-232">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5b60a-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-233">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5b60a-233">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="5b60a-234">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-234">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="5b60a-235">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-236">**Memorytype**</span><span class="sxs-lookup"><span data-stu-id="5b60a-236">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-237">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b60a-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-239">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,9 ")</span><span class="sxs-lookup"><span data-stu-id="5b60a-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-240">Tipo de memória física.</span><span class="sxs-lookup"><span data-stu-id="5b60a-240">Type of physical memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5b60a-241">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5b60a-241">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5b60a-242">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5b60a-242">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="5b60a-243">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="5b60a-243">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="5b60a-244">**DRAM síncrona** (3)</span><span class="sxs-lookup"><span data-stu-id="5b60a-244">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="5b60a-245">**DRAM de cache** (4)</span><span class="sxs-lookup"><span data-stu-id="5b60a-245">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="5b60a-246">**Edo** (5)</span><span class="sxs-lookup"><span data-stu-id="5b60a-246">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="5b60a-247">**EDRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="5b60a-247">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="5b60a-248">**VRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="5b60a-248">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="5b60a-249">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="5b60a-249">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="5b60a-250">**RAM** (9)</span><span class="sxs-lookup"><span data-stu-id="5b60a-250">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="5b60a-251">**ROM** (10)</span><span class="sxs-lookup"><span data-stu-id="5b60a-251">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="5b60a-252">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="5b60a-252">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="5b60a-253">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="5b60a-253">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="5b60a-254">**FEPROM** (13)</span><span class="sxs-lookup"><span data-stu-id="5b60a-254">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="5b60a-255">**(14** )</span><span class="sxs-lookup"><span data-stu-id="5b60a-255">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="5b60a-256">**CDRAM** (15)</span><span class="sxs-lookup"><span data-stu-id="5b60a-256">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="5b60a-257">**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="5b60a-257">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="5b60a-258">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="5b60a-258">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="5b60a-259">**SGRAM** (18)</span><span class="sxs-lookup"><span data-stu-id="5b60a-259">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="5b60a-260">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="5b60a-260">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="5b60a-261">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="5b60a-261">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="5b60a-262">**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="5b60a-262">**DDR2** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="5b60a-263">**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="5b60a-263">**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b60a-264">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="5b60a-264">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-265">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-267">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5b60a-267">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-268">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="5b60a-268">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="5b60a-269">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-269">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-270">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5b60a-270">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-271">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-273">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5b60a-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-274">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5b60a-274">Label by which the object is known.</span></span> <span data-ttu-id="5b60a-275">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="5b60a-275">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5b60a-276">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-277">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5b60a-277">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-280">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5b60a-280">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="5b60a-281">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="5b60a-281">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="5b60a-282">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="5b60a-282">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="5b60a-283">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-283">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-284">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="5b60a-284">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-285">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-287">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5b60a-287">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-288">Número de peça atribuído pela organização que produziu ou fabricou o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5b60a-288">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="5b60a-289">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-289">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-290">**PositionInRow**</span><span class="sxs-lookup"><span data-stu-id="5b60a-290">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-291">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b60a-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-293">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Endereços mapeados do dispositivo de memória DMTF \| 1,6 ")</span><span class="sxs-lookup"><span data-stu-id="5b60a-293">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-294">Posição da memória física em uma linha.</span><span class="sxs-lookup"><span data-stu-id="5b60a-294">Position of the physical memory in a row.</span></span> <span data-ttu-id="5b60a-295">Por exemplo, se usar dispositivos de memória de 2 8 bits para formar uma linha de 16 bits, um valor de 2 indica que a memória é o segundo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b60a-295">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 indicates that the memory is the second device.</span></span> <span data-ttu-id="5b60a-296">Um valor de 0 é um valor inválido para esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="5b60a-296">A value of 0 is an invalid value for this property.</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-297">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="5b60a-297">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-298">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5b60a-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-300">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="5b60a-300">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="5b60a-301">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-301">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-302">**Removível**</span><span class="sxs-lookup"><span data-stu-id="5b60a-302">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-303">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5b60a-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-305">Se for **true**, esse elemento será projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem comprometer a função do empacotamento geral.</span><span class="sxs-lookup"><span data-stu-id="5b60a-305">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="5b60a-306">Um pacote é considerado removível, mesmo que a energia precise ser desligada para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="5b60a-306">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="5b60a-307">Se a energia puder ser ativada e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="5b60a-307">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="5b60a-308">Por exemplo, um chip de processador não atualizável é removível.</span><span class="sxs-lookup"><span data-stu-id="5b60a-308">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="5b60a-309">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-309">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-310">**Peças**</span><span class="sxs-lookup"><span data-stu-id="5b60a-310">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-311">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5b60a-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-313">Se for **true**, é possível substituir o elemento por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="5b60a-313">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="5b60a-314">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="5b60a-314">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="5b60a-315">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="5b60a-315">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="5b60a-316">Todos os componentes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="5b60a-316">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="5b60a-317">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-317">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-318">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="5b60a-318">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-321">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5b60a-321">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-322">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5b60a-322">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="5b60a-323">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-323">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-324">**SKU**</span><span class="sxs-lookup"><span data-stu-id="5b60a-324">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-327">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5b60a-327">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-328">Número de unidade de manutenção de estoque do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5b60a-328">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="5b60a-329">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-329">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-330">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="5b60a-330">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-331">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5b60a-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-333">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanossegundos")</span><span class="sxs-lookup"><span data-stu-id="5b60a-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-334">Velocidade da memória física, em nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="5b60a-334">Speed of the physical memory, in nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-335">**Status**</span><span class="sxs-lookup"><span data-stu-id="5b60a-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-338">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5b60a-338">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-339">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5b60a-339">Current status of the object.</span></span> <span data-ttu-id="5b60a-340">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5b60a-341">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5b60a-341">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5b60a-342">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5b60a-342">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5b60a-343">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5b60a-343">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5b60a-344">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5b60a-344">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5b60a-345">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5b60a-345">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5b60a-346">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5b60a-346">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5b60a-347">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5b60a-347">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5b60a-348">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5b60a-348">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5b60a-349">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5b60a-349">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5b60a-350">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5b60a-350">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5b60a-351">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5b60a-351">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5b60a-352">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5b60a-352">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5b60a-353">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5b60a-353">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5b60a-354">**Tag**</span><span class="sxs-lookup"><span data-stu-id="5b60a-354">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-357">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5b60a-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-358">Cadeia de caracteres arbitrária que identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="5b60a-358">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="5b60a-359">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="5b60a-359">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="5b60a-360">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5b60a-360">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="5b60a-361">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="5b60a-361">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="5b60a-362">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="5b60a-362">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="5b60a-363">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="5b60a-363">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="5b60a-364">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-364">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-365">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="5b60a-365">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-366">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5b60a-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-368">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="5b60a-368">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-369">Largura total, em bits, da memória física, incluindo bits de verificação ou correção de erro.</span><span class="sxs-lookup"><span data-stu-id="5b60a-369">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="5b60a-370">Se não houver nenhum bit de correção de erro, o valor nessa propriedade deverá corresponder ao especificado para a propriedade **datalargura** .</span><span class="sxs-lookup"><span data-stu-id="5b60a-370">If there are no error correction bits, the value in this property should match that specified for the **DataWidth** property.</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-371">**Versão**</span><span class="sxs-lookup"><span data-stu-id="5b60a-371">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b60a-372">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5b60a-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5b60a-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b60a-374">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5b60a-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5b60a-375">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5b60a-375">Version of the physical element.</span></span>

<span data-ttu-id="5b60a-376">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-376">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b60a-377">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b60a-377">Remarks</span></span>

<span data-ttu-id="5b60a-378">A classe **CIM \_ PhysicalMemory** é derivada do [**\_ chip CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-378">The **CIM\_PhysicalMemory** class is derived from [**CIM\_Chip**](cim-chip.md).</span></span>

<span data-ttu-id="5b60a-379">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="5b60a-379">WMI does not implement this class.</span></span> <span data-ttu-id="5b60a-380">Para classes WMI derivadas do **CIM \_ PhysicalMemory**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5b60a-380">For WMI classes derived from **CIM\_PhysicalMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5b60a-381">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="5b60a-381">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5b60a-382">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="5b60a-382">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b60a-383">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b60a-383">Requirements</span></span>



| <span data-ttu-id="5b60a-384">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b60a-384">Requirement</span></span> | <span data-ttu-id="5b60a-385">Valor</span><span class="sxs-lookup"><span data-stu-id="5b60a-385">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b60a-386">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b60a-386">Minimum supported client</span></span><br/> | <span data-ttu-id="5b60a-387">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b60a-387">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b60a-388">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b60a-388">Minimum supported server</span></span><br/> | <span data-ttu-id="5b60a-389">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b60a-389">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b60a-390">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b60a-390">Namespace</span></span><br/>                | <span data-ttu-id="5b60a-391">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5b60a-391">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5b60a-392">MOF</span><span class="sxs-lookup"><span data-stu-id="5b60a-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b60a-393"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b60a-393"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b60a-394">DLL</span><span class="sxs-lookup"><span data-stu-id="5b60a-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b60a-395"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b60a-395"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b60a-396">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b60a-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b60a-397">**\_Chip CIM**</span><span class="sxs-lookup"><span data-stu-id="5b60a-397">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> </dl>

 

