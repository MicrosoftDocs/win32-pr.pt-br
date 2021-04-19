---
description: A \_ classe CIM PhysicalPackage representa os elementos físicos que contêm ou hospedam outros componentes. Os exemplos são um compartimento de rack ou uma placa de adaptador.
ms.assetid: 9182d413-aa7e-4c2f-94fe-12e99980520c
ms.tgt_platform: multiple
title: Classe CIM_PhysicalPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage
- CIM_PhysicalPackage.Caption
- CIM_PhysicalPackage.CreationClassName
- CIM_PhysicalPackage.Depth
- CIM_PhysicalPackage.Description
- CIM_PhysicalPackage.Height
- CIM_PhysicalPackage.HotSwappable
- CIM_PhysicalPackage.InstallDate
- CIM_PhysicalPackage.Manufacturer
- CIM_PhysicalPackage.Model
- CIM_PhysicalPackage.Name
- CIM_PhysicalPackage.OtherIdentifyingInfo
- CIM_PhysicalPackage.PartNumber
- CIM_PhysicalPackage.PoweredOn
- CIM_PhysicalPackage.Removable
- CIM_PhysicalPackage.Replaceable
- CIM_PhysicalPackage.SerialNumber
- CIM_PhysicalPackage.SKU
- CIM_PhysicalPackage.Status
- CIM_PhysicalPackage.Tag
- CIM_PhysicalPackage.Version
- CIM_PhysicalPackage.Weight
- CIM_PhysicalPackage.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1905467fd949e2c18d8be9e7a7bfff39ad8d1477
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748268"
---
# <a name="cim_physicalpackage-class"></a><span data-ttu-id="b5278-104">\_Classe CIM PhysicalPackage</span><span class="sxs-lookup"><span data-stu-id="b5278-104">CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="b5278-105">A classe **CIM \_ PhysicalPackage** representa os elementos físicos que contêm ou hospedam outros componentes.</span><span class="sxs-lookup"><span data-stu-id="b5278-105">The **CIM\_PhysicalPackage** class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="b5278-106">Os exemplos são um compartimento de rack ou uma placa de adaptador.</span><span class="sxs-lookup"><span data-stu-id="b5278-106">Examples are a rack enclosure or an adapter card.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5278-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b5278-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b5278-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b5278-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b5278-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b5278-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b5278-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b5278-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5278-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5278-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B6E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalPackage : CIM_PhysicalElement
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
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
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="b5278-112">Membros</span><span class="sxs-lookup"><span data-stu-id="b5278-112">Members</span></span>

<span data-ttu-id="b5278-113">A classe **CIM \_ PhysicalPackage** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b5278-113">The **CIM\_PhysicalPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="b5278-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b5278-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b5278-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b5278-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b5278-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="b5278-116">Methods</span></span>

<span data-ttu-id="b5278-117">A classe **CIM \_ PhysicalPackage** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b5278-117">The **CIM\_PhysicalPackage** class has these methods.</span></span>



| <span data-ttu-id="b5278-118">Método</span><span class="sxs-lookup"><span data-stu-id="b5278-118">Method</span></span>                                                                   | <span data-ttu-id="b5278-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5278-119">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5278-120">**Iscompatível**</span><span class="sxs-lookup"><span data-stu-id="b5278-120">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md) | <span data-ttu-id="b5278-121">Verifica se o elemento físico referenciado pode ser contido ou inserido no pacote físico.</span><span class="sxs-lookup"><span data-stu-id="b5278-121">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="b5278-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="b5278-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b5278-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b5278-123">Properties</span></span>

<span data-ttu-id="b5278-124">A classe **CIM \_ PhysicalPackage** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b5278-124">The **CIM\_PhysicalPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5278-125">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b5278-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-128">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b5278-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b5278-129">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b5278-129">Short textual description of the object.</span></span>

<span data-ttu-id="b5278-130">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b5278-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-134">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b5278-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b5278-135">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="b5278-135">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b5278-136">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="b5278-136">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b5278-137">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-138">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="b5278-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-139">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="b5278-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-141">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="b5278-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b5278-142">Profundidade do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="b5278-142">Depth of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="b5278-143">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b5278-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-146">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="b5278-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b5278-147">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b5278-147">Textual description of the object.</span></span>

<span data-ttu-id="b5278-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-149">**Altura**</span><span class="sxs-lookup"><span data-stu-id="b5278-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-150">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="b5278-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-152">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="b5278-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b5278-153">Altura do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="b5278-153">Height of the physical package, in inches.</span></span>

</dd> <dt>

