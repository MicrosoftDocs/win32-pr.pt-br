---
description: A \_ classe CIM PhysicalLink representa o cabeamento dos elementos físicos.
ms.assetid: 0d96cb7f-ca50-4eb2-b8d4-e749bbe67ad7
ms.tgt_platform: multiple
title: Classe CIM_PhysicalLink
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalLink
- CIM_PhysicalLink.Caption
- CIM_PhysicalLink.CreationClassName
- CIM_PhysicalLink.Description
- CIM_PhysicalLink.InstallDate
- CIM_PhysicalLink.Length
- CIM_PhysicalLink.Manufacturer
- CIM_PhysicalLink.MaxLength
- CIM_PhysicalLink.MediaType
- CIM_PhysicalLink.Model
- CIM_PhysicalLink.Name
- CIM_PhysicalLink.OtherIdentifyingInfo
- CIM_PhysicalLink.PartNumber
- CIM_PhysicalLink.PoweredOn
- CIM_PhysicalLink.SerialNumber
- CIM_PhysicalLink.SKU
- CIM_PhysicalLink.Status
- CIM_PhysicalLink.Tag
- CIM_PhysicalLink.Version
- CIM_PhysicalLink.Wired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 659e73d9f5331d5c6648af00e147797dc6424130
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501040"
---
# <a name="cim_physicallink-class"></a><span data-ttu-id="a7d9d-103">\_Classe CIM PhysicalLink</span><span class="sxs-lookup"><span data-stu-id="a7d9d-103">CIM\_PhysicalLink class</span></span>

