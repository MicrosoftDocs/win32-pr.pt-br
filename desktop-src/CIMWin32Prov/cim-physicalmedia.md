---
description: A \_ classe CIM PhysicalMedia representa tipos de mídia de documentação e armazenamento, como fitas, CD ROMs e assim por diante.
ms.assetid: ba258e53-4a82-4b30-aadd-54448841cd06
ms.tgt_platform: multiple
title: Classe CIM_PhysicalMedia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMedia
- CIM_PhysicalMedia.Capacity
- CIM_PhysicalMedia.Caption
- CIM_PhysicalMedia.CleanerMedia
- CIM_PhysicalMedia.CreationClassName
- CIM_PhysicalMedia.Description
- CIM_PhysicalMedia.HotSwappable
- CIM_PhysicalMedia.InstallDate
- CIM_PhysicalMedia.Manufacturer
- CIM_PhysicalMedia.MediaDescription
- CIM_PhysicalMedia.MediaType
- CIM_PhysicalMedia.Model
- CIM_PhysicalMedia.Name
- CIM_PhysicalMedia.OtherIdentifyingInfo
- CIM_PhysicalMedia.PartNumber
- CIM_PhysicalMedia.PoweredOn
- CIM_PhysicalMedia.Removable
- CIM_PhysicalMedia.Replaceable
- CIM_PhysicalMedia.SerialNumber
- CIM_PhysicalMedia.SKU
- CIM_PhysicalMedia.Status
- CIM_PhysicalMedia.Tag
- CIM_PhysicalMedia.Version
- CIM_PhysicalMedia.WriteProtectOn
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8709128c189956bba4bc371e0f5bfb30d67b49f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172508"
---
# <a name="cim_physicalmedia-class"></a><span data-ttu-id="53d87-103">\_Classe CIM PhysicalMedia</span><span class="sxs-lookup"><span data-stu-id="53d87-103">CIM\_PhysicalMedia class</span></span>

