---
description: A \_ classe de chip CIM representa o tipo de hardware de circuito integrado, incluindo ASICs, processadores, chips de memória e assim por diante.
ms.assetid: 3c2b0023-5d02-49b9-90f5-d66eb8a103f0
ms.tgt_platform: multiple
title: Classe CIM_Chip
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chip
- CIM_Chip.Caption
- CIM_Chip.Description
- CIM_Chip.InstallDate
- CIM_Chip.Name
- CIM_Chip.Status
- CIM_Chip.CreationClassName
- CIM_Chip.Manufacturer
- CIM_Chip.Model
- CIM_Chip.OtherIdentifyingInfo
- CIM_Chip.PartNumber
- CIM_Chip.PoweredOn
- CIM_Chip.SerialNumber
- CIM_Chip.SKU
- CIM_Chip.Tag
- CIM_Chip.Version
- CIM_Chip.HotSwappable
- CIM_Chip.Removable
- CIM_Chip.Replaceable
- CIM_Chip.FormFactor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 953ae371edca42409246307b21aad69a02cf4a66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457082"
---
# <a name="cim_chip-class"></a><span data-ttu-id="5e402-103">\_Classe de chip CIM</span><span class="sxs-lookup"><span data-stu-id="5e402-103">CIM\_Chip class</span></span>

