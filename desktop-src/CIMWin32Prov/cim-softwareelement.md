---
description: A \_ classe CIM softwareelement decompõe um objeto CIM \_ SoftwareFeature em um conjunto de partes individuais gerenciáveis ou implantáveis para uma plataforma específica.
ms.assetid: b2418735-b738-411a-a620-acc31662f824
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElement (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.Caption
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.Description
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.InstallDate
- CIM_SoftwareElement.LanguageEdition
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.Status
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fbe64ddfcf81a7410f5654db89c2924a8eabacc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089262"
---
# <a name="cim_softwareelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="a35ad-103">Classe CIM_SoftwareElement (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="a35ad-103">CIM_SoftwareElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a35ad-104">A classe **CIM \_ softwareelement** decompõe um objeto [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) em um conjunto de partes individuais gerenciáveis ou implantáveis para uma plataforma específica.</span><span class="sxs-lookup"><span data-stu-id="a35ad-104">The **CIM\_SoftwareElement** class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="a35ad-105">A plataforma de um elemento de software é identificada exclusivamente por sua arquitetura de hardware e sistema operacional subjacentes.</span><span class="sxs-lookup"><span data-stu-id="a35ad-105">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

<span data-ttu-id="a35ad-106">Como tal, para entender os detalhes de como a funcionalidade de um recurso de software específico é fornecida em uma plataforma específica, os objetos **CIM \_ softwareelement** referenciados pelas associações do [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) são organizados em conjuntos não contíguos com base na propriedade **TargetOperatingSystem** .</span><span class="sxs-lookup"><span data-stu-id="a35ad-106">As such, to understand the details of how the functionality of a particular software feature is provided on a particular platform, the **CIM\_SoftwareElement** objects referenced by [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) associations are organized in disjoint sets based on the **TargetOperatingSystem** property.</span></span> <span data-ttu-id="a35ad-107">Um objeto **CIM \_ softwareelement** captura os detalhes de gerenciamento de uma parte ou componente em um dos quatro Estados caracterizados pela propriedade **SoftwareElementState** .</span><span class="sxs-lookup"><span data-stu-id="a35ad-107">A **CIM\_SoftwareElement** object captures the management details of a part or component in one of four states characterized by the **SoftwareElementState** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a35ad-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="a35ad-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a35ad-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a35ad-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a35ad-110">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a35ad-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a35ad-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a35ad-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35ad-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a35ad-112">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C561-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
  string   LanguageEdition;
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="a35ad-113">Membros</span><span class="sxs-lookup"><span data-stu-id="a35ad-113">Members</span></span>

<span data-ttu-id="a35ad-114">A classe **CIM \_ softwareelement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a35ad-114">The **CIM\_SoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="a35ad-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a35ad-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a35ad-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a35ad-116">Properties</span></span>

<span data-ttu-id="a35ad-117">A classe **CIM \_ softwareelement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a35ad-117">The **CIM\_SoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a35ad-118">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="a35ad-118">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,4 ")</span><span class="sxs-lookup"><span data-stu-id="a35ad-121">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-122">Identificador interno para a compilação deste elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a35ad-122">Internal identifier for the compilation of this software element.</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-123">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a35ad-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-126">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a35ad-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-127">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a35ad-127">Short textual description of the object.</span></span>

<span data-ttu-id="a35ad-128">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a35ad-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-129">**Código de**</span><span class="sxs-lookup"><span data-stu-id="a35ad-129">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-132">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a35ad-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-133">Conjunto de códigos usado pelo elemento software.</span><span class="sxs-lookup"><span data-stu-id="a35ad-133">Code set used by the software element.</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a35ad-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-137">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="a35ad-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-138">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a35ad-138">Textual description of the object.</span></span>

<span data-ttu-id="a35ad-139">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a35ad-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-140">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="a35ad-140">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-143">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="a35ad-143">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-144">Identificador do fabricante para o elemento de software, geralmente uma SKU (unidade de manutenção de estoque) ou um número de peça.</span><span class="sxs-lookup"><span data-stu-id="a35ad-144">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a35ad-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-146">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a35ad-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="a35ad-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-149">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="a35ad-149">Date and time the object was installed.</span></span> <span data-ttu-id="a35ad-150">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a35ad-150">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a35ad-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a35ad-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-152">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="a35ad-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-155">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,6 ")</span><span class="sxs-lookup"><span data-stu-id="a35ad-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-156">Language Edition do elemento software.</span><span class="sxs-lookup"><span data-stu-id="a35ad-156">Language edition of the software element.</span></span> <span data-ttu-id="a35ad-157">Os códigos de idioma definidos no ISO 639 devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="a35ad-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="a35ad-158">Onde o elemento software representa versões multilíngues ou internacionais de um produto, a cadeia de caracteres "multilíngue" deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="a35ad-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-159">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="a35ad-159">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-162">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="a35ad-162">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-163">Fabricante do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a35ad-163">Manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-164">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a35ad-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-167">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a35ad-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-168">Nome usado para identificar o elemento de software que essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a35ad-168">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-169">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="a35ad-169">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-172">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="a35ad-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-173">O tipo de fabricante e sistema operacional para um elemento de software quando a propriedade **TargetOperatingSystem** tem um valor de 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="a35ad-173">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="a35ad-174">Quando a propriedade **TargetOperatingSystem** tem um valor de 1, essa propriedade deve ter um valor não nulo.</span><span class="sxs-lookup"><span data-stu-id="a35ad-174">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="a35ad-175">Para todos os outros valores de **TargetOperatingSystem** , essa propriedade é NULL.</span><span class="sxs-lookup"><span data-stu-id="a35ad-175">For all other **TargetOperatingSystem** values, this property is null.</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-176">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="a35ad-176">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-179">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="a35ad-179">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-180">Número de série do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a35ad-180">Serial number of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-181">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="a35ad-181">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-184">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a35ad-184">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-185">Identificador para o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a35ad-185">Identifier for the software element.</span></span> <span data-ttu-id="a35ad-186">Ele foi projetado para ser usado em conjunto com outras chaves para criar uma representação exclusiva desse **CIM \_ softwareelement**.</span><span class="sxs-lookup"><span data-stu-id="a35ad-186">It is designed to be used in conjunction with other keys to create a unique representation of this **CIM\_SoftwareElement**.</span></span>

</dd> <dt>

<span data-ttu-id="a35ad-187">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="a35ad-187">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-188">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a35ad-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-190">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a35ad-190">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-191">Estado de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a35ad-191">State of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="a35ad-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="a35ad-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-193">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="a35ad-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="a35ad-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="a35ad-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-195">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="a35ad-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="a35ad-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="a35ad-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-197">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="a35ad-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="a35ad-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="a35ad-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-199">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="a35ad-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a35ad-200">**Status**</span><span class="sxs-lookup"><span data-stu-id="a35ad-200">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-203">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a35ad-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-204">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a35ad-204">Current status of the object.</span></span>

<span data-ttu-id="a35ad-205">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a35ad-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a35ad-206">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a35ad-206">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a35ad-207">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a35ad-207">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a35ad-208">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="a35ad-208">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a35ad-209">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a35ad-209">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a35ad-210">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a35ad-210">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a35ad-211">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a35ad-211">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a35ad-212">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="a35ad-212">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a35ad-213">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="a35ad-213">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a35ad-214">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="a35ad-214">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a35ad-215">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="a35ad-215">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a35ad-216">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a35ad-216">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a35ad-217">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="a35ad-217">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a35ad-218">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="a35ad-218">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a35ad-219">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="a35ad-219">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-220">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a35ad-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-222">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de componente de software DMTF \| 2,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" sistema [**\_ operacional CIM**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="a35ad-222">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-223">Ambiente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a35ad-223">Operating system environment.</span></span> <span data-ttu-id="a35ad-224">O valor dessa propriedade não garante executability binários, mais informações são necessárias.</span><span class="sxs-lookup"><span data-stu-id="a35ad-224">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="a35ad-225">A versão do sistema operacional deve ser especificada usando a verificação de versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a35ad-225">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="a35ad-226">Também é necessária a arquitetura na qual o sistema operacional é executado.</span><span class="sxs-lookup"><span data-stu-id="a35ad-226">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="a35ad-227">A combinação dessas construções permite que o provedor identifique claramente o nível de sistema operacional necessário para um determinado elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a35ad-227">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a35ad-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a35ad-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a35ad-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a35ad-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="a35ad-230"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="a35ad-230"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-231">Mac OS</span><span class="sxs-lookup"><span data-stu-id="a35ad-231">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="a35ad-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="a35ad-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-233">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="a35ad-233">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="a35ad-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="a35ad-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="a35ad-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="a35ad-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="a35ad-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="a35ad-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="a35ad-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="a35ad-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-238">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="a35ad-238">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="a35ad-239"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="a35ad-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-240">HP-UX</span><span class="sxs-lookup"><span data-stu-id="a35ad-240">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="a35ad-241"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="a35ad-241"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="a35ad-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="a35ad-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="a35ad-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="a35ad-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="a35ad-244"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="a35ad-244"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="a35ad-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="a35ad-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-246">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="a35ad-246">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="a35ad-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="a35ad-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="a35ad-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="a35ad-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-249">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="a35ad-249">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="a35ad-250"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="a35ad-250"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-251">Windows 95</span><span class="sxs-lookup"><span data-stu-id="a35ad-251">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="a35ad-252"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="a35ad-252"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-253">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a35ad-253">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="a35ad-254"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="a35ad-254"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-255">Windows NT</span><span class="sxs-lookup"><span data-stu-id="a35ad-255">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="a35ad-256"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="a35ad-256"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-257">Windows CE</span><span class="sxs-lookup"><span data-stu-id="a35ad-257">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="a35ad-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="a35ad-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-259">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="a35ad-259">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="a35ad-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="a35ad-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="a35ad-261"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="a35ad-261"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="a35ad-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="a35ad-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="a35ad-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="a35ad-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="a35ad-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="a35ad-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="a35ad-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="a35ad-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="a35ad-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="a35ad-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="a35ad-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="a35ad-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="a35ad-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="a35ad-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="a35ad-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="a35ad-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="a35ad-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="a35ad-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="a35ad-271"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="a35ad-271"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-272">Uma série</span><span class="sxs-lookup"><span data-stu-id="a35ad-272">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="a35ad-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="a35ad-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-274">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="a35ad-274">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="a35ad-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="a35ad-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-276">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="a35ad-276">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="a35ad-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="a35ad-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-278">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="a35ad-278">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="a35ad-279"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="a35ad-279"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="a35ad-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="a35ad-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="a35ad-281"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="a35ad-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="a35ad-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="a35ad-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="a35ad-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="a35ad-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="a35ad-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="a35ad-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-285">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="a35ad-285">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="a35ad-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="a35ad-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="a35ad-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="a35ad-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="a35ad-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="a35ad-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="a35ad-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="a35ad-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-290">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="a35ad-290">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="a35ad-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="a35ad-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="a35ad-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="a35ad-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="a35ad-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="a35ad-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="a35ad-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="a35ad-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="a35ad-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="a35ad-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="a35ad-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="a35ad-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="a35ad-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="a35ad-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="a35ad-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="a35ad-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="a35ad-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="a35ad-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="a35ad-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="a35ad-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="a35ad-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="a35ad-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="a35ad-302">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="a35ad-302">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="a35ad-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="a35ad-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="a35ad-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="a35ad-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="a35ad-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="a35ad-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="a35ad-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="a35ad-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="a35ad-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="a35ad-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a35ad-308">**Versão**</span><span class="sxs-lookup"><span data-stu-id="a35ad-308">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a35ad-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a35ad-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a35ad-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a35ad-311">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="a35ad-311">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a35ad-312">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="a35ad-312">Version of the operation.</span></span>

<span data-ttu-id="a35ad-313">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="a35ad-313">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="a35ad-314"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="a35ad-314"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="a35ad-315"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="a35ad-315"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a35ad-316">Comentários</span><span class="sxs-lookup"><span data-stu-id="a35ad-316">Remarks</span></span>

<span data-ttu-id="a35ad-317">A classe **CIM \_ softwareelement** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a35ad-317">The **CIM\_SoftwareElement** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="a35ad-318">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="a35ad-318">WMI does not implement this class.</span></span> <span data-ttu-id="a35ad-319">Para classes WMI derivadas do **CIM \_ softwareelement**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a35ad-319">For WMI classes derived from **CIM\_SoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a35ad-320">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="a35ad-320">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a35ad-321">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="a35ad-321">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a35ad-322">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a35ad-322">Requirements</span></span>



| <span data-ttu-id="a35ad-323">Requisito</span><span class="sxs-lookup"><span data-stu-id="a35ad-323">Requirement</span></span> | <span data-ttu-id="a35ad-324">Valor</span><span class="sxs-lookup"><span data-stu-id="a35ad-324">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a35ad-325">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a35ad-325">Minimum supported client</span></span><br/> | <span data-ttu-id="a35ad-326">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a35ad-326">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a35ad-327">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a35ad-327">Minimum supported server</span></span><br/> | <span data-ttu-id="a35ad-328">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a35ad-328">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a35ad-329">Namespace</span><span class="sxs-lookup"><span data-stu-id="a35ad-329">Namespace</span></span><br/>                | <span data-ttu-id="a35ad-330">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a35ad-330">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a35ad-331">MOF</span><span class="sxs-lookup"><span data-stu-id="a35ad-331">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a35ad-332"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a35ad-332"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a35ad-333">DLL</span><span class="sxs-lookup"><span data-stu-id="a35ad-333">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a35ad-334"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a35ad-334"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a35ad-335">Confira também</span><span class="sxs-lookup"><span data-stu-id="a35ad-335">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35ad-336">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="a35ad-336">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

