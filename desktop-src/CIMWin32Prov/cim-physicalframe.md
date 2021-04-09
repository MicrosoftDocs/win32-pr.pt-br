---
description: A \_ classe CIM PhysicalFrame é uma classe pai de rack, chassi e outros compartimentos de quadro, pois são definidos em classes de extensão.
ms.assetid: 571c8ca2-1644-4060-8d89-d9625a591f86
ms.tgt_platform: multiple
title: Classe CIM_PhysicalFrame
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame
- CIM_PhysicalFrame.AudibleAlarm
- CIM_PhysicalFrame.BreachDescription
- CIM_PhysicalFrame.CableManagementStrategy
- CIM_PhysicalFrame.Caption
- CIM_PhysicalFrame.CreationClassName
- CIM_PhysicalFrame.Depth
- CIM_PhysicalFrame.Description
- CIM_PhysicalFrame.Height
- CIM_PhysicalFrame.HotSwappable
- CIM_PhysicalFrame.InstallDate
- CIM_PhysicalFrame.LockPresent
- CIM_PhysicalFrame.Manufacturer
- CIM_PhysicalFrame.Model
- CIM_PhysicalFrame.Name
- CIM_PhysicalFrame.OtherIdentifyingInfo
- CIM_PhysicalFrame.PartNumber
- CIM_PhysicalFrame.PoweredOn
- CIM_PhysicalFrame.Removable
- CIM_PhysicalFrame.Replaceable
- CIM_PhysicalFrame.SecurityBreach
- CIM_PhysicalFrame.SerialNumber
- CIM_PhysicalFrame.ServiceDescriptions
- CIM_PhysicalFrame.ServicePhilosophy
- CIM_PhysicalFrame.SKU
- CIM_PhysicalFrame.Status
- CIM_PhysicalFrame.Tag
- CIM_PhysicalFrame.Version
- CIM_PhysicalFrame.VisibleAlarm
- CIM_PhysicalFrame.Weight
- CIM_PhysicalFrame.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b445c928412bc475a3269ba59be48395b254efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089487"
---
# <a name="cim_physicalframe-class"></a><span data-ttu-id="c1145-103">\_Classe CIM PhysicalFrame</span><span class="sxs-lookup"><span data-stu-id="c1145-103">CIM\_PhysicalFrame class</span></span>

<span data-ttu-id="c1145-104">A classe **CIM \_ PhysicalFrame** é uma classe pai de rack, chassi e outros compartimentos de quadro, pois são definidos em classes de extensão.</span><span class="sxs-lookup"><span data-stu-id="c1145-104">The **CIM\_PhysicalFrame** class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="c1145-105">Propriedades como **VisibleAlarm** e **AudibleAlarm** e dados relacionados a violações de segurança são incluídos nessa classe pai.</span><span class="sxs-lookup"><span data-stu-id="c1145-105">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c1145-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c1145-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c1145-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c1145-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c1145-108">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c1145-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c1145-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c1145-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1145-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1145-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B70-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalFrame : CIM_PhysicalPackage
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="c1145-111">Membros</span><span class="sxs-lookup"><span data-stu-id="c1145-111">Members</span></span>

<span data-ttu-id="c1145-112">A classe **CIM \_ PhysicalFrame** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c1145-112">The **CIM\_PhysicalFrame** class has these types of members:</span></span>

-   [<span data-ttu-id="c1145-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1145-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="c1145-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1145-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c1145-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1145-115">Methods</span></span>

<span data-ttu-id="c1145-116">A classe **CIM \_ PhysicalFrame** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c1145-116">The **CIM\_PhysicalFrame** class has these methods.</span></span>



| <span data-ttu-id="c1145-117">Método</span><span class="sxs-lookup"><span data-stu-id="c1145-117">Method</span></span>                                                                 | <span data-ttu-id="c1145-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1145-118">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1145-119">**Iscompatível**</span><span class="sxs-lookup"><span data-stu-id="c1145-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalframe.md) | <span data-ttu-id="c1145-120">Verifica se o elemento físico referenciado pode ser contido ou inserido no pacote físico.</span><span class="sxs-lookup"><span data-stu-id="c1145-120">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="c1145-121">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="c1145-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c1145-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1145-122">Properties</span></span>

