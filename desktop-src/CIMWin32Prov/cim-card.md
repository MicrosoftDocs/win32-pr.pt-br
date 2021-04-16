---
description: A \_ classe de placa CIM representa um tipo de contêiner físico que pode ser conectado a outro cartão ou placa de hospedagem, ou é uma placa de hospedagem/placa-mãe em um chassi.
ms.assetid: edbbfe43-c8e8-4cde-9507-e0a248c15ca7
ms.tgt_platform: multiple
title: Classe CIM_Card
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card
- CIM_Card.Caption
- CIM_Card.Description
- CIM_Card.InstallDate
- CIM_Card.Name
- CIM_Card.Status
- CIM_Card.CreationClassName
- CIM_Card.Manufacturer
- CIM_Card.Model
- CIM_Card.OtherIdentifyingInfo
- CIM_Card.PartNumber
- CIM_Card.PoweredOn
- CIM_Card.SerialNumber
- CIM_Card.SKU
- CIM_Card.Tag
- CIM_Card.Version
- CIM_Card.Depth
- CIM_Card.Height
- CIM_Card.HotSwappable
- CIM_Card.Removable
- CIM_Card.Replaceable
- CIM_Card.Weight
- CIM_Card.Width
- CIM_Card.HostingBoard
- CIM_Card.RequirementsDescription
- CIM_Card.RequiresDaughterBoard
- CIM_Card.SlotLayout
- CIM_Card.SpecialRequirements
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b10478e5d0e34020f64d8775e857d9fa6af94d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753590"
---
# <a name="cim_card-class"></a><span data-ttu-id="da6f4-103">\_Classe de placa CIM</span><span class="sxs-lookup"><span data-stu-id="da6f4-103">CIM\_Card class</span></span>

