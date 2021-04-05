---
description: A \_ classe de rack CIM representa um rack (um quadro físico ou compartimento) no qual os chassis são armazenados. Normalmente, um rack representa o compartimento; todos os componentes em funcionamento são empacotados no chassi.
ms.assetid: 1e0273ce-2a09-4f75-a82e-d0555d6a831e
ms.tgt_platform: multiple
title: Classe CIM_Rack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack
- CIM_Rack.AudibleAlarm
- CIM_Rack.BreachDescription
- CIM_Rack.CableManagementStrategy
- CIM_Rack.Caption
- CIM_Rack.CountryDesignation
- CIM_Rack.CreationClassName
- CIM_Rack.Depth
- CIM_Rack.Description
- CIM_Rack.Height
- CIM_Rack.HotSwappable
- CIM_Rack.InstallDate
- CIM_Rack.LockPresent
- CIM_Rack.Manufacturer
- CIM_Rack.Model
- CIM_Rack.Name
- CIM_Rack.OtherIdentifyingInfo
- CIM_Rack.PartNumber
- CIM_Rack.PoweredOn
- CIM_Rack.Removable
- CIM_Rack.Replaceable
- CIM_Rack.SecurityBreach
- CIM_Rack.SerialNumber
- CIM_Rack.ServiceDescriptions
- CIM_Rack.ServicePhilosophy
- CIM_Rack.SKU
- CIM_Rack.Status
- CIM_Rack.Tag
- CIM_Rack.TypeOfRack
- CIM_Rack.Version
- CIM_Rack.VisibleAlarm
- CIM_Rack.Weight
- CIM_Rack.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2eb5234e8dd65d7df86acec7ab121ef961c2121
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646333"
---
# <a name="cim_rack-class"></a><span data-ttu-id="f363b-104">\_Classe de rack CIM</span><span class="sxs-lookup"><span data-stu-id="f363b-104">CIM\_Rack class</span></span>

<span data-ttu-id="f363b-105">A classe de **\_ rack CIM** representa um rack (um quadro físico ou compartimento) no qual os chassis são armazenados.</span><span class="sxs-lookup"><span data-stu-id="f363b-105">The **CIM\_Rack** class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="f363b-106">Normalmente, um rack representa o compartimento; todos os componentes em funcionamento são empacotados no chassi.</span><span class="sxs-lookup"><span data-stu-id="f363b-106">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f363b-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f363b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f363b-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f363b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f363b-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f363b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f363b-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="f363b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f363b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f363b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B71-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Rack : CIM_PhysicalFrame
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CountryDesignation;
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
  uint16   TypeOfRack;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="f363b-112">Membros</span><span class="sxs-lookup"><span data-stu-id="f363b-112">Members</span></span>

<span data-ttu-id="f363b-113">A classe de **\_ rack CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f363b-113">The **CIM\_Rack** class has these types of members:</span></span>