<span data-ttu-id="53d87-104">A classe **CIM \_ PhysicalMedia** representa tipos de mídia de documentação e armazenamento, como fitas, CD ROMs e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="53d87-104">The **CIM\_PhysicalMedia** class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span> <span data-ttu-id="53d87-105">Essa classe normalmente é usada para localizar e gerenciar mídia removível (versus mídia selada com o dispositivo de acesso à mídia como um único pacote, como discos rígidos).</span><span class="sxs-lookup"><span data-stu-id="53d87-105">This class is typically used to locate and manage removable media (versus media sealed with the media access device as a single package, such as hard disks).</span></span> <span data-ttu-id="53d87-106">No entanto, a mídia selada também pode ser modelada usando essa classe quando a mídia está associada ao pacote físico usando a relação de [**\_ PackagedComponent do CIM**](cim-packagedcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="53d87-106">Sealed media, however, can also be modeled using this class when the media is associated with the physical package using the [**CIM\_PackagedComponent**](cim-packagedcomponent.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53d87-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="53d87-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="53d87-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="53d87-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="53d87-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="53d87-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="53d87-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="53d87-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d87-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53d87-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMedia : CIM_PhysicalComponent
{
  uint64   Capacity;
  string   Caption;
  boolean  CleanerMedia;
  string   CreationClassName;
  string   Description;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   MediaDescription;
  uint16   MediaType;
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
  string   Version;
  boolean  WriteProtectOn;
};
```

## <a name="members"></a><span data-ttu-id="53d87-112">Membros</span><span class="sxs-lookup"><span data-stu-id="53d87-112">Members</span></span>

<span data-ttu-id="53d87-113">A classe **CIM \_ PhysicalMedia** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="53d87-113">The **CIM\_PhysicalMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="53d87-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="53d87-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53d87-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="53d87-115">Properties</span></span>

<span data-ttu-id="53d87-116">A classe **CIM \_ PhysicalMedia** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="53d87-116">The **CIM\_PhysicalMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53d87-117">**Capacidade**</span><span class="sxs-lookup"><span data-stu-id="53d87-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-118">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="53d87-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-120">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="53d87-120">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="53d87-121">Número de bytes que podem ser lidos ou gravados em uma mídia.</span><span class="sxs-lookup"><span data-stu-id="53d87-121">Number of bytes that can be read from, or written to, a media.</span></span> <span data-ttu-id="53d87-122">Essa propriedade não é aplicável à cópia impressa (documentação) ou à mídia de limpeza.</span><span class="sxs-lookup"><span data-stu-id="53d87-122">This property is not applicable to hard copy (documentation) or cleaner media.</span></span> <span data-ttu-id="53d87-123">A compactação de dados não deve ser assumida, pois aumentaria o valor nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="53d87-123">Data compression should not be assumed, as it would increase the value in this property.</span></span> <span data-ttu-id="53d87-124">Para fitas, deve-se supor que nenhuma marca de arquivo ou áreas de espaço em branco sejam registradas na mídia.</span><span class="sxs-lookup"><span data-stu-id="53d87-124">For tapes, it should be assumed that no file marks or blank space areas are recorded on the media.</span></span>

<span data-ttu-id="53d87-125">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="53d87-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-126">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="53d87-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-129">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="53d87-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="53d87-130">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="53d87-130">Short textual description of the object.</span></span>

<span data-ttu-id="53d87-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-132">**CleanerMedia**</span><span class="sxs-lookup"><span data-stu-id="53d87-132">**CleanerMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-133">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="53d87-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53d87-135">Se for **true**, a mídia física será usada para fins de limpeza, não para armazenamento de dados.</span><span class="sxs-lookup"><span data-stu-id="53d87-135">If **TRUE**, the physical media is used for cleaning purposes, not data storage.</span></span>

</dd> <dt>

<span data-ttu-id="53d87-136">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="53d87-136">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-139">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="53d87-139">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53d87-140">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="53d87-140">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="53d87-141">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="53d87-141">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="53d87-142">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-142">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-143">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="53d87-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-146">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="53d87-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="53d87-147">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="53d87-147">Textual description of the object.</span></span>

<span data-ttu-id="53d87-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-149">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="53d87-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-150">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="53d87-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53d87-152">Se **for true**, o pacote poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="53d87-152">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="53d87-153">Um pacote físico pode ser intercambiável se o elemento puder ser substituído por um fisicamente diferente (mas equivalente) um enquanto o pacote que o contém está ativado.</span><span class="sxs-lookup"><span data-stu-id="53d87-153">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="53d87-154">Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="53d87-154">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="53d87-155">Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="53d87-155">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="53d87-156">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-156">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="53d87-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-158">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="53d87-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-160">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="53d87-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="53d87-161">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="53d87-161">Date and time the object was installed.</span></span> <span data-ttu-id="53d87-162">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="53d87-162">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="53d87-163">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-164">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="53d87-164">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-167">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="53d87-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53d87-168">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="53d87-168">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="53d87-169">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-169">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="53d87-170">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-170">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-171">**MediaDescription**</span><span class="sxs-lookup"><span data-stu-id="53d87-171">**MediaDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-174">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalMedia**.**MediaType**")</span><span class="sxs-lookup"><span data-stu-id="53d87-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaType**")</span></span>
</dt> </dl>

<span data-ttu-id="53d87-175">Detalhes adicionais relacionados à enumeração de **MediaType** .</span><span class="sxs-lookup"><span data-stu-id="53d87-175">Additional detail related to the **MediaType** enumeration.</span></span> <span data-ttu-id="53d87-176">Por exemplo, se o valor 3 ("cartucho QIC") for especificado, essa propriedade indicará se a fita tem largura ou 1/4 polegadas, que é compatível com o onbarra, com trava e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="53d87-176">For example, if value 3 ("QIC Cartridge") is specified, this property would indicate whether the tape is wide or 1/4 inch, pre-formatted, Travan compatible, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="53d87-177">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="53d87-177">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-178">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="53d87-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-180">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalMedia**.**MediaDescription**")</span><span class="sxs-lookup"><span data-stu-id="53d87-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalMedia**.**MediaDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="53d87-181">Tipo de mídia física.</span><span class="sxs-lookup"><span data-stu-id="53d87-181">Type of physical media.</span></span> <span data-ttu-id="53d87-182">A propriedade **MediaDescription** fornece mais definição explícita do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="53d87-182">The **MediaDescription** property provides more explicit definition of the media type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="53d87-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="53d87-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="53d87-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="53d87-184"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>

<span data-ttu-id="53d87-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Cartucho de fita** (2)</span><span class="sxs-lookup"><span data-stu-id="53d87-185"><span id="Tape_Cartridge"></span><span id="tape_cartridge"></span><span id="TAPE_CARTRIDGE"></span>**Tape Cartridge** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>

<span data-ttu-id="53d87-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**Cartucho QIC** (3)</span><span class="sxs-lookup"><span data-stu-id="53d87-186"><span id="QIC_Cartridge"></span><span id="qic_cartridge"></span><span id="QIC_CARTRIDGE"></span>**QIC Cartridge** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>

<span data-ttu-id="53d87-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**Cartucho de AIT** (4)</span><span class="sxs-lookup"><span data-stu-id="53d87-187"><span id="AIT_Cartridge"></span><span id="ait_cartridge"></span><span id="AIT_CARTRIDGE"></span>**AIT Cartridge** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>

<span data-ttu-id="53d87-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**Cartucho DTF** (5)</span><span class="sxs-lookup"><span data-stu-id="53d87-188"><span id="DTF_Cartridge"></span><span id="dtf_cartridge"></span><span id="DTF_CARTRIDGE"></span>**DTF Cartridge** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>

<span data-ttu-id="53d87-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**Cartucho dat** (6)</span><span class="sxs-lookup"><span data-stu-id="53d87-189"><span id="DAT_Cartridge"></span><span id="dat_cartridge"></span><span id="DAT_CARTRIDGE"></span>**DAT Cartridge** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="53d87-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**cartucho de fita 8mm** (7)</span><span class="sxs-lookup"><span data-stu-id="53d87-190"><span id="8mm_Tape_Cartridge"></span><span id="8mm_tape_cartridge"></span><span id="8MM_TAPE_CARTRIDGE"></span>**8mm Tape Cartridge** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>

<span data-ttu-id="53d87-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**cartucho de fita 19mm** (8)</span><span class="sxs-lookup"><span data-stu-id="53d87-191"><span id="19mm_Tape_Cartridge"></span><span id="19mm_tape_cartridge"></span><span id="19MM_TAPE_CARTRIDGE"></span>**19mm Tape Cartridge** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>

<span data-ttu-id="53d87-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**Cartucho DLT** (9)</span><span class="sxs-lookup"><span data-stu-id="53d87-192"><span id="DLT_Cartridge"></span><span id="dlt_cartridge"></span><span id="DLT_CARTRIDGE"></span>**DLT Cartridge** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>

<span data-ttu-id="53d87-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Cartucho de fita magnética de meia polegada** (10)</span><span class="sxs-lookup"><span data-stu-id="53d87-193"><span id="Half-Inch_Magnetic_Tape_Cartridge"></span><span id="half-inch_magnetic_tape_cartridge"></span><span id="HALF-INCH_MAGNETIC_TAPE_CARTRIDGE"></span>**Half-Inch Magnetic Tape Cartridge** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>

<span data-ttu-id="53d87-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Disco do cartucho** (11)</span><span class="sxs-lookup"><span data-stu-id="53d87-194"><span id="Cartridge_Disk"></span><span id="cartridge_disk"></span><span id="CARTRIDGE_DISK"></span>**Cartridge Disk** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>

<span data-ttu-id="53d87-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**Disco jaz** (12)</span><span class="sxs-lookup"><span data-stu-id="53d87-195"><span id="JAZ_Disk"></span><span id="jaz_disk"></span><span id="JAZ_DISK"></span>**JAZ Disk** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>

<span data-ttu-id="53d87-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**Disco Zip** (13)</span><span class="sxs-lookup"><span data-stu-id="53d87-196"><span id="ZIP_Disk"></span><span id="zip_disk"></span><span id="ZIP_DISK"></span>**ZIP Disk** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>

<span data-ttu-id="53d87-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**Disco SyQuest** (14)</span><span class="sxs-lookup"><span data-stu-id="53d87-197"><span id="SyQuest_Disk"></span><span id="syquest_disk"></span><span id="SYQUEST_DISK"></span>**SyQuest Disk** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>

<span data-ttu-id="53d87-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Disco removível do Winchester** (15)</span><span class="sxs-lookup"><span data-stu-id="53d87-198"><span id="Winchester_Removable_Disk"></span><span id="winchester_removable_disk"></span><span id="WINCHESTER_REMOVABLE_DISK"></span>**Winchester Removable Disk** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="53d87-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="53d87-199"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

<span data-ttu-id="53d87-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="53d87-200"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

<span data-ttu-id="53d87-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="53d87-201"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

<span data-ttu-id="53d87-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD gravável** (19)</span><span class="sxs-lookup"><span data-stu-id="53d87-202"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="WORM"></span><span id="worm"></span>

<span data-ttu-id="53d87-203"><span id="WORM"></span><span id="worm"></span>**Worm** (20)</span><span class="sxs-lookup"><span data-stu-id="53d87-203"><span id="WORM"></span><span id="worm"></span>**WORM** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>

<span data-ttu-id="53d87-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-óptico** (21)</span><span class="sxs-lookup"><span data-stu-id="53d87-204"><span id="Magneto-Optical"></span><span id="magneto-optical"></span><span id="MAGNETO-OPTICAL"></span>**Magneto-Optical** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

<span data-ttu-id="53d87-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="53d87-205"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_RW"></span><span id="dvd_rw"></span>

<span data-ttu-id="53d87-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD + RW** (23)</span><span class="sxs-lookup"><span data-stu-id="53d87-206"><span id="DVD_RW"></span><span id="dvd_rw"></span>**DVD+RW** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

<span data-ttu-id="53d87-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="53d87-207"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

<span data-ttu-id="53d87-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="53d87-208"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

<span data-ttu-id="53d87-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-vídeo** (26)</span><span class="sxs-lookup"><span data-stu-id="53d87-209"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

<span data-ttu-id="53d87-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**DivX** (27)</span><span class="sxs-lookup"><span data-stu-id="53d87-210"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>

<span data-ttu-id="53d87-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Disquete/disquete** (28)</span><span class="sxs-lookup"><span data-stu-id="53d87-211"><span id="Floppy_Diskette"></span><span id="floppy_diskette"></span><span id="FLOPPY_DISKETTE"></span>**Floppy/Diskette** (28)</span></span>


</dt> <dd>

<span data-ttu-id="53d87-212">Disquete</span><span class="sxs-lookup"><span data-stu-id="53d87-212">Floppy disk</span></span>

</dd> <dt>

<span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>

<span data-ttu-id="53d87-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Disco rígido** (29)</span><span class="sxs-lookup"><span data-stu-id="53d87-213"><span id="Hard_Disk"></span><span id="hard_disk"></span><span id="HARD_DISK"></span>**Hard Disk** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>

<span data-ttu-id="53d87-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Placa de memória** (30)</span><span class="sxs-lookup"><span data-stu-id="53d87-214"><span id="Memory_Card"></span><span id="memory_card"></span><span id="MEMORY_CARD"></span>**Memory Card** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>

<span data-ttu-id="53d87-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Cópia impressa** (31)</span><span class="sxs-lookup"><span data-stu-id="53d87-215"><span id="Hard_Copy"></span><span id="hard_copy"></span><span id="HARD_COPY"></span>**Hard Copy** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>

<span data-ttu-id="53d87-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Disco clique** (32)</span><span class="sxs-lookup"><span data-stu-id="53d87-216"><span id="Clik_Disk"></span><span id="clik_disk"></span><span id="CLIK_DISK"></span>**Clik Disk** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

<span data-ttu-id="53d87-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="53d87-217"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

<span data-ttu-id="53d87-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-da** (34)</span><span class="sxs-lookup"><span data-stu-id="53d87-218"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

<span data-ttu-id="53d87-219"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="53d87-219"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

<span data-ttu-id="53d87-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD gravável** (36)</span><span class="sxs-lookup"><span data-stu-id="53d87-220"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

<span data-ttu-id="53d87-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="53d87-221"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

<span data-ttu-id="53d87-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-áudio** (38)</span><span class="sxs-lookup"><span data-stu-id="53d87-222"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

<span data-ttu-id="53d87-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="53d87-223"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

<span data-ttu-id="53d87-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="53d87-224"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

<span data-ttu-id="53d87-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="53d87-225"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

<span data-ttu-id="53d87-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="53d87-226"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>

<span data-ttu-id="53d87-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magneto-óptico regravável** (43)</span><span class="sxs-lookup"><span data-stu-id="53d87-227"><span id="Magneto-Optical_Rewriteable"></span><span id="magneto-optical_rewriteable"></span><span id="MAGNETO-OPTICAL_REWRITEABLE"></span>**Magneto-Optical Rewriteable** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>

<span data-ttu-id="53d87-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Magneto-óptico gravar uma vez** (44)</span><span class="sxs-lookup"><span data-stu-id="53d87-228"><span id="Magneto-Optical_Write_Once"></span><span id="magneto-optical_write_once"></span><span id="MAGNETO-OPTICAL_WRITE_ONCE"></span>**Magneto-Optical Write Once** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>

<span data-ttu-id="53d87-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magneto-óptico regravável (LIMDOW)** (45)</span><span class="sxs-lookup"><span data-stu-id="53d87-229"><span id="Magneto-Optical_Rewriteable__LIMDOW_"></span><span id="magneto-optical_rewriteable__limdow_"></span><span id="MAGNETO-OPTICAL_REWRITEABLE__LIMDOW_"></span>**Magneto-Optical Rewriteable (LIMDOW)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>

<span data-ttu-id="53d87-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>A **alteração de fase é gravada uma vez** (46)</span><span class="sxs-lookup"><span data-stu-id="53d87-230"><span id="Phase_Change_Write_Once"></span><span id="phase_change_write_once"></span><span id="PHASE_CHANGE_WRITE_ONCE"></span>**Phase Change Write Once** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>

<span data-ttu-id="53d87-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Alteração de fase regravável** (47)</span><span class="sxs-lookup"><span data-stu-id="53d87-231"><span id="Phase_Change_Rewriteable"></span><span id="phase_change_rewriteable"></span><span id="PHASE_CHANGE_REWRITEABLE"></span>**Phase Change Rewriteable** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>

<span data-ttu-id="53d87-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Alteração de fase dupla regravável** (48)</span><span class="sxs-lookup"><span data-stu-id="53d87-232"><span id="Phase_Change_Dual_Rewriteable"></span><span id="phase_change_dual_rewriteable"></span><span id="PHASE_CHANGE_DUAL_REWRITEABLE"></span>**Phase Change Dual Rewriteable** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>

<span data-ttu-id="53d87-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Ablative gravar uma vez** (49)</span><span class="sxs-lookup"><span data-stu-id="53d87-233"><span id="Ablative_Write_Once"></span><span id="ablative_write_once"></span><span id="ABLATIVE_WRITE_ONCE"></span>**Ablative Write Once** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>

<span data-ttu-id="53d87-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Gravação de campo próximo** (50)</span><span class="sxs-lookup"><span data-stu-id="53d87-234"><span id="Near_Field_Recording"></span><span id="near_field_recording"></span><span id="NEAR_FIELD_RECORDING"></span>**Near Field Recording** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>

<span data-ttu-id="53d87-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQic** (51)</span><span class="sxs-lookup"><span data-stu-id="53d87-235"><span id="MiniQic"></span><span id="miniqic"></span><span id="MINIQIC"></span>**MiniQic** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>

<span data-ttu-id="53d87-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travado** (52)</span><span class="sxs-lookup"><span data-stu-id="53d87-236"><span id="Travan"></span><span id="travan"></span><span id="TRAVAN"></span>**Travan** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>

<span data-ttu-id="53d87-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**partícula de metal de 8mm** (53)</span><span class="sxs-lookup"><span data-stu-id="53d87-237"><span id="8mm_Metal_Particle"></span><span id="8mm_metal_particle"></span><span id="8MM_METAL_PARTICLE"></span>**8mm Metal Particle** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>

<span data-ttu-id="53d87-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**evaporação avançada de metal de 8mm** (54)</span><span class="sxs-lookup"><span data-stu-id="53d87-238"><span id="8mm_Advanced_Metal_Evaporate"></span><span id="8mm_advanced_metal_evaporate"></span><span id="8MM_ADVANCED_METAL_EVAPORATE"></span>**8mm Advanced Metal Evaporate** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NCTP"></span><span id="nctp"></span>

<span data-ttu-id="53d87-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)</span><span class="sxs-lookup"><span data-stu-id="53d87-239"><span id="NCTP"></span><span id="nctp"></span>**NCTP** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>

<span data-ttu-id="53d87-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span><span class="sxs-lookup"><span data-stu-id="53d87-240"><span id="LTO_Ultrium"></span><span id="lto_ultrium"></span><span id="LTO_ULTRIUM"></span>**LTO Ultrium** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>

<span data-ttu-id="53d87-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**LTO Accelis** (57)</span><span class="sxs-lookup"><span data-stu-id="53d87-241"><span id="LTO_Accelis"></span><span id="lto_accelis"></span><span id="LTO_ACCELIS"></span>**LTO Accelis** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>

<span data-ttu-id="53d87-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 rastrear fita** (58)</span><span class="sxs-lookup"><span data-stu-id="53d87-242"><span id="9_Track_Tape"></span><span id="9_track_tape"></span><span id="9_TRACK_TAPE"></span>**9 Track Tape** (58)</span></span>


</dt> <dd>

<span data-ttu-id="53d87-243">9-controlar fita</span><span class="sxs-lookup"><span data-stu-id="53d87-243">9-track tape</span></span>

</dd> <dt>

<span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>

<span data-ttu-id="53d87-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 trilhas de fita** (59)</span><span class="sxs-lookup"><span data-stu-id="53d87-244"><span id="18_Track_Tape"></span><span id="18_track_tape"></span><span id="18_TRACK_TAPE"></span>**18 Track Tape** (59)</span></span>


</dt> <dd>

<span data-ttu-id="53d87-245">fita de 18 trilhas</span><span class="sxs-lookup"><span data-stu-id="53d87-245">18-track tape</span></span>

</dd> <dt>

<span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>

<span data-ttu-id="53d87-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 faixa de fita** (60)</span><span class="sxs-lookup"><span data-stu-id="53d87-246"><span id="36_Track_Tape"></span><span id="36_track_tape"></span><span id="36_TRACK_TAPE"></span>**36 Track Tape** (60)</span></span>


</dt> <dd>

<span data-ttu-id="53d87-247">36-rastrear fita</span><span class="sxs-lookup"><span data-stu-id="53d87-247">36-track tape</span></span>

</dd> <dt>

<span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>

<span data-ttu-id="53d87-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span><span class="sxs-lookup"><span data-stu-id="53d87-248"><span id="Magstar_3590"></span><span id="magstar_3590"></span><span id="MAGSTAR_3590"></span>**Magstar 3590** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>

<span data-ttu-id="53d87-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**MAGSTAR MP** (62)</span><span class="sxs-lookup"><span data-stu-id="53d87-249"><span id="Magstar_MP"></span><span id="magstar_mp"></span><span id="MAGSTAR_MP"></span>**Magstar MP** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>

<span data-ttu-id="53d87-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**Fita D2** (63)</span><span class="sxs-lookup"><span data-stu-id="53d87-250"><span id="D2_Tape"></span><span id="d2_tape"></span><span id="D2_TAPE"></span>**D2 Tape** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>

<span data-ttu-id="53d87-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Fita-DST pequena** (64)</span><span class="sxs-lookup"><span data-stu-id="53d87-251"><span id="Tape_-_DST_Small"></span><span id="tape_-_dst_small"></span><span id="TAPE_-_DST_SMALL"></span>**Tape - DST Small** (64)</span></span>


</dt> <dd>

<span data-ttu-id="53d87-252">DST pequena de fita</span><span class="sxs-lookup"><span data-stu-id="53d87-252">Tape   DST small</span></span>

</dd> <dt>

<span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>

<span data-ttu-id="53d87-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Fita-DST média** (65)</span><span class="sxs-lookup"><span data-stu-id="53d87-253"><span id="Tape_-_DST_Medium"></span><span id="tape_-_dst_medium"></span><span id="TAPE_-_DST_MEDIUM"></span>**Tape - DST Medium** (65)</span></span>


</dt> <dd>

<span data-ttu-id="53d87-254">DST média de fita</span><span class="sxs-lookup"><span data-stu-id="53d87-254">Tape   DST medium</span></span>

</dd> <dt>

<span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>

<span data-ttu-id="53d87-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Fita-DST grande** (66)</span><span class="sxs-lookup"><span data-stu-id="53d87-255"><span id="Tape_-_DST_Large"></span><span id="tape_-_dst_large"></span><span id="TAPE_-_DST_LARGE"></span>**Tape - DST Large** (66)</span></span>


</dt> <dd>

<span data-ttu-id="53d87-256">DST grande em fita</span><span class="sxs-lookup"><span data-stu-id="53d87-256">Tape   DST large</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="53d87-257">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="53d87-257">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-260">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="53d87-260">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="53d87-261">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="53d87-261">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="53d87-262">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-263">**Nome**</span><span class="sxs-lookup"><span data-stu-id="53d87-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-266">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="53d87-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="53d87-267">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="53d87-267">Label by which the object is known.</span></span> <span data-ttu-id="53d87-268">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="53d87-268">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="53d87-269">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-269">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-270">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="53d87-270">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-271">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-272">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53d87-273">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="53d87-273">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="53d87-274">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="53d87-274">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="53d87-275">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="53d87-275">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="53d87-276">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-276">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-277">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="53d87-277">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-280">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="53d87-280">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53d87-281">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="53d87-281">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="53d87-282">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-283">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="53d87-283">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-284">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="53d87-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53d87-286">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="53d87-286">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="53d87-287">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-287">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-288">**Removível**</span><span class="sxs-lookup"><span data-stu-id="53d87-288">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-289">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="53d87-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53d87-291">Se for **true**, esse elemento será projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem comprometer a função do empacotamento geral.</span><span class="sxs-lookup"><span data-stu-id="53d87-291">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="53d87-292">Um pacote é considerado removível, mesmo que a energia precise ser desligada para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="53d87-292">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="53d87-293">Se a energia puder ser ativada e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="53d87-293">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="53d87-294">Por exemplo, um chip de processador não atualizável é removível.</span><span class="sxs-lookup"><span data-stu-id="53d87-294">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="53d87-295">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-295">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-296">**Peças**</span><span class="sxs-lookup"><span data-stu-id="53d87-296">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-297">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="53d87-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53d87-299">Se for **true**, é possível substituir o elemento por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="53d87-299">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="53d87-300">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="53d87-300">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="53d87-301">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="53d87-301">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="53d87-302">Todos os componentes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="53d87-302">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="53d87-303">Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-303">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-304">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="53d87-304">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-305">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-307">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="53d87-307">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="53d87-308">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="53d87-308">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="53d87-309">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-309">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-310">**SKU**</span><span class="sxs-lookup"><span data-stu-id="53d87-310">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-311">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-313">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="53d87-313">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="53d87-314">Número de unidade de manutenção de estoque do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="53d87-314">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="53d87-315">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-315">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-316">**Status**</span><span class="sxs-lookup"><span data-stu-id="53d87-316">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-319">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="53d87-319">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="53d87-320">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="53d87-320">Current status of the object.</span></span>

<span data-ttu-id="53d87-321">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="53d87-322">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="53d87-322">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="53d87-323">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="53d87-323">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="53d87-324">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="53d87-324">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="53d87-325">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="53d87-325">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="53d87-326">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="53d87-326">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="53d87-327">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="53d87-327">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="53d87-328">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="53d87-328">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="53d87-329">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="53d87-329">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="53d87-330">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="53d87-330">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="53d87-331">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="53d87-331">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="53d87-332">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="53d87-332">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="53d87-333">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="53d87-333">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="53d87-334">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="53d87-334">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="53d87-335">**Tag**</span><span class="sxs-lookup"><span data-stu-id="53d87-335">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-338">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="53d87-338">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53d87-339">Cadeia de caracteres arbitrária que identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="53d87-339">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="53d87-340">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="53d87-340">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="53d87-341">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="53d87-341">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="53d87-342">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="53d87-342">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="53d87-343">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="53d87-343">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="53d87-344">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="53d87-344">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="53d87-345">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-345">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-346">**Versão**</span><span class="sxs-lookup"><span data-stu-id="53d87-346">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-347">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="53d87-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53d87-349">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="53d87-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="53d87-350">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="53d87-350">Version of the physical element.</span></span>

<span data-ttu-id="53d87-351">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-351">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="53d87-352">**WriteProtectOn**</span><span class="sxs-lookup"><span data-stu-id="53d87-352">**WriteProtectOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53d87-353">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="53d87-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="53d87-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="53d87-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53d87-355">Se for **true**, a mídia estará protegida contra gravação por um mecanismo físico, como uma guia proteger em um disquete.</span><span class="sxs-lookup"><span data-stu-id="53d87-355">If **TRUE**, the media is currently write-protected by a physical mechanism, such as a protect tab on a floppy disk.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53d87-356">Comentários</span><span class="sxs-lookup"><span data-stu-id="53d87-356">Remarks</span></span>

<span data-ttu-id="53d87-357">A classe **CIM \_ PhysicalMedia** é derivada de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="53d87-357">The **CIM\_PhysicalMedia** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

<span data-ttu-id="53d87-358">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="53d87-358">WMI does not implement this class.</span></span>

<span data-ttu-id="53d87-359">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="53d87-359">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="53d87-360">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="53d87-360">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d87-361">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53d87-361">Requirements</span></span>



| <span data-ttu-id="53d87-362">Requisito</span><span class="sxs-lookup"><span data-stu-id="53d87-362">Requirement</span></span> | <span data-ttu-id="53d87-363">Valor</span><span class="sxs-lookup"><span data-stu-id="53d87-363">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53d87-364">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53d87-364">Minimum supported client</span></span><br/> | <span data-ttu-id="53d87-365">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53d87-365">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53d87-366">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53d87-366">Minimum supported server</span></span><br/> | <span data-ttu-id="53d87-367">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53d87-367">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53d87-368">Namespace</span><span class="sxs-lookup"><span data-stu-id="53d87-368">Namespace</span></span><br/>                | <span data-ttu-id="53d87-369">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="53d87-369">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="53d87-370">MOF</span><span class="sxs-lookup"><span data-stu-id="53d87-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53d87-371"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53d87-371"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="53d87-372">DLL</span><span class="sxs-lookup"><span data-stu-id="53d87-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53d87-373"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53d87-373"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53d87-374">Confira também</span><span class="sxs-lookup"><span data-stu-id="53d87-374">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d87-375">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="53d87-375">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> </dl>

 

