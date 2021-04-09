---
description: A \_ classe CIM bioselement representa o software de nível baixo que é carregado no armazenamento não volátil e usado para iniciar e configurar um sistema de computador.
ms.assetid: c203244a-51e0-4733-a0bc-cf9b7957f364
ms.tgt_platform: multiple
title: Classe CIM_BIOSElement (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Caption
- CIM_BIOSElement.Description
- CIM_BIOSElement.InstallDate
- CIM_BIOSElement.Status
- CIM_BIOSElement.Name
- CIM_BIOSElement.BuildNumber
- CIM_BIOSElement.CodeSet
- CIM_BIOSElement.IdentificationCode
- CIM_BIOSElement.LanguageEdition
- CIM_BIOSElement.OtherTargetOS
- CIM_BIOSElement.SerialNumber
- CIM_BIOSElement.SoftwareElementID
- CIM_BIOSElement.SoftwareElementState
- CIM_BIOSElement.TargetOperatingSystem
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.Version
- CIM_BIOSElement.PrimaryBIOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21cd0d13d62f5cfa70f579110480b4c11c36b77d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010236"
---
# <a name="cim_bioselement-class-cimwin32-wmi-providers"></a><span data-ttu-id="495fa-103">Classe CIM_BIOSElement (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="495fa-103">CIM_BIOSElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="495fa-104">A classe **CIM \_ bioselement** representa o software de nível baixo que é carregado no armazenamento não volátil e usado para iniciar e configurar um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="495fa-104">The **CIM\_BIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="495fa-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="495fa-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="495fa-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="495fa-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="495fa-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="495fa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="495fa-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="495fa-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="495fa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="495fa-109">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C562-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  string   BuildNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  uint16   TargetOperatingSystem;
  string   Manufacturer;
  string   Version;
  boolean  PrimaryBIOS;
};
```

## <a name="members"></a><span data-ttu-id="495fa-110">Membros</span><span class="sxs-lookup"><span data-stu-id="495fa-110">Members</span></span>

<span data-ttu-id="495fa-111">A classe **CIM \_ bioselement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="495fa-111">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="495fa-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="495fa-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="495fa-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="495fa-113">Properties</span></span>

<span data-ttu-id="495fa-114">A classe **CIM \_ bioselement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="495fa-114">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="495fa-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="495fa-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,4 ")</span><span class="sxs-lookup"><span data-stu-id="495fa-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-119">Identificador interno para a compilação deste elemento de software.</span><span class="sxs-lookup"><span data-stu-id="495fa-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="495fa-120">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="495fa-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="495fa-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-124">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="495fa-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-125">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="495fa-125">A short textual description of the object.</span></span>

<span data-ttu-id="495fa-126">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="495fa-127">**Código de**</span><span class="sxs-lookup"><span data-stu-id="495fa-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-130">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="495fa-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="495fa-131">Conjunto de códigos usado pelo elemento software.</span><span class="sxs-lookup"><span data-stu-id="495fa-131">Code set used by the software element.</span></span>

<span data-ttu-id="495fa-132">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="495fa-133">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="495fa-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-136">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="495fa-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-137">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="495fa-137">A textual description of the object.</span></span>

<span data-ttu-id="495fa-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="495fa-139">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="495fa-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-142">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="495fa-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-143">Identificador do fabricante para o elemento de software, geralmente uma SKU (unidade de manutenção de estoque) ou um número de peça.</span><span class="sxs-lookup"><span data-stu-id="495fa-143">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="495fa-144">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="495fa-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="495fa-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-146">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="495fa-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="495fa-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-149">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="495fa-149">Indicates when the object was installed.</span></span> <span data-ttu-id="495fa-150">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="495fa-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="495fa-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="495fa-152">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="495fa-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-155">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,6 ")</span><span class="sxs-lookup"><span data-stu-id="495fa-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-156">Language Edition do elemento software.</span><span class="sxs-lookup"><span data-stu-id="495fa-156">Language edition of the software element.</span></span> <span data-ttu-id="495fa-157">Os códigos de idioma definidos no ISO 639 devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="495fa-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="495fa-158">Onde o elemento software representa versões multilíngues ou internacionais de um produto, a cadeia de caracteres "multilíngue" deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="495fa-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="495fa-159">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-159">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="495fa-160">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="495fa-160">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-163">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("fabricante"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="495fa-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-164">O fabricante do BIOS.</span><span class="sxs-lookup"><span data-stu-id="495fa-164">The manufacturer of the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="495fa-165">**Nome**</span><span class="sxs-lookup"><span data-stu-id="495fa-165">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-168">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="495fa-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="495fa-169">O nome usado para identificar este elemento de software</span><span class="sxs-lookup"><span data-stu-id="495fa-169">The name used to identify this software element</span></span>

<span data-ttu-id="495fa-170">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-170">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="495fa-171">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="495fa-171">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-174">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="495fa-174">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-175">O tipo de fabricante e sistema operacional para um elemento de software quando a propriedade **TargetOperatingSystem** tem um valor de 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="495fa-175">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="495fa-176">Quando a propriedade **TargetOperatingSystem** tem um valor de 1, essa propriedade deve ter um valor não nulo.</span><span class="sxs-lookup"><span data-stu-id="495fa-176">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="495fa-177">Para todos os outros valores de **TargetOperatingSystem** , essa propriedade é NULL.</span><span class="sxs-lookup"><span data-stu-id="495fa-177">For all other **TargetOperatingSystem** values, this property is null.</span></span>

<span data-ttu-id="495fa-178">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-178">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="495fa-179">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="495fa-179">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-180">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="495fa-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-182">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="495fa-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-183">Se for **true**, esse é o BIOS primário do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="495fa-183">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="495fa-184">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="495fa-184">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-187">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="495fa-187">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-188">Número de série do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="495fa-188">Serial number of the software element.</span></span>

<span data-ttu-id="495fa-189">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-189">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="495fa-190">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="495fa-190">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-193">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="495fa-193">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="495fa-194">Identificador para o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="495fa-194">Identifier for the software element.</span></span> <span data-ttu-id="495fa-195">Ele foi projetado para ser usado em conjunto com outras chaves para criar uma representação exclusiva desse [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-195">It is designed to be used in conjunction with other keys to create a unique representation of this [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="495fa-196">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-196">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="495fa-197">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="495fa-197">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-198">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="495fa-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-200">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="495fa-200">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="495fa-201">Estado de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="495fa-201">State of a software element.</span></span>

<span data-ttu-id="495fa-202">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-202">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="495fa-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="495fa-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-204">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="495fa-204">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="495fa-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="495fa-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-206">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="495fa-206">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="495fa-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="495fa-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-208">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="495fa-208">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="495fa-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="495fa-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-210">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="495fa-210">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="495fa-211">**Status**</span><span class="sxs-lookup"><span data-stu-id="495fa-211">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-212">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-214">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="495fa-214">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-215">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="495fa-215">String that indicates the current status of the object.</span></span> <span data-ttu-id="495fa-216">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="495fa-216">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="495fa-217">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="495fa-217">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="495fa-218">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="495fa-218">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="495fa-219">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="495fa-219">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="495fa-220">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="495fa-220">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="495fa-221">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="495fa-221">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="495fa-222">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="495fa-223">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="495fa-223">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="495fa-224">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="495fa-224">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="495fa-225">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="495fa-225">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="495fa-226">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="495fa-226">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="495fa-227">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="495fa-227">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="495fa-228">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="495fa-228">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="495fa-229">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="495fa-229">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="495fa-230">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="495fa-230">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="495fa-231">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="495fa-231">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="495fa-232">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="495fa-232">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="495fa-233">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="495fa-233">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="495fa-234">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="495fa-234">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="495fa-235">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="495fa-235">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="495fa-236">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="495fa-236">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-237">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="495fa-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-239">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de componente de software DMTF \| 2,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" sistema [**\_ operacional CIM**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="495fa-239">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-240">Ambiente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="495fa-240">Operating system environment.</span></span> <span data-ttu-id="495fa-241">O valor dessa propriedade não garante executability binários, mais informações são necessárias.</span><span class="sxs-lookup"><span data-stu-id="495fa-241">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="495fa-242">A versão do sistema operacional deve ser especificada usando a verificação de versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="495fa-242">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="495fa-243">Também é necessária a arquitetura na qual o sistema operacional é executado.</span><span class="sxs-lookup"><span data-stu-id="495fa-243">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="495fa-244">A combinação dessas construções permite que o provedor identifique claramente o nível de sistema operacional necessário para um determinado elemento de software.</span><span class="sxs-lookup"><span data-stu-id="495fa-244">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="495fa-245">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-245">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="495fa-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="495fa-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="495fa-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="495fa-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="495fa-248"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="495fa-248"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-249">Mac OS</span><span class="sxs-lookup"><span data-stu-id="495fa-249">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="495fa-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="495fa-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-251">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="495fa-251">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="495fa-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="495fa-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="495fa-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="495fa-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="495fa-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="495fa-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="495fa-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="495fa-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-256">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="495fa-256">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="495fa-257"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="495fa-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-258">HP-UX</span><span class="sxs-lookup"><span data-stu-id="495fa-258">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="495fa-259"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="495fa-259"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="495fa-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="495fa-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="495fa-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="495fa-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="495fa-262"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="495fa-262"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="495fa-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="495fa-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-264">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="495fa-264">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="495fa-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="495fa-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="495fa-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="495fa-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-267">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="495fa-267">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="495fa-268"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="495fa-268"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-269">Windows 95</span><span class="sxs-lookup"><span data-stu-id="495fa-269">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="495fa-270"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="495fa-270"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-271">Windows 98</span><span class="sxs-lookup"><span data-stu-id="495fa-271">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="495fa-272"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="495fa-272"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-273">Windows NT</span><span class="sxs-lookup"><span data-stu-id="495fa-273">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="495fa-274"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="495fa-274"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-275">Windows CE</span><span class="sxs-lookup"><span data-stu-id="495fa-275">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="495fa-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="495fa-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-277">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="495fa-277">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="495fa-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="495fa-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="495fa-279"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="495fa-279"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="495fa-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="495fa-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="495fa-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="495fa-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="495fa-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="495fa-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="495fa-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="495fa-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="495fa-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="495fa-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="495fa-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="495fa-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="495fa-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="495fa-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="495fa-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="495fa-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="495fa-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="495fa-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="495fa-289"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="495fa-289"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-290">Uma série</span><span class="sxs-lookup"><span data-stu-id="495fa-290">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="495fa-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="495fa-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-292">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="495fa-292">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="495fa-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="495fa-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-294">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="495fa-294">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="495fa-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="495fa-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-296">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="495fa-296">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="495fa-297"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="495fa-297"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="495fa-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="495fa-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="495fa-299"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="495fa-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="495fa-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="495fa-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="495fa-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="495fa-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="495fa-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="495fa-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-303">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="495fa-303">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="495fa-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="495fa-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="495fa-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="495fa-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="495fa-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="495fa-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="495fa-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="495fa-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-308">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="495fa-308">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="495fa-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="495fa-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="495fa-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="495fa-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="495fa-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="495fa-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="495fa-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="495fa-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="495fa-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="495fa-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="495fa-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="495fa-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="495fa-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="495fa-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="495fa-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="495fa-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="495fa-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="495fa-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="495fa-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="495fa-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="495fa-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="495fa-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="495fa-320">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="495fa-320">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="495fa-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="495fa-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="495fa-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="495fa-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="495fa-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="495fa-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="495fa-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="495fa-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="495fa-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="495fa-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="495fa-326">**Versão**</span><span class="sxs-lookup"><span data-stu-id="495fa-326">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="495fa-327">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="495fa-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="495fa-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="495fa-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="495fa-329">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="495fa-329">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="495fa-330">A versão do BIOS.</span><span class="sxs-lookup"><span data-stu-id="495fa-330">The version of the BIOS.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="495fa-331">Comentários</span><span class="sxs-lookup"><span data-stu-id="495fa-331">Remarks</span></span>

<span data-ttu-id="495fa-332">A classe **CIM \_ bioselement** é derivada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-332">The **CIM\_BIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="495fa-333">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="495fa-333">WMI does not implement this class.</span></span> <span data-ttu-id="495fa-334">Para obter mais informações sobre classes derivadas de **CIM \_ bioselement**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="495fa-334">For more information about classes derived from **CIM\_BIOSElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="495fa-335">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="495fa-335">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="495fa-336">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="495fa-336">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="495fa-337">Requisitos</span><span class="sxs-lookup"><span data-stu-id="495fa-337">Requirements</span></span>



| <span data-ttu-id="495fa-338">Requisito</span><span class="sxs-lookup"><span data-stu-id="495fa-338">Requirement</span></span> | <span data-ttu-id="495fa-339">Valor</span><span class="sxs-lookup"><span data-stu-id="495fa-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="495fa-340">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="495fa-340">Minimum supported client</span></span><br/> | <span data-ttu-id="495fa-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="495fa-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="495fa-342">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="495fa-342">Minimum supported server</span></span><br/> | <span data-ttu-id="495fa-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="495fa-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="495fa-344">Namespace</span><span class="sxs-lookup"><span data-stu-id="495fa-344">Namespace</span></span><br/>                | <span data-ttu-id="495fa-345">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="495fa-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="495fa-346">MOF</span><span class="sxs-lookup"><span data-stu-id="495fa-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="495fa-347"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="495fa-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="495fa-348">DLL</span><span class="sxs-lookup"><span data-stu-id="495fa-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="495fa-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="495fa-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="495fa-350">Confira também</span><span class="sxs-lookup"><span data-stu-id="495fa-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="495fa-351">**\_Software CIM**</span><span class="sxs-lookup"><span data-stu-id="495fa-351">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