-   [<span data-ttu-id="f363b-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="f363b-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="f363b-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f363b-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f363b-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="f363b-116">Methods</span></span>

<span data-ttu-id="f363b-117">A classe de **\_ rack CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f363b-117">The **CIM\_Rack** class has these methods.</span></span>



| <span data-ttu-id="f363b-118">Método</span><span class="sxs-lookup"><span data-stu-id="f363b-118">Method</span></span>                                                        | <span data-ttu-id="f363b-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="f363b-119">Description</span></span>                                                                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f363b-120">**Iscompatível**</span><span class="sxs-lookup"><span data-stu-id="f363b-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-rack.md) | <span data-ttu-id="f363b-121">Verifica se o elemento físico referenciado pode ser contido ou inserido no pacote físico.</span><span class="sxs-lookup"><span data-stu-id="f363b-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="f363b-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="f363b-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f363b-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f363b-123">Properties</span></span>

<span data-ttu-id="f363b-124">A classe de **\_ rack CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f363b-124">The **CIM\_Rack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f363b-125">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="f363b-125">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-126">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f363b-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f363b-128">Se for **true**, o quadro será equipado com um alarme audível.</span><span class="sxs-lookup"><span data-stu-id="f363b-128">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="f363b-129">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-129">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-130">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="f363b-130">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-133">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="f363b-133">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-134">Cadeia de caracteres de forma livre que fornecerá informações se a propriedade **SecurityBreach** indicar que ocorreu uma violação ou algum outro evento relacionado à segurança.</span><span class="sxs-lookup"><span data-stu-id="f363b-134">Free-form string that provides information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="f363b-135">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-135">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-136">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="f363b-136">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f363b-139">Cadeia de caracteres de forma livre que contém informações sobre como os vários cabos são conectados e agrupados para o quadro.</span><span class="sxs-lookup"><span data-stu-id="f363b-139">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="f363b-140">Com muitos cabos de rede, relacionados ao armazenamento e de energia, o gerenciamento de cabos pode ser um esforço complexo e desafiador.</span><span class="sxs-lookup"><span data-stu-id="f363b-140">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="f363b-141">Essa propriedade de cadeia de caracteres contém informações para auxiliar no assembly e no serviço do quadro.</span><span class="sxs-lookup"><span data-stu-id="f363b-141">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="f363b-142">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-142">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-143">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="f363b-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-146">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f363b-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-147">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f363b-147">Short textual description of the object.</span></span>

<span data-ttu-id="f363b-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-149">**CountryDesignation**</span><span class="sxs-lookup"><span data-stu-id="f363b-149">**CountryDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-152">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ rack CIM**.**TypeOfRack**")</span><span class="sxs-lookup"><span data-stu-id="f363b-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**TypeOfRack**")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-153">País ou região para o qual o rack foi projetado.</span><span class="sxs-lookup"><span data-stu-id="f363b-153">Country or region for which the rack is designed.</span></span> <span data-ttu-id="f363b-154">As cadeias de caracteres de código de país ou região são definidas por ISO/IEC 3166.</span><span class="sxs-lookup"><span data-stu-id="f363b-154">Country or region code strings are as defined by ISO/IEC 3166.</span></span> <span data-ttu-id="f363b-155">O tipo de rack é especificado na propriedade **TypeOfRack** .</span><span class="sxs-lookup"><span data-stu-id="f363b-155">The rack type is specified in the **TypeOfRack** property.</span></span>

</dd> <dt>

<span data-ttu-id="f363b-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f363b-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-159">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f363b-159">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f363b-160">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="f363b-160">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f363b-161">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="f363b-161">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f363b-162">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-162">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-163">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="f363b-163">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-164">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="f363b-164">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-166">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="f363b-166">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-167">Profundidade do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="f363b-167">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="f363b-168">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-169">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f363b-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-172">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="f363b-172">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-173">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f363b-173">Textual description of the object.</span></span>

<span data-ttu-id="f363b-174">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-175">**Altura**</span><span class="sxs-lookup"><span data-stu-id="f363b-175">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-176">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="f363b-176">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-178">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("altura"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("EUA")</span><span class="sxs-lookup"><span data-stu-id="f363b-178">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Height"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-179">Altura do pacote físico, usando a unidade de medida "U".</span><span class="sxs-lookup"><span data-stu-id="f363b-179">Height of the physical package, using the "U" unit of measure.</span></span> <span data-ttu-id="f363b-180">Um "U" é uma unidade de medida padrão para a altura de um rack, ou componente montável em rack, e é igual a 1,75 polegadas ou 4,445 centímetros.</span><span class="sxs-lookup"><span data-stu-id="f363b-180">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