<span data-ttu-id="a7d9d-104">A classe **CIM \_ PhysicalLink** representa o cabeamento dos elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-104">The **CIM\_PhysicalLink** class represents the cabling of physical elements.</span></span> <span data-ttu-id="a7d9d-105">Por exemplo, cabos serial ou Ethernet e links de infravermelho seriam subclasses (se propriedades ou associações adicionais forem definidas) ou instâncias de **\_ PhysicalLink CIM**.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-105">For example, serial or Ethernet cables and infrared links would be subclasses (if additional properties or associations are defined) or instances of **CIM\_PhysicalLink**.</span></span> <span data-ttu-id="a7d9d-106">Normalmente, os vários cabos físicos em um pacote físico ou rede não são modelados.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-106">Typically, the numerous physical cables within a physical package or network are not modeled.</span></span> <span data-ttu-id="a7d9d-107">No entanto, quando os cabos ou os links são componentes críticos ou ativos marcados da empresa, os objetos podem ser instanciados usando essa classe ou uma de suas classes descendentes.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-107">However, when the cables or links are critical components or tagged assets of the company, the objects can be instantiated using this class or one of its descendant classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7d9d-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a7d9d-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a7d9d-110">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a7d9d-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d9d-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7d9d-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B82-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalLink : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  real64   Length;
  string   Manufacturer;
  real64   MaxLength;
  uint16   MediaType;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  Wired;
};
```

## <a name="members"></a><span data-ttu-id="a7d9d-113">Membros</span><span class="sxs-lookup"><span data-stu-id="a7d9d-113">Members</span></span>

<span data-ttu-id="a7d9d-114">A classe **CIM \_ PhysicalLink** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a7d9d-114">The **CIM\_PhysicalLink** class has these types of members:</span></span>

-   [<span data-ttu-id="a7d9d-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a7d9d-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7d9d-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a7d9d-116">Properties</span></span>

<span data-ttu-id="a7d9d-117">A classe **CIM \_ PhysicalLink** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-117">The **CIM\_PhysicalLink** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7d9d-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-122">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-122">Short textual description of the object.</span></span>

<span data-ttu-id="a7d9d-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-127">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-128">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a7d9d-129">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a7d9d-130">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-134">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-135">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-135">Textual description of the object.</span></span>

<span data-ttu-id="a7d9d-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-138">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-140">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-141">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-141">Date and time the object was installed.</span></span> <span data-ttu-id="a7d9d-142">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a7d9d-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-144">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-145">Tipo de dados: **real64**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-145">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-147">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pés")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-147">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-148">Comprimento atual do link físico, em pés.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-148">Current length of the physical link, in feet.</span></span> <span data-ttu-id="a7d9d-149">Para algumas conexões, especialmente as tecnologias sem fio, essa propriedade pode não ser aplicável e deve ser deixada não inicializada.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-149">For some connections, especially wireless technologies, this property might not be applicable and should be left uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-150">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-150">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-153">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-153">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-154">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-154">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="a7d9d-155">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-155">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="a7d9d-156">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-156">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-157">**MaxLength**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-157">**MaxLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-158">Tipo de dados: **real64**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-158">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-160">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pés")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-160">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("feet")</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-161">Comprimento máximo do link físico em pés.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-161">Maximum length of the physical link in feet.</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-162">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-162">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-165">Tipo de mídia por meio da qual os sinais de transmissão são aprovados.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-165">Type of media through which transmission signals pass.</span></span> <span data-ttu-id="a7d9d-166">A mídia de rede comum inclui o cabo trançado, coaxial e a fibra ótica.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-166">Common network media include twisted-pair, coaxial, and fiber-optic cable.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7d9d-167">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-167">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a7d9d-168">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat1"></span><span id="cat1"></span><span id="CAT1"></span>

<span data-ttu-id="a7d9d-169">**Cat1** (2)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-169">**Cat1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat2"></span><span id="cat2"></span><span id="CAT2"></span>

<span data-ttu-id="a7d9d-170">**Cat2** (3)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-170">**Cat2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat3"></span><span id="cat3"></span><span id="CAT3"></span>

<span data-ttu-id="a7d9d-171">**Cat3** (4)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-171">**Cat3** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat4"></span><span id="cat4"></span><span id="CAT4"></span>

<span data-ttu-id="a7d9d-172">**Cat4** (5)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-172">**Cat4** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Cat5"></span><span id="cat5"></span><span id="CAT5"></span>

<span data-ttu-id="a7d9d-173">**CAT5** (6)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-173">**Cat5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="50-ohm_Coaxial"></span><span id="50-ohm_coaxial"></span><span id="50-OHM_COAXIAL"></span>

<span data-ttu-id="a7d9d-174">**50-ohm coaxial** (7)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-174">**50-ohm Coaxial** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="75-ohm_Coaxial"></span><span id="75-ohm_coaxial"></span><span id="75-OHM_COAXIAL"></span>

<span data-ttu-id="a7d9d-175">**75-ohm coaxial** (8)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-175">**75-ohm Coaxial** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="100-ohm_Coaxial"></span><span id="100-ohm_coaxial"></span><span id="100-OHM_COAXIAL"></span>

<span data-ttu-id="a7d9d-176">**100-ohm coaxial** (9)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-176">**100-ohm Coaxial** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber-optic"></span><span id="fiber-optic"></span><span id="FIBER-OPTIC"></span>

<span data-ttu-id="a7d9d-177">**Fibra óptica** (10)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-177">**Fiber-optic** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP"></span><span id="utp"></span>

<span data-ttu-id="a7d9d-178">**UTP** (11)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-178">**UTP** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="STP"></span><span id="stp"></span>

<span data-ttu-id="a7d9d-179">**STP** (12)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-179">**STP** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon_Cable"></span><span id="ribbon_cable"></span><span id="RIBBON_CABLE"></span>

<span data-ttu-id="a7d9d-180">**Cabo de faixa de fita** (13)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-180">**Ribbon Cable** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Twinaxial"></span><span id="twinaxial"></span><span id="TWINAXIAL"></span>

<span data-ttu-id="a7d9d-181">**Twinaxial** (14)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-181">**Twinaxial** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_9um"></span><span id="optical_9um"></span><span id="OPTICAL_9UM"></span>

<span data-ttu-id="a7d9d-182">**9Um óptico** (15)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-182">**Optical 9um** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_50um"></span><span id="optical_50um"></span><span id="OPTICAL_50UM"></span>

<span data-ttu-id="a7d9d-183">**50Um óptico** (16)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-183">**Optical 50um** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical_62.5um"></span><span id="optical_62.5um"></span><span id="OPTICAL_62.5UM"></span>

<span data-ttu-id="a7d9d-184">**Óptico de 62,5 um** (17)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-184">**Optical 62.5um** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a7d9d-185">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-185">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-188">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-189">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-189">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="a7d9d-190">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-190">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-191">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-191">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-194">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-194">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-195">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-195">Label by which the object is known.</span></span> <span data-ttu-id="a7d9d-196">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-196">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a7d9d-197">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-198">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-198">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-201">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-201">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="a7d9d-202">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-202">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="a7d9d-203">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="a7d9d-203">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="a7d9d-204">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-204">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-205">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-205">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-206">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-208">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-209">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-209">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="a7d9d-210">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-210">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-211">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-211">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-212">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-214">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-214">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="a7d9d-215">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-216">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-216">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-219">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-220">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-220">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="a7d9d-221">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-222">**SKU**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-222">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-225">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-225">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-226">Número de unidade de manutenção de estoque do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-226">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="a7d9d-227">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-228">**Status**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-228">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-229">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-231">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-232">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-232">Current status of the object.</span></span>

<span data-ttu-id="a7d9d-233">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-233">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a7d9d-234">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a7d9d-234">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a7d9d-235">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-235">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a7d9d-236">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-236">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a7d9d-237">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-237">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7d9d-238">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-238">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a7d9d-239">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-239">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a7d9d-240">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-240">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a7d9d-241">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-241">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a7d9d-242">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-242">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a7d9d-243">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-243">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a7d9d-244">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-244">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a7d9d-245">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-245">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a7d9d-246">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="a7d9d-246">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a7d9d-247">**Tag**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-247">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-248">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-250">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-250">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-251">Cadeia de caracteres arbitrária que identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-251">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="a7d9d-252">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-252">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="a7d9d-253">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-253">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="a7d9d-254">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-254">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="a7d9d-255">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-255">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="a7d9d-256">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-256">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="a7d9d-257">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-258">**Versão**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-259">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-261">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a7d9d-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-262">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-262">Version of the physical element.</span></span>

<span data-ttu-id="a7d9d-263">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7d9d-264">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-264">**Wired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7d9d-265">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a7d9d-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a7d9d-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7d9d-267">Se for **true**, o link físico será um cabo.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-267">If **TRUE**, the physical link is a cable.</span></span> <span data-ttu-id="a7d9d-268">Caso contrário, é uma conexão sem fio.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-268">Otherwise, it is a wireless connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7d9d-269">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7d9d-269">Remarks</span></span>

<span data-ttu-id="a7d9d-270">A classe **CIM \_ PhysicalLink** é derivada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7d9d-270">The **CIM\_PhysicalLink** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="a7d9d-271">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-271">WMI does not implement this class.</span></span>

<span data-ttu-id="a7d9d-272">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-272">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a7d9d-273">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="a7d9d-273">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d9d-274">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7d9d-274">Requirements</span></span>



| <span data-ttu-id="a7d9d-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7d9d-275">Requirement</span></span> | <span data-ttu-id="a7d9d-276">Valor</span><span class="sxs-lookup"><span data-stu-id="a7d9d-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d9d-277">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7d9d-277">Minimum supported client</span></span><br/> | <span data-ttu-id="a7d9d-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7d9d-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7d9d-279">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7d9d-279">Minimum supported server</span></span><br/> | <span data-ttu-id="a7d9d-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7d9d-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7d9d-281">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7d9d-281">Namespace</span></span><br/>                | <span data-ttu-id="a7d9d-282">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a7d9d-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7d9d-283">MOF</span><span class="sxs-lookup"><span data-stu-id="a7d9d-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7d9d-284"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7d9d-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7d9d-285">DLL</span><span class="sxs-lookup"><span data-stu-id="a7d9d-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7d9d-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7d9d-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7d9d-287">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7d9d-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d9d-288">**Físico do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a7d9d-288">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

