---
description: As \_ subclasses do CIM PhysicalElement definem qualquer componente de um sistema que tenha uma identidade física distinta. As instâncias dessa classe podem ser definidas em termos de rótulos que podem ser fisicamente anexados ao objeto.
ms.assetid: 7ba6d1a9-f449-4ae2-a37c-517245bea39e
ms.tgt_platform: multiple
title: Classe CIM_PhysicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElement
- CIM_PhysicalElement.Caption
- CIM_PhysicalElement.Description
- CIM_PhysicalElement.InstallDate
- CIM_PhysicalElement.Name
- CIM_PhysicalElement.Status
- CIM_PhysicalElement.CreationClassName
- CIM_PhysicalElement.Manufacturer
- CIM_PhysicalElement.Model
- CIM_PhysicalElement.OtherIdentifyingInfo
- CIM_PhysicalElement.PartNumber
- CIM_PhysicalElement.PoweredOn
- CIM_PhysicalElement.SerialNumber
- CIM_PhysicalElement.SKU
- CIM_PhysicalElement.Tag
- CIM_PhysicalElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5afeda74789bc492aac3d37629b64385b8734f60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500817"
---
# <a name="cim_physicalelement-class"></a><span data-ttu-id="35756-104">Classe do CIM \_ físicoelement</span><span class="sxs-lookup"><span data-stu-id="35756-104">CIM\_PhysicalElement class</span></span>

<span data-ttu-id="35756-105">As subclasses do **CIM \_ PhysicalElement** definem qualquer componente de um sistema que tenha uma identidade física distinta.</span><span class="sxs-lookup"><span data-stu-id="35756-105">The **CIM\_PhysicalElement** subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="35756-106">As instâncias dessa classe podem ser definidas em termos de rótulos que podem ser fisicamente anexados ao objeto.</span><span class="sxs-lookup"><span data-stu-id="35756-106">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span> <span data-ttu-id="35756-107">Todos os processos, arquivos e dispositivos lógicos não são considerados elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="35756-107">All processes, files, and logical devices are not considered to be physical elements.</span></span> <span data-ttu-id="35756-108">Por exemplo, não é possível anexar um rótulo a um modem; Só é possível anexar um rótulo ao cartão que implementa o modem.</span><span class="sxs-lookup"><span data-stu-id="35756-108">For example, it is not possible to attach a label to a modem; it is only possible to attach a label to the card that implements the modem.</span></span> <span data-ttu-id="35756-109">O mesmo cartão também poderia implementar um adaptador de LAN.</span><span class="sxs-lookup"><span data-stu-id="35756-109">The same card could also implement a LAN adapter.</span></span>