<span data-ttu-id="f363b-181">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-181">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-182">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="f363b-182">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-183">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f363b-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f363b-185">Se **for true**, o pacote poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="f363b-185">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="f363b-186">Um pacote físico pode ser intercambiável se o elemento puder ser substituído por um fisicamente diferente (mas equivalente) um enquanto o pacote que o contém está ativado.</span><span class="sxs-lookup"><span data-stu-id="f363b-186">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="f363b-187">Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="f363b-187">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="f363b-188">Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="f363b-188">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="f363b-189">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-189">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-190">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f363b-190">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-191">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f363b-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-193">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="f363b-193">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-194">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="f363b-194">Date and time the object was installed.</span></span> <span data-ttu-id="f363b-195">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="f363b-195">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f363b-196">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-197">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="f363b-197">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-198">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f363b-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f363b-200">Se for **true**, o quadro será protegido com um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="f363b-200">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="f363b-201">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-201">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-202">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="f363b-202">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-205">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f363b-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f363b-206">Nome da organização que produziu o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f363b-206">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="f363b-207">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-207">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="f363b-208">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-208">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-209">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="f363b-209">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-212">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f363b-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f363b-213">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="f363b-213">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="f363b-214">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-214">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-215">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f363b-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-218">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f363b-218">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-219">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="f363b-219">Label by which the object is known.</span></span> <span data-ttu-id="f363b-220">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="f363b-220">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f363b-221">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-222">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f363b-222">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f363b-225">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f363b-225">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="f363b-226">Um exemplo são dados de código de barras associados a um elemento que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="f363b-226">One example is bar-code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="f363b-227">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-227">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="f363b-228">Se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será NULL e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="f363b-228">If only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="f363b-229">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="f363b-229">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-232">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f363b-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f363b-233">Número de peça atribuído pela organização que produziu ou fabricou o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f363b-233">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="f363b-234">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-234">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-235">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="f363b-235">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-236">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f363b-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f363b-238">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="f363b-238">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="f363b-239">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-239">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-240">**Removível**</span><span class="sxs-lookup"><span data-stu-id="f363b-240">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-241">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f363b-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f363b-243">Se for **true**, esse elemento será projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem comprometer a função do empacotamento geral.</span><span class="sxs-lookup"><span data-stu-id="f363b-243">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="f363b-244">Um pacote é considerado removível, mesmo que a energia deva ser "desativada" para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="f363b-244">A package is considered removable even if the power must be "off" to perform the removal.</span></span> <span data-ttu-id="f363b-245">Se a potência puder ser "ativada" e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="f363b-245">If the power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="f363b-246">Por exemplo, uma bateria extra em um laptop é removível, assim como um pacote de drive de disco inserido usando conectores SCA; no entanto, o último pode ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="f363b-246">For example, an extra battery in a laptop is removable, as is a disk-drive package inserted using SCA connectors; however, the latter can be hot-swapped.</span></span> <span data-ttu-id="f363b-247">A tela de um laptop não é removível, nem uma fonte de alimentação não redundante.</span><span class="sxs-lookup"><span data-stu-id="f363b-247">A laptop's display is not removable, nor is a non-redundant power supply.</span></span> <span data-ttu-id="f363b-248">A remoção desses componentes afeta a função do empacotamento geral ou é impossível devido à forte integração do pacote.</span><span class="sxs-lookup"><span data-stu-id="f363b-248">Removing these components impacts the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="f363b-249">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-249">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-250">**Peças**</span><span class="sxs-lookup"><span data-stu-id="f363b-250">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-251">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f363b-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f363b-253">Se for **true**, é possível substituir o elemento por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="f363b-253">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="f363b-254">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="f363b-254">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="f363b-255">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="f363b-255">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="f363b-256">Todos os componentes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="f363b-256">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="f363b-257">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-257">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-258">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="f363b-258">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-259">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f363b-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-261">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Tabela global de contêiner físico DMTF \| 2,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="f363b-261">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-262">Indica se uma violação física do quadro foi tentada, mas malsucedida, ou se foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f363b-262">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span> <span data-ttu-id="f363b-263">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-263">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f363b-264">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="f363b-264">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f363b-265">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="f363b-265">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="f363b-266">**Sem violação** (3)</span><span class="sxs-lookup"><span data-stu-id="f363b-266">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="f363b-267">**Tentativa de violação** (4)</span><span class="sxs-lookup"><span data-stu-id="f363b-267">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="f363b-268">**Violação bem-sucedida** (5)</span><span class="sxs-lookup"><span data-stu-id="f363b-268">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f363b-269">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="f363b-269">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-270">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-272">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f363b-272">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f363b-273">Número alocado pelo fabricante usado para identificar o rack.</span><span class="sxs-lookup"><span data-stu-id="f363b-273">Manufacturer-allocated number used to identify the rack.</span></span>