<span data-ttu-id="da6f4-104">A classe de **\_ placa CIM** representa um tipo de contêiner físico que pode ser conectado a outro cartão ou placa de hospedagem, ou é uma placa de hospedagem/placa-mãe em um chassi.</span><span class="sxs-lookup"><span data-stu-id="da6f4-104">The **CIM\_Card** class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="da6f4-105">Essa classe inclui qualquer pacote que seja capaz de carregar sinais e fornecer um ponto de montagem para componentes físicos, como chips ou outros pacotes físicos, como outros cartões.</span><span class="sxs-lookup"><span data-stu-id="da6f4-105">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da6f4-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="da6f4-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="da6f4-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="da6f4-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="da6f4-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="da6f4-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="da6f4-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="da6f4-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="da6f4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da6f4-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B76-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Card : CIM_PhysicalPackage
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
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  HostingBoard;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SlotLayout;
  boolean  SpecialRequirements;
};
```

## <a name="members"></a><span data-ttu-id="da6f4-111">Membros</span><span class="sxs-lookup"><span data-stu-id="da6f4-111">Members</span></span>

<span data-ttu-id="da6f4-112">A classe de **\_ placa CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="da6f4-112">The **CIM\_Card** class has these types of members:</span></span>

-   [<span data-ttu-id="da6f4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="da6f4-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="da6f4-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da6f4-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="da6f4-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="da6f4-115">Methods</span></span>

<span data-ttu-id="da6f4-116">A classe de **\_ placa CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="da6f4-116">The **CIM\_Card** class has these methods.</span></span>



| <span data-ttu-id="da6f4-117">Método</span><span class="sxs-lookup"><span data-stu-id="da6f4-117">Method</span></span>                                                        | <span data-ttu-id="da6f4-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="da6f4-118">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da6f4-119">**Iscompatível**</span><span class="sxs-lookup"><span data-stu-id="da6f4-119">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-card.md) | <span data-ttu-id="da6f4-120">Verifica se o elemento físico referenciado pode estar contido ou inserido no pacote físico.</span><span class="sxs-lookup"><span data-stu-id="da6f4-120">Verifies whether the referenced physical element may be contained by or inserted into the physical package.</span></span> <span data-ttu-id="da6f4-121">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="da6f4-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="da6f4-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da6f4-122">Properties</span></span>

<span data-ttu-id="da6f4-123">A classe de **\_ placa CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="da6f4-123">The **CIM\_Card** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da6f4-124">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="da6f4-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-127">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="da6f4-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-128">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="da6f4-128">A short textual description of the object.</span></span>

<span data-ttu-id="da6f4-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="da6f4-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-133">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="da6f4-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-134">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="da6f4-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="da6f4-135">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="da6f4-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="da6f4-136">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-136">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-137">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="da6f4-137">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-138">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="da6f4-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-140">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="da6f4-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-141">Profundidade do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="da6f4-141">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="da6f4-142">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-142">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-143">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="da6f4-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-146">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="da6f4-146">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-147">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="da6f4-147">A textual description of the object.</span></span>

<span data-ttu-id="da6f4-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-149">**Altura**</span><span class="sxs-lookup"><span data-stu-id="da6f4-149">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-150">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="da6f4-150">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-152">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="da6f4-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-153">Altura do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="da6f4-153">Height of the physical package, in inches.</span></span>

<span data-ttu-id="da6f4-154">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-154">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-155">**HostingBoard**</span><span class="sxs-lookup"><span data-stu-id="da6f4-155">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-156">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="da6f4-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-158">Se for **true**, esse cartão será uma placa-mãe ou, mais genericamente, uma placa-base em um chassi.</span><span class="sxs-lookup"><span data-stu-id="da6f4-158">If **TRUE**, this card is a motherboard or, more generically, a baseboard in a chassis.</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-159">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="da6f4-159">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-160">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="da6f4-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-162">Se **for true**, o pacote poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="da6f4-162">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="da6f4-163">Um pacote físico pode ser intercambiável se o elemento puder ser substituído por um fisicamente diferente (mas equivalente) um enquanto o pacote que o contém está ativado.</span><span class="sxs-lookup"><span data-stu-id="da6f4-163">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="da6f4-164">Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="da6f4-164">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="da6f4-165">Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="da6f4-165">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="da6f4-166">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-166">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-167">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="da6f4-167">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-168">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="da6f4-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-170">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="da6f4-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-171">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="da6f4-171">Indicates when the object was installed.</span></span> <span data-ttu-id="da6f4-172">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="da6f4-172">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="da6f4-173">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-174">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="da6f4-174">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-177">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="da6f4-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-178">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="da6f4-178">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="da6f4-179">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-179">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="da6f4-180">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-180">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-181">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="da6f4-181">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-184">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="da6f4-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-185">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="da6f4-185">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="da6f4-186">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-186">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-187">**Nome**</span><span class="sxs-lookup"><span data-stu-id="da6f4-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-190">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="da6f4-190">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-191">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="da6f4-191">Label by which the object is known.</span></span> <span data-ttu-id="da6f4-192">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="da6f4-192">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="da6f4-193">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-194">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="da6f4-194">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-197">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="da6f4-197">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="da6f4-198">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="da6f4-198">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="da6f4-199">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="da6f4-199">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="da6f4-200">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-200">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-201">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="da6f4-201">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-204">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="da6f4-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-205">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="da6f4-205">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="da6f4-206">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-207">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="da6f4-207">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-208">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="da6f4-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-210">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="da6f4-210">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="da6f4-211">Caso contrário, ele estará desativado no momento.</span><span class="sxs-lookup"><span data-stu-id="da6f4-211">Otherwise, it is currently off.</span></span>

<span data-ttu-id="da6f4-212">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-213">**Removível**</span><span class="sxs-lookup"><span data-stu-id="da6f4-213">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-214">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="da6f4-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-216">Se for **true**, o pacote será projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem comprometer a função do empacotamento geral.</span><span class="sxs-lookup"><span data-stu-id="da6f4-216">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="da6f4-217">Um pacote é considerado removível, mesmo que a energia precise ser desligada para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="da6f4-217">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="da6f4-218">Se a energia puder ser ativada e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="da6f4-218">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="da6f4-219">Por exemplo, um chip de processador atualizável é removível.</span><span class="sxs-lookup"><span data-stu-id="da6f4-219">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="da6f4-220">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-220">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-221">**Peças**</span><span class="sxs-lookup"><span data-stu-id="da6f4-221">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-222">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="da6f4-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-224">Se for **true**, é possível substituir o elemento por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="da6f4-224">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="da6f4-225">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="da6f4-225">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="da6f4-226">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="da6f4-226">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="da6f4-227">Todos os componentes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="da6f4-227">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="da6f4-228">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-228">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-229">**RequirementsDescription**</span><span class="sxs-lookup"><span data-stu-id="da6f4-229">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-232">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ placa CIM**.**SpecialRequirements**")</span><span class="sxs-lookup"><span data-stu-id="da6f4-232">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-233">Cadeia de caracteres de forma livre que descreve as maneiras em que o cartão é fisicamente exclusivo de outros cartões.</span><span class="sxs-lookup"><span data-stu-id="da6f4-233">Free-form string that describes the ways in which the card is physically unique from other cards.</span></span> <span data-ttu-id="da6f4-234">Essa propriedade só tem significado quando a propriedade booliana correspondente, **SpecialRequirements**, é definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="da6f4-234">This property only has meaning when the corresponding Boolean property, **SpecialRequirements**, is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-235">**RequiresDaughterBoard**</span><span class="sxs-lookup"><span data-stu-id="da6f4-235">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-236">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="da6f4-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-238">Se for **true**, para funcionar corretamente, pelo menos um cartão daughterboard ou auxiliar será necessário.</span><span class="sxs-lookup"><span data-stu-id="da6f4-238">If **TRUE**, to function properly, at least one daughterboard or auxiliary card is required.</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-239">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="da6f4-239">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-242">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="da6f4-242">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-243">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="da6f4-243">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="da6f4-244">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-244">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-245">**SKU**</span><span class="sxs-lookup"><span data-stu-id="da6f4-245">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-247">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-248">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="da6f4-248">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-249">Número de unidade de manutenção de estoque para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="da6f4-249">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="da6f4-250">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-250">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-251">**SlotLayout**</span><span class="sxs-lookup"><span data-stu-id="da6f4-251">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-254">Cadeia de caracteres de forma livre que descreve o posicionamento do slot, o uso típico, as restrições, os espaçamentos de slot individuais ou outras informações pertinentes para os slots em um cartão.</span><span class="sxs-lookup"><span data-stu-id="da6f4-254">Free-form string that describes the slot positioning, typical usage, restrictions, individual slot spacings, or other pertinent information for the slots on a card.</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-255">**SpecialRequirements**</span><span class="sxs-lookup"><span data-stu-id="da6f4-255">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-256">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="da6f4-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-258">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ placa CIM**.**RequirementsDescription**")</span><span class="sxs-lookup"><span data-stu-id="da6f4-258">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Card**.**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-259">Se for **true**, o cartão será fisicamente exclusivo de outros cartões do mesmo tipo e, portanto, exigirá um slot especial.</span><span class="sxs-lookup"><span data-stu-id="da6f4-259">If **TRUE**, the card is physically unique from other cards of the same type and, therefore, requires a special slot.</span></span> <span data-ttu-id="da6f4-260">Por exemplo, um cartão de largura dupla requer dois slots.</span><span class="sxs-lookup"><span data-stu-id="da6f4-260">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="da6f4-261">Outro exemplo é quando um determinado cartão pode ser usado para a mesma função geral que outros cartões, mas requer um slot especial (extra longo, por exemplo); enquanto outros cartões podem ser colocados em qualquer slot disponível.</span><span class="sxs-lookup"><span data-stu-id="da6f4-261">Another example is when a certain card can be used for the same general function as other cards, but requires a special slot (extra long, for example); whereas, other cards can be placed in any available slot.</span></span> <span data-ttu-id="da6f4-262">Se **for true**, a propriedade **RequirementsDescription** correspondente deverá especificar a natureza da exclusividade ou da finalidade do cartão.</span><span class="sxs-lookup"><span data-stu-id="da6f4-262">If **TRUE**, the corresponding **RequirementsDescription** property should specify the nature of the uniqueness or purpose of the card.</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-263">**Status**</span><span class="sxs-lookup"><span data-stu-id="da6f4-263">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-266">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="da6f4-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-267">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="da6f4-267">String that indicates the current status of the object.</span></span> <span data-ttu-id="da6f4-268">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="da6f4-268">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="da6f4-269">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="da6f4-269">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="da6f4-270">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="da6f4-270">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="da6f4-271">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="da6f4-271">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="da6f4-272">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="da6f4-272">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="da6f4-273">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="da6f4-273">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="da6f4-274">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-274">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="da6f4-275">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="da6f4-275">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="da6f4-276">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="da6f4-276">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="da6f4-277">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="da6f4-277">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="da6f4-278">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="da6f4-278">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="da6f4-279">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="da6f4-279">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="da6f4-280">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="da6f4-280">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="da6f4-281">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="da6f4-281">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="da6f4-282">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="da6f4-282">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="da6f4-283">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="da6f4-283">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="da6f4-284">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="da6f4-284">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="da6f4-285">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="da6f4-285">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="da6f4-286">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="da6f4-286">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="da6f4-287">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="da6f4-287">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="da6f4-288">**Tag**</span><span class="sxs-lookup"><span data-stu-id="da6f4-288">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-291">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="da6f4-291">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-292">Identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="da6f4-292">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="da6f4-293">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="da6f4-293">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="da6f4-294">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="da6f4-294">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="da6f4-295">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="da6f4-295">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="da6f4-296">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="da6f4-296">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="da6f4-297">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="da6f4-297">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="da6f4-298">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-299">**Versão**</span><span class="sxs-lookup"><span data-stu-id="da6f4-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da6f4-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-302">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="da6f4-302">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-303">Indica a versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="da6f4-303">Indicates the version of the physical element.</span></span>

<span data-ttu-id="da6f4-304">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-304">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-305">**Weight**</span><span class="sxs-lookup"><span data-stu-id="da6f4-305">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-306">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="da6f4-306">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-308">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="da6f4-308">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-309">Peso do pacote físico, em libras.</span><span class="sxs-lookup"><span data-stu-id="da6f4-309">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="da6f4-310">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-310">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="da6f4-311">**Largura**</span><span class="sxs-lookup"><span data-stu-id="da6f4-311">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da6f4-312">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="da6f4-312">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da6f4-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da6f4-314">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="da6f4-314">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="da6f4-315">Largura do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="da6f4-315">Width of the physical package, in inches.</span></span>

<span data-ttu-id="da6f4-316">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-316">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da6f4-317">Comentários</span><span class="sxs-lookup"><span data-stu-id="da6f4-317">Remarks</span></span>

<span data-ttu-id="da6f4-318">A classe de **\_ placa CIM** é derivada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-318">The **CIM\_Card** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

<span data-ttu-id="da6f4-319">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="da6f4-319">WMI does not implement this class.</span></span> <span data-ttu-id="da6f4-320">Para obter mais informações sobre classes derivadas **do \_ cartão CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="da6f4-320">For more information about classes derived from **CIM\_Card**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="da6f4-321">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="da6f4-321">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="da6f4-322">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="da6f4-322">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="da6f4-323">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da6f4-323">Requirements</span></span>



| <span data-ttu-id="da6f4-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="da6f4-324">Requirement</span></span> | <span data-ttu-id="da6f4-325">Valor</span><span class="sxs-lookup"><span data-stu-id="da6f4-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da6f4-326">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da6f4-326">Minimum supported client</span></span><br/> | <span data-ttu-id="da6f4-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da6f4-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da6f4-328">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da6f4-328">Minimum supported server</span></span><br/> | <span data-ttu-id="da6f4-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da6f4-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da6f4-330">Namespace</span><span class="sxs-lookup"><span data-stu-id="da6f4-330">Namespace</span></span><br/>                | <span data-ttu-id="da6f4-331">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="da6f4-331">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da6f4-332">MOF</span><span class="sxs-lookup"><span data-stu-id="da6f4-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da6f4-333"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da6f4-333"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da6f4-334">DLL</span><span class="sxs-lookup"><span data-stu-id="da6f4-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da6f4-335"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da6f4-335"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da6f4-336">Confira também</span><span class="sxs-lookup"><span data-stu-id="da6f4-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da6f4-337">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="da6f4-337">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