<span data-ttu-id="c1145-123">A classe **CIM \_ PhysicalFrame** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c1145-123">The **CIM\_PhysicalFrame** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1145-124">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="c1145-124">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-125">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1145-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1145-127">Se for **true**, o quadro será equipado com um alarme audível.</span><span class="sxs-lookup"><span data-stu-id="c1145-127">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="c1145-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="c1145-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-131">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="c1145-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-132">Cadeia de caracteres de forma livre que fornece mais informações se a propriedade **SecurityBreach** indicar que ocorreu uma violação ou algum outro evento relacionado à segurança.</span><span class="sxs-lookup"><span data-stu-id="c1145-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c1145-133">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="c1145-133">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1145-136">Cadeia de caracteres de forma livre que contém informações sobre como os vários cabos são conectados e agrupados para o quadro.</span><span class="sxs-lookup"><span data-stu-id="c1145-136">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="c1145-137">Com muitos cabos de rede, relacionados ao armazenamento e de energia, o gerenciamento de cabos pode ser um esforço complexo e desafiador.</span><span class="sxs-lookup"><span data-stu-id="c1145-137">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="c1145-138">Essa propriedade de cadeia de caracteres contém informações para auxiliar no assembly e no serviço do quadro.</span><span class="sxs-lookup"><span data-stu-id="c1145-138">This string property contains information to aid in assembly and service of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="c1145-139">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c1145-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-142">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c1145-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-143">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c1145-143">Short textual description of the object.</span></span>

<span data-ttu-id="c1145-144">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c1145-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-148">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c1145-148">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c1145-149">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="c1145-149">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c1145-150">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="c1145-150">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c1145-151">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-151">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-152">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="c1145-152">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-153">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="c1145-153">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-155">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="c1145-155">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-156">Profundidade do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="c1145-156">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="c1145-157">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-157">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-158">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c1145-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-161">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="c1145-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-162">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c1145-162">Textual description of the object.</span></span>

<span data-ttu-id="c1145-163">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-164">**Altura**</span><span class="sxs-lookup"><span data-stu-id="c1145-164">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-165">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="c1145-165">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-167">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="c1145-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-168">Altura do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="c1145-168">Height of the physical package, in inches.</span></span>

<span data-ttu-id="c1145-169">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-169">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-170">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="c1145-170">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-171">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1145-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1145-173">Se **for true**, o pacote poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="c1145-173">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="c1145-174">Um pacote físico pode ser intercambiável se o elemento puder ser substituído por um fisicamente diferente (mas equivalente) um enquanto o pacote que o contém está ativado.</span><span class="sxs-lookup"><span data-stu-id="c1145-174">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="c1145-175">Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="c1145-175">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="c1145-176">Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="c1145-176">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="c1145-177">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-177">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-178">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c1145-178">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-179">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c1145-179">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-181">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="c1145-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-182">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="c1145-182">Date and time the object was installed.</span></span> <span data-ttu-id="c1145-183">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c1145-183">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c1145-184">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-185">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="c1145-185">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-186">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1145-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1145-188">Se for **true**, o quadro será protegido com um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c1145-188">If **TRUE**, the frame is protected with a lock.</span></span>

</dd> <dt>

<span data-ttu-id="c1145-189">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="c1145-189">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-192">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c1145-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c1145-193">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c1145-193">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="c1145-194">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-194">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="c1145-195">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-195">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-196">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="c1145-196">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-199">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c1145-199">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c1145-200">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="c1145-200">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="c1145-201">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-202">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c1145-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-205">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c1145-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-206">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="c1145-206">Label by which the object is known.</span></span> <span data-ttu-id="c1145-207">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="c1145-207">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c1145-208">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-209">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c1145-209">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1145-212">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c1145-212">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="c1145-213">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="c1145-213">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="c1145-214">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="c1145-214">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="c1145-215">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-216">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="c1145-216">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-219">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c1145-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c1145-220">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c1145-220">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="c1145-221">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-221">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-222">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="c1145-222">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-223">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1145-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1145-225">Se **for true**, o elemento físico será ligado; caso contrário, ele estará desativado no momento.</span><span class="sxs-lookup"><span data-stu-id="c1145-225">If **TRUE**, the physical element is powered on; otherwise, it is currently off.</span></span>