<span data-ttu-id="f363b-274">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-274">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-275">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f363b-275">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-276">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-276">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f363b-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-278">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM PhysicalFrame**](cim-physicalframe.md).**Infilosofia**")</span><span class="sxs-lookup"><span data-stu-id="f363b-278">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-279">Cadeias de caracteres de forma livre que fornecem explicações detalhadas para entradas na matriz de **unifilosofia** .</span><span class="sxs-lookup"><span data-stu-id="f363b-279">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="f363b-280">Observe que cada entrada da matriz está relacionada à entrada em **perfilosofia** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="f363b-280">Note, each entry of the array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="f363b-281">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-281">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-282">**Infilosofia**</span><span class="sxs-lookup"><span data-stu-id="f363b-282">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-283">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f363b-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f363b-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-285">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="f363b-285">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-286">Indica se o quadro é atendido de cima, para frente, para trás ou para o lado; e se ele tem bandejas deslizantes ou lados removíveis e se o quadro é móvel (por exemplo, com cilindros).</span><span class="sxs-lookup"><span data-stu-id="f363b-286">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="f363b-287">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-287">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f363b-288">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="f363b-288">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f363b-289">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="f363b-289">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="f363b-290">**Serviço da parte superior** (2)</span><span class="sxs-lookup"><span data-stu-id="f363b-290">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="f363b-291">**Serviço da frente** (3)</span><span class="sxs-lookup"><span data-stu-id="f363b-291">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="f363b-292">**Serviço de volta** (4)</span><span class="sxs-lookup"><span data-stu-id="f363b-292">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="f363b-293">**Serviço do lado** (5)</span><span class="sxs-lookup"><span data-stu-id="f363b-293">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="f363b-294">**Bandejas deslizantes** (6)</span><span class="sxs-lookup"><span data-stu-id="f363b-294">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="f363b-295">**Lados removíveis** (7)</span><span class="sxs-lookup"><span data-stu-id="f363b-295">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="f363b-296">**Móvel** (8)</span><span class="sxs-lookup"><span data-stu-id="f363b-296">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f363b-297">**SKU**</span><span class="sxs-lookup"><span data-stu-id="f363b-297">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-300">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f363b-300">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f363b-301">Número de unidade de manutenção de estoque do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f363b-301">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="f363b-302">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-303">**Status**</span><span class="sxs-lookup"><span data-stu-id="f363b-303">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-306">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f363b-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-307">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f363b-307">Current status of the object.</span></span> <span data-ttu-id="f363b-308">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f363b-309">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f363b-309">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f363b-310">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f363b-310">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f363b-311">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="f363b-311">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f363b-312">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f363b-312">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f363b-313">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="f363b-313">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f363b-314">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f363b-314">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f363b-315">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="f363b-315">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f363b-316">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="f363b-316">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f363b-317">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="f363b-317">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f363b-318">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="f363b-318">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f363b-319">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f363b-319">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f363b-320">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="f363b-320">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f363b-321">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="f363b-321">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f363b-322">**Tag**</span><span class="sxs-lookup"><span data-stu-id="f363b-322">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-323">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-325">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f363b-325">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f363b-326">Cadeia de caracteres arbitrária que identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="f363b-326">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="f363b-327">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="f363b-327">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="f363b-328">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="f363b-328">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="f363b-329">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="f363b-329">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="f363b-330">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="f363b-330">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="f363b-331">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="f363b-331">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="f363b-332">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-332">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-333">**TypeOfRack**</span><span class="sxs-lookup"><span data-stu-id="f363b-333">**TypeOfRack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-334">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f363b-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-336">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ rack CIM**.**CountryDesignation**")</span><span class="sxs-lookup"><span data-stu-id="f363b-336">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Rack**.**CountryDesignation**")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-337">Tipo de rack.</span><span class="sxs-lookup"><span data-stu-id="f363b-337">Type of rack.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f363b-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="f363b-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>

