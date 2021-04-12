---
description: A \_ classe CIM PhysicalComponent representa um componente básico ou de baixo nível em um pacote. Um elemento físico que não é um link, um conector ou um pacote é um descendente (ou membro) dessa classe.
ms.assetid: 079874cd-5717-4662-a192-0ced16270bbd
ms.tgt_platform: multiple
title: Classe CIM_PhysicalComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalComponent
- CIM_PhysicalComponent.Caption
- CIM_PhysicalComponent.Description
- CIM_PhysicalComponent.InstallDate
- CIM_PhysicalComponent.Name
- CIM_PhysicalComponent.Status
- CIM_PhysicalComponent.CreationClassName
- CIM_PhysicalComponent.Manufacturer
- CIM_PhysicalComponent.Model
- CIM_PhysicalComponent.OtherIdentifyingInfo
- CIM_PhysicalComponent.PartNumber
- CIM_PhysicalComponent.PoweredOn
- CIM_PhysicalComponent.SerialNumber
- CIM_PhysicalComponent.SKU
- CIM_PhysicalComponent.Tag
- CIM_PhysicalComponent.Version
- CIM_PhysicalComponent.HotSwappable
- CIM_PhysicalComponent.Removable
- CIM_PhysicalComponent.Replaceable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e7e1db2c1d314b2d45816801643912dcf3b31bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457075"
---
# <a name="cim_physicalcomponent-class"></a><span data-ttu-id="2c5c7-104">\_Classe CIM PhysicalComponent</span><span class="sxs-lookup"><span data-stu-id="2c5c7-104">CIM\_PhysicalComponent class</span></span>

<span data-ttu-id="2c5c7-105">A classe **CIM \_ PhysicalComponent** representa um componente básico ou de baixo nível em um pacote.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-105">The **CIM\_PhysicalComponent** class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="2c5c7-106">Um elemento físico que não é um link, um conector ou um pacote é um descendente (ou membro) dessa classe.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-106">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span> <span data-ttu-id="2c5c7-107">Por exemplo, o chipset UART em uma placa de modem interno seria uma subclasse (se propriedades ou associações adicionais forem definidas) ou uma instância de **\_ PhysicalComponent CIM**.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-107">For example, the UART chipset on an internal modem card would be a subclass (if additional properties or associations are defined) or an instance of **CIM\_PhysicalComponent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c5c7-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2c5c7-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2c5c7-110">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2c5c7-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c5c7-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c5c7-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B78-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalComponent : CIM_PhysicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="2c5c7-113">Membros</span><span class="sxs-lookup"><span data-stu-id="2c5c7-113">Members</span></span>

<span data-ttu-id="2c5c7-114">A classe **CIM \_ PhysicalComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2c5c7-114">The **CIM\_PhysicalComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="2c5c7-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2c5c7-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c5c7-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2c5c7-116">Properties</span></span>

<span data-ttu-id="2c5c7-117">A classe **CIM \_ PhysicalComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-117">The **CIM\_PhysicalComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c5c7-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-122">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-122">A short textual description of the object.</span></span>

<span data-ttu-id="2c5c7-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-127">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2c5c7-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-128">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2c5c7-129">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2c5c7-130">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-134">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-135">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-135">A textual description of the object.</span></span>

<span data-ttu-id="2c5c7-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-137">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-137">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-138">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-140">Se **for true**, o pacote poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-140">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="2c5c7-141">Um pacote físico pode ser intercambiável se o elemento puder ser substituído por um fisicamente diferente (mas equivalente) um enquanto o pacote que o contém está ativado.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-141">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="2c5c7-142">Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-142">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="2c5c7-143">Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-143">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-145">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-147">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-148">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-148">Indicates when the object was installed.</span></span> <span data-ttu-id="2c5c7-149">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2c5c7-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-151">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-151">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-154">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2c5c7-154">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-155">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-155">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="2c5c7-156">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-156">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="2c5c7-157">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-157">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-158">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-158">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-161">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2c5c7-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-162">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-162">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="2c5c7-163">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-163">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-164">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-167">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-167">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-168">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-168">Label by which the object is known.</span></span> <span data-ttu-id="2c5c7-169">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-169">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2c5c7-170">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-171">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-171">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-174">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-174">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="2c5c7-175">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-175">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="2c5c7-176">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="2c5c7-176">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="2c5c7-177">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-177">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-178">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-178">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-181">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2c5c7-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-182">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-182">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="2c5c7-183">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-183">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-184">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-184">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-185">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-187">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-187">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="2c5c7-188">Caso contrário, ele estará desativado no momento.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-188">Otherwise, it is currently off.</span></span>