<span data-ttu-id="c1145-226">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-226">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-227">**Removível**</span><span class="sxs-lookup"><span data-stu-id="c1145-227">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-228">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1145-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1145-230">Se for **true**, esse elemento será projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem comprometer a função do empacotamento geral.</span><span class="sxs-lookup"><span data-stu-id="c1145-230">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="c1145-231">Um pacote é considerado removível, mesmo que a energia precise ser desligada para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="c1145-231">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="c1145-232">Se a energia puder ser ativada e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="c1145-232">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="c1145-233">Por exemplo, um chip de processador atualizável é removível.</span><span class="sxs-lookup"><span data-stu-id="c1145-233">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="c1145-234">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-234">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-235">**Peças**</span><span class="sxs-lookup"><span data-stu-id="c1145-235">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-236">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1145-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1145-238">Se for **true**, é possível substituir o elemento por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="c1145-238">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="c1145-239">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="c1145-239">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="c1145-240">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="c1145-240">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="c1145-241">Todos os componentes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="c1145-241">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="c1145-242">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-242">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-243">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="c1145-243">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-244">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1145-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-246">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Tabela global de contêiner físico DMTF \| 2,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ PhysicalFrame**.**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="c1145-246">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-247">Indica se uma violação física do quadro foi tentada, mas malsucedida, ou se foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c1145-247">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c1145-248">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c1145-248">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c1145-249">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c1145-249">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="c1145-250">**Sem violação** (3)</span><span class="sxs-lookup"><span data-stu-id="c1145-250">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="c1145-251">**Tentativa de violação** (4)</span><span class="sxs-lookup"><span data-stu-id="c1145-251">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="c1145-252">**Violação bem-sucedida** (5)</span><span class="sxs-lookup"><span data-stu-id="c1145-252">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c1145-253">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="c1145-253">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-254">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-256">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c1145-256">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c1145-257">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c1145-257">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="c1145-258">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-258">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-259">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c1145-259">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-260">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c1145-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-262">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM PhysicalFrame**.**Infilosofia**")</span><span class="sxs-lookup"><span data-stu-id="c1145-262">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-263">Cadeias de caracteres de forma livre que fornecem explicações detalhadas para entradas na matriz de **unifilosofia** .</span><span class="sxs-lookup"><span data-stu-id="c1145-263">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="c1145-264">Cada entrada dessa matriz está relacionada à entrada na matriz de **unifilosofia** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="c1145-264">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="c1145-265">**Infilosofia**</span><span class="sxs-lookup"><span data-stu-id="c1145-265">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-266">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1145-266">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c1145-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-268">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM PhysicalFrame**.**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="c1145-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_PhysicalFrame**.**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-269">Indica se o quadro é atendido de cima, para frente, para trás ou para o lado; e se ele tem bandejas deslizantes ou lados removíveis e se o quadro é móvel (por exemplo, com cilindros).</span><span class="sxs-lookup"><span data-stu-id="c1145-269">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c1145-270">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c1145-270">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c1145-271">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c1145-271">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="c1145-272">**Serviço da parte superior** (2)</span><span class="sxs-lookup"><span data-stu-id="c1145-272">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="c1145-273">**Serviço da frente** (3)</span><span class="sxs-lookup"><span data-stu-id="c1145-273">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="c1145-274">**Serviço de volta** (4)</span><span class="sxs-lookup"><span data-stu-id="c1145-274">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="c1145-275">**Serviço do lado** (5)</span><span class="sxs-lookup"><span data-stu-id="c1145-275">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="c1145-276">**Bandejas deslizantes** (6)</span><span class="sxs-lookup"><span data-stu-id="c1145-276">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="c1145-277">**Lados removíveis** (7)</span><span class="sxs-lookup"><span data-stu-id="c1145-277">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="c1145-278">**Móvel** (8)</span><span class="sxs-lookup"><span data-stu-id="c1145-278">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c1145-279">**SKU**</span><span class="sxs-lookup"><span data-stu-id="c1145-279">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-280">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-282">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c1145-282">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c1145-283">Número de unidade de manutenção de estoque do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c1145-283">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="c1145-284">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-284">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-285">**Status**</span><span class="sxs-lookup"><span data-stu-id="c1145-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-288">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c1145-288">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-289">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c1145-289">Current status of the object.</span></span>