<span data-ttu-id="f363b-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Padrão 19 polegadas** (1)</span><span class="sxs-lookup"><span data-stu-id="f363b-339"><span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Standard 19 Inch** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f363b-340">Padrão de 19 polegadas</span><span class="sxs-lookup"><span data-stu-id="f363b-340">Standard 19-inch</span></span>

</dd> <dt>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>

<span data-ttu-id="f363b-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span><span class="sxs-lookup"><span data-stu-id="f363b-341"><span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>

<span data-ttu-id="f363b-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Prateleira de equipamento** (3)</span><span class="sxs-lookup"><span data-stu-id="f363b-342"><span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Equipment Shelf** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>

<span data-ttu-id="f363b-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Não padrão** (4)</span><span class="sxs-lookup"><span data-stu-id="f363b-343"><span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Non-Standard** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f363b-344">**Versão**</span><span class="sxs-lookup"><span data-stu-id="f363b-344">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f363b-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-347">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f363b-347">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f363b-348">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="f363b-348">Version of the physical element.</span></span>

<span data-ttu-id="f363b-349">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-349">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-350">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="f363b-350">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-351">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f363b-351">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f363b-353">Se **for true**, o equipamento incluirá um alarme visível.</span><span class="sxs-lookup"><span data-stu-id="f363b-353">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="f363b-354">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-354">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-355">**Weight**</span><span class="sxs-lookup"><span data-stu-id="f363b-355">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-356">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="f363b-356">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-358">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="f363b-358">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-359">Peso do pacote físico, em libras.</span><span class="sxs-lookup"><span data-stu-id="f363b-359">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="f363b-360">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-360">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="f363b-361">**Largura**</span><span class="sxs-lookup"><span data-stu-id="f363b-361">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f363b-362">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="f363b-362">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="f363b-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f363b-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f363b-364">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="f363b-364">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="f363b-365">Largura do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="f363b-365">Width of the physical package, in inches.</span></span>

<span data-ttu-id="f363b-366">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-366">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f363b-367">Comentários</span><span class="sxs-lookup"><span data-stu-id="f363b-367">Remarks</span></span>

<span data-ttu-id="f363b-368">A classe de **\_ rack CIM** é derivada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="f363b-368">The **CIM\_Rack** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="f363b-369">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="f363b-369">WMI does not implement this class.</span></span>

<span data-ttu-id="f363b-370">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="f363b-370">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f363b-371">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="f363b-371">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f363b-372">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f363b-372">Requirements</span></span>



| <span data-ttu-id="f363b-373">Requisito</span><span class="sxs-lookup"><span data-stu-id="f363b-373">Requirement</span></span> | <span data-ttu-id="f363b-374">Valor</span><span class="sxs-lookup"><span data-stu-id="f363b-374">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f363b-375">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f363b-375">Minimum supported client</span></span><br/> | <span data-ttu-id="f363b-376">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f363b-376">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f363b-377">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f363b-377">Minimum supported server</span></span><br/> | <span data-ttu-id="f363b-378">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f363b-378">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f363b-379">Namespace</span><span class="sxs-lookup"><span data-stu-id="f363b-379">Namespace</span></span><br/>                | <span data-ttu-id="f363b-380">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f363b-380">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f363b-381">MOF</span><span class="sxs-lookup"><span data-stu-id="f363b-381">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f363b-382"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f363b-382"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f363b-383">DLL</span><span class="sxs-lookup"><span data-stu-id="f363b-383">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f363b-384"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f363b-384"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f363b-385">Confira também</span><span class="sxs-lookup"><span data-stu-id="f363b-385">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f363b-386">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="f363b-386">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