<span data-ttu-id="b5278-154">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="b5278-154">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-155">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5278-155">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5278-157">Se **for true**, o pacote poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="b5278-157">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="b5278-158">Um pacote físico pode ser intercambiável se o elemento puder ser substituído por um fisicamente diferente (mas equivalente) um enquanto o pacote que o contém está ativado.</span><span class="sxs-lookup"><span data-stu-id="b5278-158">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="b5278-159">Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="b5278-159">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="b5278-160">Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="b5278-160">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="b5278-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b5278-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-162">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b5278-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-164">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="b5278-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b5278-165">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b5278-165">Date and time the object was installed.</span></span> <span data-ttu-id="b5278-166">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b5278-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b5278-167">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-168">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="b5278-168">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-171">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b5278-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b5278-172">Nome da organização que produziu o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b5278-172">Name of the organization that produced the physical element.</span></span> <span data-ttu-id="b5278-173">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-173">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="b5278-174">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-175">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="b5278-175">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-178">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b5278-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b5278-179">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="b5278-179">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="b5278-180">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-181">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b5278-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-184">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b5278-184">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b5278-185">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b5278-185">Label by which the object is known.</span></span> <span data-ttu-id="b5278-186">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="b5278-186">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b5278-187">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-188">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b5278-188">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5278-191">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b5278-191">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="b5278-192">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="b5278-192">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="b5278-193">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="b5278-193">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="b5278-194">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-195">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="b5278-195">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-198">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b5278-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b5278-199">Número de peça atribuído pela organização que produziu ou fabricou o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b5278-199">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="b5278-200">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-201">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="b5278-201">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-202">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5278-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5278-204">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="b5278-204">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="b5278-205">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-205">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-206">**Removível**</span><span class="sxs-lookup"><span data-stu-id="b5278-206">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-207">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5278-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5278-209">Se for **true**, o pacote será projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem comprometer a função do empacotamento geral.</span><span class="sxs-lookup"><span data-stu-id="b5278-209">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="b5278-210">Um pacote é considerado removível, mesmo que a energia precise ser desligada para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="b5278-210">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="b5278-211">Se a energia puder ser ativada e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="b5278-211">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="b5278-212">Por exemplo, um chip de processador atualizável é removível.</span><span class="sxs-lookup"><span data-stu-id="b5278-212">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="b5278-213">**Peças**</span><span class="sxs-lookup"><span data-stu-id="b5278-213">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-214">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b5278-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5278-216">Se for **true**, é possível substituir o elemento por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="b5278-216">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="b5278-217">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="b5278-217">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="b5278-218">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="b5278-218">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="b5278-219">Todos os componentes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="b5278-219">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="b5278-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b5278-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-223">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b5278-223">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b5278-224">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b5278-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="b5278-225">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="b5278-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-229">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b5278-229">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b5278-230">Número de unidade de manutenção de estoque do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b5278-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="b5278-231">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-232">**Status**</span><span class="sxs-lookup"><span data-stu-id="b5278-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-233">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-235">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b5278-235">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b5278-236">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b5278-236">Current status of the object.</span></span>

<span data-ttu-id="b5278-237">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b5278-238">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b5278-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b5278-239">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b5278-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b5278-240">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="b5278-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b5278-241">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b5278-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b5278-242">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b5278-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b5278-243">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b5278-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b5278-244">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="b5278-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b5278-245">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="b5278-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b5278-246">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="b5278-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b5278-247">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="b5278-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b5278-248">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b5278-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b5278-249">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="b5278-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b5278-250">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="b5278-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b5278-251">**Tag**</span><span class="sxs-lookup"><span data-stu-id="b5278-251">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-254">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b5278-254">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b5278-255">Cadeia de caracteres arbitrária que identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="b5278-255">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="b5278-256">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="b5278-256">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="b5278-257">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b5278-257">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="b5278-258">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="b5278-258">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="b5278-259">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="b5278-259">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="b5278-260">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="b5278-260">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="b5278-261">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-262">**Versão**</span><span class="sxs-lookup"><span data-stu-id="b5278-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-263">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b5278-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-264">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-265">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b5278-265">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b5278-266">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b5278-266">Version of the physical element.</span></span>

<span data-ttu-id="b5278-267">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-267">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5278-268">**Weight**</span><span class="sxs-lookup"><span data-stu-id="b5278-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-269">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="b5278-269">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-271">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="b5278-271">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="b5278-272">Peso do pacote físico, em libras.</span><span class="sxs-lookup"><span data-stu-id="b5278-272">Weight of the physical package, in pounds.</span></span>

</dd> <dt>

<span data-ttu-id="b5278-273">**Largura**</span><span class="sxs-lookup"><span data-stu-id="b5278-273">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5278-274">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="b5278-274">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b5278-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b5278-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5278-276">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="b5278-276">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b5278-277">Largura do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="b5278-277">Width of the physical package, in inches.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5278-278">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5278-278">Remarks</span></span>

<span data-ttu-id="b5278-279">A classe **CIM \_ PhysicalPackage** é derivada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-279">The **CIM\_PhysicalPackage** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="b5278-280">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b5278-280">WMI does not implement this class.</span></span> <span data-ttu-id="b5278-281">Para classes WMI que são derivadas do **CIM \_ PhysicalPackage**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-281">For WMI classes that are derived from **CIM\_PhysicalPackage**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b5278-282">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b5278-282">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b5278-283">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b5278-283">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5278-284">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5278-284">Requirements</span></span>



| <span data-ttu-id="b5278-285">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5278-285">Requirement</span></span> | <span data-ttu-id="b5278-286">Valor</span><span class="sxs-lookup"><span data-stu-id="b5278-286">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5278-287">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5278-287">Minimum supported client</span></span><br/> | <span data-ttu-id="b5278-288">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5278-288">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5278-289">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5278-289">Minimum supported server</span></span><br/> | <span data-ttu-id="b5278-290">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5278-290">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5278-291">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5278-291">Namespace</span></span><br/>                | <span data-ttu-id="b5278-292">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b5278-292">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5278-293">MOF</span><span class="sxs-lookup"><span data-stu-id="b5278-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5278-294"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5278-294"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5278-295">DLL</span><span class="sxs-lookup"><span data-stu-id="b5278-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5278-296"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5278-296"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5278-297">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5278-297">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5278-298">**Físico do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b5278-298">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