<span data-ttu-id="c1145-290">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c1145-291">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c1145-291">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c1145-292">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c1145-292">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c1145-293">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="c1145-293">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c1145-294">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c1145-294">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c1145-295">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c1145-295">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c1145-296">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c1145-296">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c1145-297">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c1145-297">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c1145-298">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="c1145-298">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c1145-299">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="c1145-299">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c1145-300">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="c1145-300">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c1145-301">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c1145-301">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c1145-302">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="c1145-302">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c1145-303">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="c1145-303">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c1145-304">**Tag**</span><span class="sxs-lookup"><span data-stu-id="c1145-304">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-305">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-307">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c1145-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c1145-308">Cadeia de caracteres arbitrária que identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="c1145-308">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="c1145-309">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="c1145-309">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="c1145-310">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware/entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c1145-310">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="c1145-311">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="c1145-311">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="c1145-312">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="c1145-312">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="c1145-313">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="c1145-313">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="c1145-314">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-315">**Versão**</span><span class="sxs-lookup"><span data-stu-id="c1145-315">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1145-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-318">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c1145-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c1145-319">Cadeia de caracteres que indica a versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="c1145-319">String that indicates the version of the physical element.</span></span>

<span data-ttu-id="c1145-320">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-321">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="c1145-321">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-322">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c1145-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1145-324">Se **for true**, o equipamento incluirá um alarme visível.</span><span class="sxs-lookup"><span data-stu-id="c1145-324">If **TRUE**, the equipment includes a visible alarm.</span></span>

</dd> <dt>

<span data-ttu-id="c1145-325">**Weight**</span><span class="sxs-lookup"><span data-stu-id="c1145-325">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-326">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="c1145-326">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-328">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="c1145-328">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-329">Peso do pacote físico, em libras.</span><span class="sxs-lookup"><span data-stu-id="c1145-329">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="c1145-330">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-330">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1145-331">**Largura**</span><span class="sxs-lookup"><span data-stu-id="c1145-331">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1145-332">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="c1145-332">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="c1145-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1145-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1145-334">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="c1145-334">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="c1145-335">Largura do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="c1145-335">Width of the physical package, in inches.</span></span>

<span data-ttu-id="c1145-336">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-336">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1145-337">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1145-337">Remarks</span></span>

<span data-ttu-id="c1145-338">A classe **CIM \_ PhysicalFrame** é derivada de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-338">The **CIM\_PhysicalFrame** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="c1145-339">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="c1145-339">WMI does not implement this class.</span></span> <span data-ttu-id="c1145-340">Para classes WMI derivadas do **CIM \_ PhysicalFrame**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c1145-340">For WMI classes derived from **CIM\_PhysicalFrame**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c1145-341">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c1145-341">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c1145-342">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c1145-342">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1145-343">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1145-343">Requirements</span></span>



| <span data-ttu-id="c1145-344">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1145-344">Requirement</span></span> | <span data-ttu-id="c1145-345">Valor</span><span class="sxs-lookup"><span data-stu-id="c1145-345">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1145-346">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1145-346">Minimum supported client</span></span><br/> | <span data-ttu-id="c1145-347">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1145-347">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1145-348">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1145-348">Minimum supported server</span></span><br/> | <span data-ttu-id="c1145-349">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1145-349">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1145-350">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1145-350">Namespace</span></span><br/>                | <span data-ttu-id="c1145-351">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c1145-351">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c1145-352">MOF</span><span class="sxs-lookup"><span data-stu-id="c1145-352">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1145-353"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1145-353"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1145-354">DLL</span><span class="sxs-lookup"><span data-stu-id="c1145-354">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1145-355"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1145-355"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1145-356">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1145-356">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1145-357">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="c1145-357">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

