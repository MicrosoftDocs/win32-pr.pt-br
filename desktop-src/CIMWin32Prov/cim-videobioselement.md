---
description: A \_ classe CIM VideoBIOSElement representa o software de nível baixo que é carregado no armazenamento não volátil e usado para configurar e acessar o controlador de vídeo de um sistema de computador e exibi-lo.
ms.assetid: f23d411f-4781-4727-abd1-61fe1a366bf0
ms.tgt_platform: multiple
title: Classe CIM_VideoBIOSElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSElement
- CIM_VideoBIOSElement.BuildNumber
- CIM_VideoBIOSElement.Caption
- CIM_VideoBIOSElement.CodeSet
- CIM_VideoBIOSElement.Description
- CIM_VideoBIOSElement.IdentificationCode
- CIM_VideoBIOSElement.InstallDate
- CIM_VideoBIOSElement.IsShadowed
- CIM_VideoBIOSElement.LanguageEdition
- CIM_VideoBIOSElement.Manufacturer
- CIM_VideoBIOSElement.Name
- CIM_VideoBIOSElement.OtherTargetOS
- CIM_VideoBIOSElement.SerialNumber
- CIM_VideoBIOSElement.SoftwareElementID
- CIM_VideoBIOSElement.SoftwareElementState
- CIM_VideoBIOSElement.Status
- CIM_VideoBIOSElement.TargetOperatingSystem
- CIM_VideoBIOSElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d873b17f0bf0ea123d988d281c0cab728dd50f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920319"
---
# <a name="cim_videobioselement-class"></a><span data-ttu-id="18ed8-103">\_Classe CIM VideoBIOSElement</span><span class="sxs-lookup"><span data-stu-id="18ed8-103">CIM\_VideoBIOSElement class</span></span>

<span data-ttu-id="18ed8-104">A classe **CIM \_ VideoBIOSElement** representa o software de nível baixo que é carregado no armazenamento não volátil e usado para configurar e acessar o controlador de vídeo de um sistema de computador e exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="18ed8-104">The **CIM\_VideoBIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18ed8-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="18ed8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="18ed8-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="18ed8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="18ed8-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="18ed8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="18ed8-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="18ed8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ed8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18ed8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{76148BF6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_VideoBIOSElement : CIM_SoftwareElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
  boolean  IsShadowed;
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

## <a name="members"></a><span data-ttu-id="18ed8-110">Membros</span><span class="sxs-lookup"><span data-stu-id="18ed8-110">Members</span></span>

<span data-ttu-id="18ed8-111">A classe **CIM \_ VideoBIOSElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="18ed8-111">The **CIM\_VideoBIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="18ed8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="18ed8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18ed8-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="18ed8-113">Properties</span></span>

<span data-ttu-id="18ed8-114">A classe **CIM \_ VideoBIOSElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="18ed8-114">The **CIM\_VideoBIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18ed8-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="18ed8-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,4 ")</span><span class="sxs-lookup"><span data-stu-id="18ed8-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-119">Identificador interno para a compilação deste elemento de software.</span><span class="sxs-lookup"><span data-stu-id="18ed8-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="18ed8-120">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="18ed8-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-124">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="18ed8-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-125">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="18ed8-125">Short textual description of the object.</span></span>

<span data-ttu-id="18ed8-126">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-127">**Código de**</span><span class="sxs-lookup"><span data-stu-id="18ed8-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-130">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="18ed8-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-131">Conjunto de códigos usado pelo elemento software.</span><span class="sxs-lookup"><span data-stu-id="18ed8-131">Code set used by the software element.</span></span>

<span data-ttu-id="18ed8-132">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-133">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="18ed8-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-136">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="18ed8-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-137">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="18ed8-137">Textual description of the object.</span></span>

<span data-ttu-id="18ed8-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-139">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="18ed8-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-142">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="18ed8-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-143">Identificador do fabricante para o elemento de software, como uma SKU (unidade de manutenção de estoque) ou um número de peça.</span><span class="sxs-lookup"><span data-stu-id="18ed8-143">Manufacturer's identifier for the software element, such as a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="18ed8-144">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18ed8-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-146">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18ed8-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="18ed8-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-149">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="18ed8-149">Date and time the object was installed.</span></span> <span data-ttu-id="18ed8-150">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="18ed8-150">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="18ed8-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-152">**Issombreado**</span><span class="sxs-lookup"><span data-stu-id="18ed8-152">**IsShadowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-153">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="18ed8-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-155">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS de vídeo DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="18ed8-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-156">Se **for true**, o BIOS de vídeo será sombreado.</span><span class="sxs-lookup"><span data-stu-id="18ed8-156">If **TRUE**, the video BIOS is shadowed.</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-157">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="18ed8-157">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-160">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,6 ")</span><span class="sxs-lookup"><span data-stu-id="18ed8-160">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-161">Language Edition do elemento software.</span><span class="sxs-lookup"><span data-stu-id="18ed8-161">Language edition of the software element.</span></span> <span data-ttu-id="18ed8-162">Os códigos de idioma definidos no ISO 639 devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="18ed8-162">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="18ed8-163">Quando o elemento software representa uma versão multilíngue ou internacional de um produto, a cadeia de caracteres "multilíngue" deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="18ed8-163">When the software element represents a multilingual or international version of a product, the string "Multilingual" should be used.</span></span>