<span data-ttu-id="35756-110">Elementos de sistema gerenciados tangíveis (geralmente itens de hardware) têm uma manifestação física.</span><span class="sxs-lookup"><span data-stu-id="35756-110">Tangible managed system elements (usually hardware items) have a physical manifestation.</span></span> <span data-ttu-id="35756-111">Um elemento de sistema gerenciado não é necessariamente um componente discreto.</span><span class="sxs-lookup"><span data-stu-id="35756-111">A managed system element is not necessarily a discrete component.</span></span> <span data-ttu-id="35756-112">Por exemplo, é possível que um único cartão (um tipo de elemento físico) hospede mais de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="35756-112">For example, it is possible for a single card (a type of physical element) to host more than one logical device.</span></span> <span data-ttu-id="35756-113">O cartão seria representado por um único elemento físico associado a vários dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="35756-113">The card would be represented by a single physical element associated with multiple logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35756-114">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="35756-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="35756-115">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="35756-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="35756-116">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="35756-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="35756-117">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="35756-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="35756-118">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35756-118">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B61-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElement : CIM_ManagedSystemElement
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
};
```

## <a name="members"></a><span data-ttu-id="35756-119">Membros</span><span class="sxs-lookup"><span data-stu-id="35756-119">Members</span></span>

<span data-ttu-id="35756-120">A classe do **CIM \_ físicoelement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="35756-120">The **CIM\_PhysicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="35756-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="35756-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35756-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="35756-122">Properties</span></span>

<span data-ttu-id="35756-123">A classe do **CIM \_ físicoelement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="35756-123">The **CIM\_PhysicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35756-124">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="35756-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-127">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="35756-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="35756-128">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="35756-128">A short textual description of the object.</span></span>

<span data-ttu-id="35756-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35756-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35756-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="35756-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-133">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="35756-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="35756-134">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="35756-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="35756-135">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="35756-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="35756-136">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="35756-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-139">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="35756-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="35756-140">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="35756-140">A textual description of the object.</span></span>

<span data-ttu-id="35756-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35756-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35756-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="35756-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-143">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="35756-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35756-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-145">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="35756-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="35756-146">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="35756-146">Indicates when the object was installed.</span></span> <span data-ttu-id="35756-147">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="35756-147">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="35756-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35756-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35756-149">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="35756-149">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-152">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="35756-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="35756-153">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="35756-153">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="35756-154">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="35756-154">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="35756-155">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="35756-155">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-158">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="35756-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="35756-159">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="35756-159">Name by which the physical element is generally known.</span></span>

</dd> <dt>

<span data-ttu-id="35756-160">**Nome**</span><span class="sxs-lookup"><span data-stu-id="35756-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-163">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="35756-163">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="35756-164">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="35756-164">Label by which the object is known.</span></span> <span data-ttu-id="35756-165">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="35756-165">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="35756-166">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35756-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35756-167">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="35756-167">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35756-170">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="35756-170">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="35756-171">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="35756-171">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="35756-172">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="35756-172">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

</dd> <dt>

<span data-ttu-id="35756-173">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="35756-173">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-176">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="35756-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="35756-177">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="35756-177">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="35756-178">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="35756-178">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-179">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="35756-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35756-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35756-181">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="35756-181">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="35756-182">Caso contrário, ele estará desativado no momento.</span><span class="sxs-lookup"><span data-stu-id="35756-182">Otherwise, it is currently off.</span></span>

</dd> <dt>

<span data-ttu-id="35756-183">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="35756-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-186">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="35756-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="35756-187">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="35756-187">Manufacturer-allocated number used to identify the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="35756-188">**SKU**</span><span class="sxs-lookup"><span data-stu-id="35756-188">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-191">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="35756-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="35756-192">Número de unidade de manutenção de estoque para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="35756-192">Stock-keeping unit number for this physical element.</span></span>

</dd> <dt>

<span data-ttu-id="35756-193">**Status**</span><span class="sxs-lookup"><span data-stu-id="35756-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-196">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="35756-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="35756-197">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="35756-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="35756-198">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="35756-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="35756-199">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="35756-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="35756-200">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="35756-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="35756-201">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="35756-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="35756-202">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="35756-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="35756-203">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="35756-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="35756-204">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35756-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="35756-205">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="35756-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="35756-206">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="35756-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="35756-207">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="35756-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="35756-208">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="35756-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="35756-209">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="35756-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="35756-210">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="35756-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="35756-211">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="35756-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="35756-212">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="35756-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="35756-213">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="35756-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="35756-214">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="35756-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="35756-215">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="35756-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="35756-216">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="35756-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="35756-217">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="35756-217">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="35756-218">**Tag**</span><span class="sxs-lookup"><span data-stu-id="35756-218">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-221">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="35756-221">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="35756-222">Identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="35756-222">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="35756-223">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="35756-223">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="35756-224">A chave para **o \_ físico do CIM** é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="35756-224">The key for **CIM\_PhysicalElement** is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="35756-225">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="35756-225">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="35756-226">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="35756-226">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="35756-227">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="35756-227">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="35756-228">**Versão**</span><span class="sxs-lookup"><span data-stu-id="35756-228">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35756-229">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="35756-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35756-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35756-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35756-231">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="35756-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="35756-232">Indica a versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="35756-232">Indicates the version of the physical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35756-233">Comentários</span><span class="sxs-lookup"><span data-stu-id="35756-233">Remarks</span></span>

<span data-ttu-id="35756-234">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="35756-234">WMI does not implement this class.</span></span> <span data-ttu-id="35756-235">Para classes WMI derivadas do **CIM \_ físicoelement**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="35756-235">For WMI classes derived from **CIM\_PhysicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="35756-236">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="35756-236">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="35756-237">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="35756-237">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="35756-238">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35756-238">Requirements</span></span>



| <span data-ttu-id="35756-239">Requisito</span><span class="sxs-lookup"><span data-stu-id="35756-239">Requirement</span></span> | <span data-ttu-id="35756-240">Valor</span><span class="sxs-lookup"><span data-stu-id="35756-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35756-241">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35756-241">Minimum supported client</span></span><br/> | <span data-ttu-id="35756-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35756-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35756-243">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35756-243">Minimum supported server</span></span><br/> | <span data-ttu-id="35756-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35756-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35756-245">Namespace</span><span class="sxs-lookup"><span data-stu-id="35756-245">Namespace</span></span><br/>                | <span data-ttu-id="35756-246">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="35756-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="35756-247">MOF</span><span class="sxs-lookup"><span data-stu-id="35756-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35756-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35756-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="35756-249">DLL</span><span class="sxs-lookup"><span data-stu-id="35756-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35756-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35756-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35756-251">Confira também</span><span class="sxs-lookup"><span data-stu-id="35756-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35756-252">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="35756-252">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