<span data-ttu-id="5e402-104">A classe de **\_ chip CIM** representa o tipo de hardware de circuito integrado, incluindo ASICs, processadores, chips de memória e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5e402-104">The **CIM\_Chip** class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e402-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="5e402-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5e402-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5e402-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5e402-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5e402-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5e402-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5e402-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e402-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e402-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chip : CIM_PhysicalComponent
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  uint16   FormFactor;
};
```

## <a name="members"></a><span data-ttu-id="5e402-110">Membros</span><span class="sxs-lookup"><span data-stu-id="5e402-110">Members</span></span>

<span data-ttu-id="5e402-111">A classe de **\_ chip CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5e402-111">The **CIM\_Chip** class has these types of members:</span></span>

-   [<span data-ttu-id="5e402-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5e402-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e402-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5e402-113">Properties</span></span>

<span data-ttu-id="5e402-114">A classe de **\_ chip CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5e402-114">The **CIM\_Chip** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e402-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5e402-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5e402-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5e402-119">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5e402-119">A short textual description of the object.</span></span>

<span data-ttu-id="5e402-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5e402-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-124">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5e402-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e402-125">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5e402-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5e402-126">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5e402-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5e402-127">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-127">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5e402-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-131">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="5e402-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5e402-132">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5e402-132">A textual description of the object.</span></span>

<span data-ttu-id="5e402-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-134">**FormFactor**</span><span class="sxs-lookup"><span data-stu-id="5e402-134">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e402-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e402-137">Fator forma de implementação para o chip.</span><span class="sxs-lookup"><span data-stu-id="5e402-137">Implementation form factor for the chip.</span></span> <span data-ttu-id="5e402-138">Os valores a seguir podem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="5e402-138">The following values can be specified.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e402-139">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5e402-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5e402-140">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5e402-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

<span data-ttu-id="5e402-141">**SIP** (2)</span><span class="sxs-lookup"><span data-stu-id="5e402-141">**SIP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DIP"></span><span id="dip"></span>

<span data-ttu-id="5e402-142">**DIP** (3)</span><span class="sxs-lookup"><span data-stu-id="5e402-142">**DIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP"></span><span id="zip"></span>

<span data-ttu-id="5e402-143">**Zip** (4)</span><span class="sxs-lookup"><span data-stu-id="5e402-143">**ZIP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOJ"></span><span id="soj"></span>

<span data-ttu-id="5e402-144">**SOJ** (5)</span><span class="sxs-lookup"><span data-stu-id="5e402-144">**SOJ** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="5e402-145">**Proprietário** (6)</span><span class="sxs-lookup"><span data-stu-id="5e402-145">**Proprietary** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SIMM"></span><span id="simm"></span>

<span data-ttu-id="5e402-146">**SIMM** (7)</span><span class="sxs-lookup"><span data-stu-id="5e402-146">**SIMM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DIMM"></span><span id="dimm"></span>

<span data-ttu-id="5e402-147">**DIMM** (8)</span><span class="sxs-lookup"><span data-stu-id="5e402-147">**DIMM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TSOP"></span><span id="tsop"></span>

<span data-ttu-id="5e402-148">**TSOP** (9)</span><span class="sxs-lookup"><span data-stu-id="5e402-148">**TSOP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PGA"></span><span id="pga"></span>

<span data-ttu-id="5e402-149">**PGA** (10)</span><span class="sxs-lookup"><span data-stu-id="5e402-149">**PGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="RIMM"></span><span id="rimm"></span>

<span data-ttu-id="5e402-150">**RIMM** (11)</span><span class="sxs-lookup"><span data-stu-id="5e402-150">**RIMM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SODIMM"></span><span id="sodimm"></span>

<span data-ttu-id="5e402-151">**SODIMM** (12)</span><span class="sxs-lookup"><span data-stu-id="5e402-151">**SODIMM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SRIMM"></span><span id="srimm"></span>

<span data-ttu-id="5e402-152">**SRIMM** (13)</span><span class="sxs-lookup"><span data-stu-id="5e402-152">**SRIMM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SMD"></span><span id="smd"></span>

<span data-ttu-id="5e402-153">**SMD** (14)</span><span class="sxs-lookup"><span data-stu-id="5e402-153">**SMD** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSMP"></span><span id="ssmp"></span>

<span data-ttu-id="5e402-154">**SSMP** (15)</span><span class="sxs-lookup"><span data-stu-id="5e402-154">**SSMP** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="QFP"></span><span id="qfp"></span>

<span data-ttu-id="5e402-155">**QFP** (16)</span><span class="sxs-lookup"><span data-stu-id="5e402-155">**QFP** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="TQFP"></span><span id="tqfp"></span>

<span data-ttu-id="5e402-156">**TQFP** (17)</span><span class="sxs-lookup"><span data-stu-id="5e402-156">**TQFP** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SOIC"></span><span id="soic"></span>

<span data-ttu-id="5e402-157">**SOIC** (18)</span><span class="sxs-lookup"><span data-stu-id="5e402-157">**SOIC** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="LCC"></span><span id="lcc"></span>

<span data-ttu-id="5e402-158">**LCC** (19)</span><span class="sxs-lookup"><span data-stu-id="5e402-158">**LCC** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PLCC"></span><span id="plcc"></span>

<span data-ttu-id="5e402-159">**PLCC** (20)</span><span class="sxs-lookup"><span data-stu-id="5e402-159">**PLCC** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="BGA"></span><span id="bga"></span>

<span data-ttu-id="5e402-160">**BGA** (21)</span><span class="sxs-lookup"><span data-stu-id="5e402-160">**BGA** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="FPBGA"></span><span id="fpbga"></span>

<span data-ttu-id="5e402-161">**FPBGA** (22)</span><span class="sxs-lookup"><span data-stu-id="5e402-161">**FPBGA** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="LGA"></span><span id="lga"></span>

<span data-ttu-id="5e402-162">**LGA** (23)</span><span class="sxs-lookup"><span data-stu-id="5e402-162">**LGA** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="FB-DIMM"></span><span id="fb-dimm"></span>

<span data-ttu-id="5e402-163">**FB-DIMM** (24)</span><span class="sxs-lookup"><span data-stu-id="5e402-163">**FB-DIMM** (24)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5e402-164">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="5e402-164">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-165">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5e402-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e402-167">Se **for true**, o pacote poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="5e402-167">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="5e402-168">Um pacote físico pode ser intercambiável se o elemento puder ser substituído por um fisicamente diferente (mas equivalente) um enquanto o pacote que o contém está ativado.</span><span class="sxs-lookup"><span data-stu-id="5e402-168">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="5e402-169">Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="5e402-169">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="5e402-170">Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="5e402-170">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="5e402-171">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-171">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5e402-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-173">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5e402-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-175">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5e402-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5e402-176">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5e402-176">Indicates when the object was installed.</span></span> <span data-ttu-id="5e402-177">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="5e402-177">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5e402-178">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-179">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="5e402-179">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-182">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5e402-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e402-183">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5e402-183">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="5e402-184">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-184">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="5e402-185">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-185">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-186">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="5e402-186">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-189">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5e402-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5e402-190">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="5e402-190">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="5e402-191">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-191">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-192">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5e402-192">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-195">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5e402-195">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5e402-196">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5e402-196">Label by which the object is known.</span></span> <span data-ttu-id="5e402-197">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="5e402-197">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5e402-198">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-199">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5e402-199">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e402-202">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5e402-202">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="5e402-203">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="5e402-203">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="5e402-204">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="5e402-204">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="5e402-205">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-206">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="5e402-206">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-209">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5e402-209">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e402-210">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5e402-210">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="5e402-211">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-211">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-212">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="5e402-212">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-213">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5e402-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e402-215">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="5e402-215">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="5e402-216">Caso contrário, ele estará desativado no momento.</span><span class="sxs-lookup"><span data-stu-id="5e402-216">Otherwise, it is currently off.</span></span>

<span data-ttu-id="5e402-217">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-217">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-218">**Removível**</span><span class="sxs-lookup"><span data-stu-id="5e402-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-219">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5e402-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e402-221">Se for **true**, esse elemento será projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem comprometer a função do empacotamento geral.</span><span class="sxs-lookup"><span data-stu-id="5e402-221">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="5e402-222">Um pacote é considerado removível, mesmo que a energia precise ser desligada para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="5e402-222">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="5e402-223">Se a energia puder ser ativada e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="5e402-223">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="5e402-224">Por exemplo, um chip de processador atualizável é removível.</span><span class="sxs-lookup"><span data-stu-id="5e402-224">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="5e402-225">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-225">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-226">**Peças**</span><span class="sxs-lookup"><span data-stu-id="5e402-226">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-227">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5e402-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e402-229">Se for **true**, é possível substituir o elemento por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="5e402-229">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="5e402-230">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="5e402-230">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="5e402-231">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="5e402-231">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="5e402-232">Todos os componentes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="5e402-232">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="5e402-233">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-233">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-234">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="5e402-234">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-235">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-237">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5e402-237">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5e402-238">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5e402-238">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="5e402-239">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-240">**SKU**</span><span class="sxs-lookup"><span data-stu-id="5e402-240">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-241">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-243">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5e402-243">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5e402-244">Número de unidade de manutenção de estoque para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5e402-244">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="5e402-245">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-245">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-246">**Status**</span><span class="sxs-lookup"><span data-stu-id="5e402-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-249">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5e402-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5e402-250">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5e402-250">String that indicates the current status of the object.</span></span> <span data-ttu-id="5e402-251">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="5e402-251">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5e402-252">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="5e402-252">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5e402-253">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="5e402-253">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5e402-254">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="5e402-254">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5e402-255">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="5e402-255">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5e402-256">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="5e402-256">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5e402-257">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-257">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5e402-258">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5e402-258">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5e402-259">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5e402-259">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5e402-260">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5e402-260">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5e402-261">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5e402-261">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e402-262">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5e402-262">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5e402-263">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5e402-263">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5e402-264">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5e402-264">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5e402-265">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5e402-265">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5e402-266">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5e402-266">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5e402-267">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5e402-267">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5e402-268">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5e402-268">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5e402-269">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5e402-269">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5e402-270">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5e402-270">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5e402-271">**Tag**</span><span class="sxs-lookup"><span data-stu-id="5e402-271">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-272">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-274">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5e402-274">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e402-275">Identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="5e402-275">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="5e402-276">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="5e402-276">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="5e402-277">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5e402-277">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="5e402-278">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="5e402-278">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="5e402-279">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="5e402-279">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="5e402-280">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="5e402-280">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="5e402-281">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e402-282">**Versão**</span><span class="sxs-lookup"><span data-stu-id="5e402-282">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e402-283">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5e402-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e402-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5e402-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e402-285">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5e402-285">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5e402-286">Indica a versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5e402-286">Indicates the version of the physical element.</span></span>

<span data-ttu-id="5e402-287">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e402-288">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e402-288">Remarks</span></span>

<span data-ttu-id="5e402-289">A classe de **\_ chip CIM** é derivada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-289">The **CIM\_Chip** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="5e402-290">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="5e402-290">WMI does not implement this class.</span></span> <span data-ttu-id="5e402-291">Para obter mais informações sobre classes derivadas **do \_ chip CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5e402-291">For more information about classes derived from **CIM\_Chip**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5e402-292">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="5e402-292">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5e402-293">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="5e402-293">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e402-294">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e402-294">Requirements</span></span>



| <span data-ttu-id="5e402-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e402-295">Requirement</span></span> | <span data-ttu-id="5e402-296">Valor</span><span class="sxs-lookup"><span data-stu-id="5e402-296">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e402-297">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e402-297">Minimum supported client</span></span><br/> | <span data-ttu-id="5e402-298">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e402-298">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e402-299">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e402-299">Minimum supported server</span></span><br/> | <span data-ttu-id="5e402-300">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e402-300">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e402-301">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e402-301">Namespace</span></span><br/>                | <span data-ttu-id="5e402-302">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5e402-302">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5e402-303">MOF</span><span class="sxs-lookup"><span data-stu-id="5e402-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e402-304"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e402-304"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e402-305">DLL</span><span class="sxs-lookup"><span data-stu-id="5e402-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e402-306"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e402-306"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e402-307">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e402-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e402-308">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="5e402-308">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