<span data-ttu-id="18ed8-164">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-164">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-165">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="18ed8-165">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-168">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="18ed8-168">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-169">Fabricante do elemento de software essa propriedade é herdada do [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-169">Manufacturer of the software element This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-170">**Nome**</span><span class="sxs-lookup"><span data-stu-id="18ed8-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-173">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="18ed8-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-174">Nome usado para identificar o elemento de software que essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-174">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-175">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="18ed8-175">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-178">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="18ed8-178">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-179">O tipo de fabricante e sistema operacional para um elemento de software quando a propriedade **TargetOperatingSystem** tem um valor de 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="18ed8-179">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="18ed8-180">Quando a propriedade **TargetOperatingSystem** tem um valor de 1, essa propriedade deve ter um valor não nulo.</span><span class="sxs-lookup"><span data-stu-id="18ed8-180">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="18ed8-181">Para todos os outros valores de **TargetOperatingSystem** , essa propriedade é NULL.</span><span class="sxs-lookup"><span data-stu-id="18ed8-181">For all other **TargetOperatingSystem** values, this property is null.</span></span> <span data-ttu-id="18ed8-182">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-182">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-183">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="18ed8-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-186">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="18ed8-186">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-187">Número de série atribuído do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="18ed8-187">Assigned serial number of the software element.</span></span>

<span data-ttu-id="18ed8-188">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-188">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-189">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="18ed8-189">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-192">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="18ed8-192">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-193">Identificador para o elemento de software que foi projetado para ser usado em conjunto com outras chaves para criar uma representação exclusiva da classe [**CIM \_ softwareelement**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="18ed8-193">Identifier for the software element that is designed to be used in conjunction with other keys to create a unique representation of the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

<span data-ttu-id="18ed8-194">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-194">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ed8-195">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="18ed8-195">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-196">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18ed8-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-198">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18ed8-198">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-199">Estado de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="18ed8-199">State of a software element.</span></span>

<span data-ttu-id="18ed8-200">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-200">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="18ed8-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="18ed8-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-202">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="18ed8-202">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="18ed8-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="18ed8-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-204">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="18ed8-204">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="18ed8-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="18ed8-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-206">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="18ed8-206">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="18ed8-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="18ed8-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-208">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="18ed8-208">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18ed8-209">**Status**</span><span class="sxs-lookup"><span data-stu-id="18ed8-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-212">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="18ed8-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-213">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="18ed8-213">Current status of the object.</span></span> <span data-ttu-id="18ed8-214">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="18ed8-215">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="18ed8-215">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="18ed8-216">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="18ed8-216">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="18ed8-217">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="18ed8-217">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18ed8-218">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="18ed8-218">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18ed8-219">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="18ed8-219">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="18ed8-220">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="18ed8-220">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="18ed8-221">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="18ed8-221">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="18ed8-222">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="18ed8-222">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="18ed8-223">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="18ed8-223">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="18ed8-224">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="18ed8-224">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="18ed8-225">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="18ed8-225">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="18ed8-226">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="18ed8-226">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="18ed8-227">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="18ed8-227">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18ed8-228">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="18ed8-228">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-229">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18ed8-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-231">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de componente de software DMTF \| 2,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" sistema [**\_ operacional CIM**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="18ed8-231">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-232">Ambiente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="18ed8-232">Operating system environment.</span></span> <span data-ttu-id="18ed8-233">O valor dessa propriedade não garante a execução binária.</span><span class="sxs-lookup"><span data-stu-id="18ed8-233">The value of this property does not ensure binary execution.</span></span> <span data-ttu-id="18ed8-234">A versão do sistema operacional deve ser especificada usando a verificação de versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="18ed8-234">The version of the operating system must be specified using the operating system version check.</span></span> <span data-ttu-id="18ed8-235">Também é necessária a arquitetura na qual o sistema operacional é executado.</span><span class="sxs-lookup"><span data-stu-id="18ed8-235">Also required is the architecture on which the operating system runs.</span></span> <span data-ttu-id="18ed8-236">A combinação dessas construções permite que o provedor identifique claramente o nível de sistema operacional necessário para um determinado elemento de software.</span><span class="sxs-lookup"><span data-stu-id="18ed8-236">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="18ed8-237">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-237">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18ed8-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="18ed8-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18ed8-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="18ed8-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="18ed8-240"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="18ed8-240"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-241">Mac OS</span><span class="sxs-lookup"><span data-stu-id="18ed8-241">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="18ed8-242"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="18ed8-242"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-243">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="18ed8-243">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="18ed8-244"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="18ed8-244"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="18ed8-245"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="18ed8-245"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="18ed8-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="18ed8-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="18ed8-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="18ed8-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-248">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="18ed8-248">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="18ed8-249"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="18ed8-249"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-250">HP-UX</span><span class="sxs-lookup"><span data-stu-id="18ed8-250">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="18ed8-251"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="18ed8-251"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="18ed8-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="18ed8-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="18ed8-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="18ed8-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="18ed8-254"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="18ed8-254"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="18ed8-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="18ed8-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-256">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="18ed8-256">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="18ed8-257"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="18ed8-257"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="18ed8-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="18ed8-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-259">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="18ed8-259">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="18ed8-260"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="18ed8-260"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-261">Windows 95</span><span class="sxs-lookup"><span data-stu-id="18ed8-261">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="18ed8-262"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="18ed8-262"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-263">Windows 98</span><span class="sxs-lookup"><span data-stu-id="18ed8-263">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="18ed8-264"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="18ed8-264"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-265">Windows NT</span><span class="sxs-lookup"><span data-stu-id="18ed8-265">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="18ed8-266"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="18ed8-266"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-267">Windows CE</span><span class="sxs-lookup"><span data-stu-id="18ed8-267">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="18ed8-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="18ed8-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-269">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="18ed8-269">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="18ed8-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="18ed8-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="18ed8-271"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="18ed8-271"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="18ed8-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="18ed8-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="18ed8-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="18ed8-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="18ed8-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="18ed8-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="18ed8-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="18ed8-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="18ed8-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="18ed8-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="18ed8-277"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="18ed8-277"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="18ed8-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="18ed8-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="18ed8-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="18ed8-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="18ed8-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="18ed8-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="18ed8-281"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="18ed8-281"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-282">Uma série</span><span class="sxs-lookup"><span data-stu-id="18ed8-282">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="18ed8-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="18ed8-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-284">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="18ed8-284">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="18ed8-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="18ed8-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-286">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="18ed8-286">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="18ed8-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="18ed8-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-288">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="18ed8-288">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="18ed8-289"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="18ed8-289"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="18ed8-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="18ed8-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="18ed8-291"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="18ed8-291"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="18ed8-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="18ed8-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="18ed8-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="18ed8-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="18ed8-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="18ed8-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-295">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="18ed8-295">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="18ed8-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="18ed8-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="18ed8-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="18ed8-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="18ed8-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="18ed8-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="18ed8-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="18ed8-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-300">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="18ed8-300">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="18ed8-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="18ed8-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="18ed8-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="18ed8-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="18ed8-303"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="18ed8-303"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="18ed8-304"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="18ed8-304"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="18ed8-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="18ed8-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="18ed8-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="18ed8-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="18ed8-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="18ed8-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="18ed8-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="18ed8-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="18ed8-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="18ed8-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="18ed8-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="18ed8-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="18ed8-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="18ed8-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="18ed8-312">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="18ed8-312">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="18ed8-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="18ed8-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="18ed8-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="18ed8-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="18ed8-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="18ed8-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="18ed8-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="18ed8-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="18ed8-317"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="18ed8-317"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18ed8-318">**Versão**</span><span class="sxs-lookup"><span data-stu-id="18ed8-318">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ed8-319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18ed8-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ed8-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18ed8-321">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="18ed8-321">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="18ed8-322">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="18ed8-322">Version of the operation.</span></span>

<span data-ttu-id="18ed8-323">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="18ed8-323">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="18ed8-324"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="18ed8-324"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="18ed8-325"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="18ed8-325"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="18ed8-326">Essa propriedade é herdada da classe [**CIM \_ softwareelement**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="18ed8-326">This property is inherited from the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18ed8-327">Comentários</span><span class="sxs-lookup"><span data-stu-id="18ed8-327">Remarks</span></span>

<span data-ttu-id="18ed8-328">A classe **CIM \_ VideoBIOSElement** é derivada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="18ed8-328">The **CIM\_VideoBIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="18ed8-329">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="18ed8-329">WMI does not implement this class.</span></span>

<span data-ttu-id="18ed8-330">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="18ed8-330">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="18ed8-331">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="18ed8-331">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ed8-332">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18ed8-332">Requirements</span></span>



| <span data-ttu-id="18ed8-333">Requisito</span><span class="sxs-lookup"><span data-stu-id="18ed8-333">Requirement</span></span> | <span data-ttu-id="18ed8-334">Valor</span><span class="sxs-lookup"><span data-stu-id="18ed8-334">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18ed8-335">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18ed8-335">Minimum supported client</span></span><br/> | <span data-ttu-id="18ed8-336">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18ed8-336">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18ed8-337">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18ed8-337">Minimum supported server</span></span><br/> | <span data-ttu-id="18ed8-338">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18ed8-338">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18ed8-339">Namespace</span><span class="sxs-lookup"><span data-stu-id="18ed8-339">Namespace</span></span><br/>                | <span data-ttu-id="18ed8-340">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="18ed8-340">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18ed8-341">MOF</span><span class="sxs-lookup"><span data-stu-id="18ed8-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18ed8-342"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18ed8-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18ed8-343">DLL</span><span class="sxs-lookup"><span data-stu-id="18ed8-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18ed8-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18ed8-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ed8-345">Confira também</span><span class="sxs-lookup"><span data-stu-id="18ed8-345">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ed8-346">**\_Software CIM**</span><span class="sxs-lookup"><span data-stu-id="18ed8-346">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