<span data-ttu-id="2c5c7-189">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-189">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-190">**Removível**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-190">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-191">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-193">Se for **true**, esse elemento será projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem comprometer a função do empacotamento geral.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-193">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="2c5c7-194">Um pacote é considerado removível, mesmo que a energia precise ser desligada para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-194">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="2c5c7-195">Se a energia puder ser ativada e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-195">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="2c5c7-196">Por exemplo, um chip de processador atualizável é removível.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-196">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-197">**Peças**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-197">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-198">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-200">Se for **true**, é possível substituir o elemento por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-200">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="2c5c7-201">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-201">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="2c5c7-202">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-202">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="2c5c7-203">Todos os componentes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-203">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-204">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-204">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-205">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-207">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2c5c7-207">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-208">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-208">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="2c5c7-209">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-209">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-210">**SKU**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-210">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-211">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-213">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2c5c7-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-214">Número de unidade de manutenção de estoque para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-214">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="2c5c7-215">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-216">**Status**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-216">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-219">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-220">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-220">String that indicates the current status of the object.</span></span> <span data-ttu-id="2c5c7-221">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-221">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2c5c7-222">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="2c5c7-222">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2c5c7-223">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-223">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2c5c7-224">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="2c5c7-224">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2c5c7-225">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-225">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2c5c7-226">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-226">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2c5c7-227">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2c5c7-228">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2c5c7-228">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2c5c7-229">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-229">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2c5c7-230">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-230">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2c5c7-231">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-231">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c5c7-232">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-232">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2c5c7-233">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-233">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2c5c7-234">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-234">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2c5c7-235">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-235">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2c5c7-236">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-236">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2c5c7-237">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-237">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2c5c7-238">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-238">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2c5c7-239">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-239">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2c5c7-240">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="2c5c7-240">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c5c7-241">**Tag**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-241">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-244">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2c5c7-244">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-245">Identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-245">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="2c5c7-246">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-246">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="2c5c7-247">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-247">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="2c5c7-248">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-248">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="2c5c7-249">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-249">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="2c5c7-250">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-250">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="2c5c7-251">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-251">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c5c7-252">**Versão**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-252">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c5c7-253">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c5c7-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c5c7-255">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2c5c7-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2c5c7-256">Indica a versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-256">Indicates the version of the physical element.</span></span>

<span data-ttu-id="2c5c7-257">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c5c7-258">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c5c7-258">Remarks</span></span>

<span data-ttu-id="2c5c7-259">A classe **CIM \_ PhysicalComponent** é derivada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-259">The **CIM\_PhysicalComponent** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="2c5c7-260">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-260">WMI does not implement this class.</span></span> <span data-ttu-id="2c5c7-261">Para classes WMI derivadas do **CIM \_ PhysicalComponent**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2c5c7-261">For WMI classes derived from **CIM\_PhysicalComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2c5c7-262">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-262">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2c5c7-263">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-263">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c5c7-264">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c5c7-264">Requirements</span></span>



| <span data-ttu-id="2c5c7-265">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c5c7-265">Requirement</span></span> | <span data-ttu-id="2c5c7-266">Valor</span><span class="sxs-lookup"><span data-stu-id="2c5c7-266">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c5c7-267">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c5c7-267">Minimum supported client</span></span><br/> | <span data-ttu-id="2c5c7-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c5c7-268">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c5c7-269">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c5c7-269">Minimum supported server</span></span><br/> | <span data-ttu-id="2c5c7-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c5c7-270">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c5c7-271">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c5c7-271">Namespace</span></span><br/>                | <span data-ttu-id="2c5c7-272">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2c5c7-272">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c5c7-273">MOF</span><span class="sxs-lookup"><span data-stu-id="2c5c7-273">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c5c7-274"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c5c7-274"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c5c7-275">DLL</span><span class="sxs-lookup"><span data-stu-id="2c5c7-275">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c5c7-276"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c5c7-276"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c5c7-277">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c5c7-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c5c7-278">**Físico do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2c5c7-278">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

