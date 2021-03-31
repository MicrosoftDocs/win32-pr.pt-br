---
description: Representa uma parte individual gerenciável ou implantável de um \_ SOFTWAREFEATURE CIM.
ms.assetid: 96affc55-b001-4122-b883-3610bf95a786
title: Classe CIM_SoftwareElement (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.Version
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.LanguageEdition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1d11b428e9a17819f850ce210e6854e4f1d17e52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662795"
---
# <a name="cim_softwareelement-class-hyper-v-management"></a><span data-ttu-id="4c482-103">Classe CIM_SoftwareElement (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="4c482-103">CIM_SoftwareElement class (Hyper-V management)</span></span>

<span data-ttu-id="4c482-104">Representa uma parte individual gerenciável ou implantável de **um \_ SoftwareFeature CIM**.</span><span class="sxs-lookup"><span data-stu-id="4c482-104">Represents an individually manageable or deployable part of a **CIM\_SoftwareFeature**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c482-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c482-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Application::DeploymentModel"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string Name;
  string Version;
  uint16 SoftwareElementState;
  string SoftwareElementID;
  uint16 TargetOperatingSystem;
  string OtherTargetOS;
  string Manufacturer;
  string BuildNumber;
  string SerialNumber;
  string CodeSet;
  string IdentificationCode;
  string LanguageEdition;
};
```

## <a name="members"></a><span data-ttu-id="4c482-106">Membros</span><span class="sxs-lookup"><span data-stu-id="4c482-106">Members</span></span>

<span data-ttu-id="4c482-107">A classe **CIM \_ softwareelement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4c482-107">The **CIM\_SoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="4c482-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c482-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c482-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c482-109">Properties</span></span>

<span data-ttu-id="4c482-110">A classe **CIM \_ softwareelement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4c482-110">The **CIM\_SoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c482-111">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="4c482-111">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c482-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-114">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,4 ")</span><span class="sxs-lookup"><span data-stu-id="4c482-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="4c482-115">O identificador interno para a compilação do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4c482-115">The internal identifier for the compilation of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="4c482-116">**Código de**</span><span class="sxs-lookup"><span data-stu-id="4c482-116">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c482-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-119">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4c482-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4c482-120">A codificação de caracteres usada pelo elemento de software, como UTF-8 e ISO8859-1.</span><span class="sxs-lookup"><span data-stu-id="4c482-120">The character encoding used by the software element, such as UTF-8 and ISO8859-1.</span></span>

</dd> <dt>

<span data-ttu-id="4c482-121">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="4c482-121">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c482-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-124">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Software de subcomponente do DMTF \| 1,6 ")</span><span class="sxs-lookup"><span data-stu-id="4c482-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="4c482-125">O identificador do fabricante do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4c482-125">The manufacturer identifier for the software element.</span></span> <span data-ttu-id="4c482-126">Isso geralmente é uma SKU (unidade de manutenção de estoque) ou um número de peça.</span><span class="sxs-lookup"><span data-stu-id="4c482-126">This is often a stock keeping unit (SKU) or a part number.</span></span>

</dd> <dt>

<span data-ttu-id="4c482-127">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="4c482-127">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c482-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-130">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Software de subcomponente do DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="4c482-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="4c482-131">A edição de idioma do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4c482-131">The language edition of the software element.</span></span> <span data-ttu-id="4c482-132">Os códigos de idioma definidos no padrão ISO 639 devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="4c482-132">The language codes defined in the ISO 639 standard should be used.</span></span> <span data-ttu-id="4c482-133">Se o elemento representa uma versão multilíngue ou internacional, a cadeia de caracteres "multilíngue" deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="4c482-133">If the element represents a multi-lingual or international version, the string "Multilingual" should be used.</span></span>

</dd> <dt>

<span data-ttu-id="4c482-134">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="4c482-134">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c482-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-137">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Software de subcomponente do DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="4c482-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="4c482-138">O fabricante do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4c482-138">The manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="4c482-139">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4c482-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c482-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-142">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4c482-142">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4c482-143">O nome usado para identificar o elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4c482-143">The name used to identify the software element.</span></span>

</dd> <dt>

<span data-ttu-id="4c482-144">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="4c482-144">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c482-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-147">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**sistema \_ operacional CIM**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="4c482-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="4c482-148">O tipo de fabricante e sistema operacional quando a propriedade **TargetOperatingSystem** é definida como **Other** ("1").</span><span class="sxs-lookup"><span data-stu-id="4c482-148">The manufacturer and operating system type when the **TargetOperatingSystem** property is set to **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="4c482-149">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="4c482-149">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c482-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-152">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="4c482-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="4c482-153">O número de série atribuído do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4c482-153">The assigned serial number of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="4c482-154">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="4c482-154">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c482-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-157">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4c482-157">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4c482-158">Um identificador para o elemento de software a ser usado em conjunto com outras chaves para criar um elemento de identificação exclusiva.</span><span class="sxs-lookup"><span data-stu-id="4c482-158">An identifier for the software element to use in conjunction with other keys to create a uniquely identify the element.</span></span>

</dd> <dt>

<span data-ttu-id="4c482-159">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="4c482-159">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-160">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4c482-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-162">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4c482-162">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4c482-163">O estado do ciclo de vida do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4c482-163">The life cycle state of the software element.</span></span>

<span data-ttu-id="4c482-164">\- Um Softwareelement no estado implantável descreve os detalhes necessários para distribuí-lo com êxito e os detalhes (verificações e ações) necessários para movê-lo para o estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="4c482-164">\- A SoftwareElement in the deployable state describes the details necessary to successfully distribute it and the details (Checks and Actions) required to move it to the installable state (i.e, the next state).</span></span>

<span data-ttu-id="4c482-165">\- Um Softwareelement no estado instalável descreve os detalhes necessários para instalá-lo com êxito e os detalhes (verificações e ações) necessários para criar um elemento no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="4c482-165">\- A SoftwareElement in the installable state describes the details necessary to successfully install it and the details (Checks and Actions) required to create an element in the executable state (i.e., the next state).</span></span>

<span data-ttu-id="4c482-166">\- Um Softwareelement no estado executável descreve os detalhes necessários para iniciá-lo com êxito e os detalhes (verificações e ações) necessários para movê-lo para o estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="4c482-166">\- A SoftwareElement in the executable state describes the details necessary to successfully start it and the details (Checks and Actions) required to move it to the running state (i.e., the next state).</span></span>

<span data-ttu-id="4c482-167">\- Um Softwareelement no estado running descreve os detalhes necessários para gerenciar o elemento Started.</span><span class="sxs-lookup"><span data-stu-id="4c482-167">\- A SoftwareElement in the running state describes the details necessary to manage the started element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="4c482-168">**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="4c482-168">**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="4c482-169">**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="4c482-169">**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="4c482-170">**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="4c482-170">**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="4c482-171">**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="4c482-171">**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4c482-172">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="4c482-172">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-173">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4c482-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-175">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Software de subcomponente do DMTF \| 1,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" sistema [**\_ operacional CIM**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="4c482-175">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="4c482-176">O sistema operacional do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4c482-176">The operating system of the software element.</span></span> <span data-ttu-id="4c482-177">O valor dessa propriedade não garante que seja um executável binário.</span><span class="sxs-lookup"><span data-stu-id="4c482-177">The value of this property does not ensure that it is binary executable.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4c482-178">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="4c482-178">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4c482-179">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="4c482-179">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="4c482-180">**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="4c482-180">**MACOS** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="4c482-181">**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="4c482-181">**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="4c482-182">**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="4c482-182">**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="4c482-183">**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="4c482-183">**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Tru64_UNIX"></span><span id="tru64_unix"></span><span id="TRU64_UNIX"></span>

<span data-ttu-id="4c482-184">**TRU64 UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="4c482-184">**Tru64 UNIX** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="4c482-185">**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="4c482-185">**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="4c482-186">HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="4c482-186">**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="4c482-187">**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="4c482-187">**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="4c482-188">**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="4c482-188">**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="4c482-189">**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="4c482-189">**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="4c482-190">**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="4c482-190">**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="4c482-191">**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="4c482-191">**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="4c482-192">**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="4c482-192">**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="4c482-193">**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="4c482-193">**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="4c482-194">**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="4c482-194">**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="4c482-195">**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="4c482-195">**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="4c482-196">**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="4c482-196">**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="4c482-197">**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="4c482-197">**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="4c482-198">**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="4c482-198">**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="4c482-199">**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="4c482-199">**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="4c482-200">**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="4c482-200">**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="4c482-201">**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="4c482-201">**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="4c482-202">**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="4c482-202">**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="4c482-203">**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="4c482-203">**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="4c482-204">**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="4c482-204">**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="4c482-205">**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="4c482-205">**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="4c482-206">**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="4c482-206">**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="4c482-207">**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="4c482-207">**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="4c482-208">**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="4c482-208">**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="4c482-209">**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="4c482-209">**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="4c482-210">**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="4c482-210">**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_NonStop_OS"></span><span id="hp_nonstop_os"></span><span id="HP_NONSTOP_OS"></span>

<span data-ttu-id="4c482-211">**Sistema operacional HP Nonstop** (33)</span><span class="sxs-lookup"><span data-stu-id="4c482-211">**HP NonStop OS** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_NonStop_OSS"></span><span id="hp_nonstop_oss"></span><span id="HP_NONSTOP_OSS"></span>

<span data-ttu-id="4c482-212">**HP Nonstop OSS** (34)</span><span class="sxs-lookup"><span data-stu-id="4c482-212">**HP NonStop OSS** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="4c482-213">**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="4c482-213">**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="4c482-214">**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="4c482-214">**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="4c482-215">**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="4c482-215">**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="4c482-216">**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="4c482-216">**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM"></span><span id="vm"></span>

<span data-ttu-id="4c482-217">**VM** (39)</span><span class="sxs-lookup"><span data-stu-id="4c482-217">**VM** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="4c482-218">**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="4c482-218">**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="4c482-219">**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="4c482-219">**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="4c482-220">**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="4c482-220">**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="4c482-221">**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="4c482-221">**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="4c482-222">**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="4c482-222">**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="4c482-223">**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="4c482-223">**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="4c482-224">**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="4c482-224">**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="4c482-225">**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="4c482-225">**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="4c482-226">**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="4c482-226">**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="4c482-227">**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="4c482-227">**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="4c482-228">**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="4c482-228">**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="4c482-229">**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="4c482-229">**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="4c482-230">**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="4c482-230">**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="4c482-231">**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="4c482-231">**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="4c482-232">**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="4c482-232">**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="4c482-233">**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="4c482-233">**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="4c482-234">**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="4c482-234">**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="4c482-235">**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="4c482-235">**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="4c482-236">**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="4c482-236">**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="4c482-237">**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="4c482-237">**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="4c482-238">**Os/390** (60)</span><span class="sxs-lookup"><span data-stu-id="4c482-238">**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="4c482-239">**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="4c482-239">**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="4c482-240">**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="4c482-240">**TPF** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows__R__Me"></span><span id="windows__r__me"></span><span id="WINDOWS__R__ME"></span>

<span data-ttu-id="4c482-241">**Windows (R) me** (63)</span><span class="sxs-lookup"><span data-stu-id="4c482-241">**Windows (R) Me** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Caldera_Open_UNIX"></span><span id="caldera_open_unix"></span><span id="CALDERA_OPEN_UNIX"></span>

<span data-ttu-id="4c482-242">**Caldera Open UNIX** (64)</span><span class="sxs-lookup"><span data-stu-id="4c482-242">**Caldera Open UNIX** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenBSD"></span><span id="openbsd"></span><span id="OPENBSD"></span>

<span data-ttu-id="4c482-243">**OpenBSD** (65)</span><span class="sxs-lookup"><span data-stu-id="4c482-243">**OpenBSD** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4c482-244">**Não aplicável** (66)</span><span class="sxs-lookup"><span data-stu-id="4c482-244">**Not Applicable** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_XP"></span><span id="windows_xp"></span><span id="WINDOWS_XP"></span>

<span data-ttu-id="4c482-245">**Windows XP** (67)</span><span class="sxs-lookup"><span data-stu-id="4c482-245">**Windows XP** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="z_OS"></span><span id="z_os"></span><span id="Z_OS"></span>

<span data-ttu-id="4c482-246">**z/os** (68)</span><span class="sxs-lookup"><span data-stu-id="4c482-246">**z/OS** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2003"></span><span id="microsoft_windows_server_2003"></span><span id="MICROSOFT_WINDOWS_SERVER_2003"></span>

<span data-ttu-id="4c482-247">**Microsoft Windows Server 2003** (69)</span><span class="sxs-lookup"><span data-stu-id="4c482-247">**Microsoft Windows Server 2003** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2003_64-Bit"></span><span id="microsoft_windows_server_2003_64-bit"></span><span id="MICROSOFT_WINDOWS_SERVER_2003_64-BIT"></span>

<span data-ttu-id="4c482-248">**Microsoft Windows Server 2003 64** bits (70)</span><span class="sxs-lookup"><span data-stu-id="4c482-248">**Microsoft Windows Server 2003 64-Bit** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_XP_64-Bit"></span><span id="windows_xp_64-bit"></span><span id="WINDOWS_XP_64-BIT"></span>

<span data-ttu-id="4c482-249">**Windows XP 64 bits** (71)</span><span class="sxs-lookup"><span data-stu-id="4c482-249">**Windows XP 64-Bit** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_XP_Embedded"></span><span id="windows_xp_embedded"></span><span id="WINDOWS_XP_EMBEDDED"></span>

<span data-ttu-id="4c482-250">**Windows XP Embedded** (72)</span><span class="sxs-lookup"><span data-stu-id="4c482-250">**Windows XP Embedded** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_Vista"></span><span id="windows_vista"></span><span id="WINDOWS_VISTA"></span>

<span data-ttu-id="4c482-251">**Windows Vista** (73)</span><span class="sxs-lookup"><span data-stu-id="4c482-251">**Windows Vista** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_Vista_64-Bit"></span><span id="windows_vista_64-bit"></span><span id="WINDOWS_VISTA_64-BIT"></span>

<span data-ttu-id="4c482-252">**Windows Vista 64** bits (74)</span><span class="sxs-lookup"><span data-stu-id="4c482-252">**Windows Vista 64-Bit** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_Embedded_for_Point_of_Service"></span><span id="windows_embedded_for_point_of_service"></span><span id="WINDOWS_EMBEDDED_FOR_POINT_OF_SERVICE"></span>

<span data-ttu-id="4c482-253">**Windows Embedded para ponto de serviço** (75)</span><span class="sxs-lookup"><span data-stu-id="4c482-253">**Windows Embedded for Point of Service** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008"></span><span id="microsoft_windows_server_2008"></span><span id="MICROSOFT_WINDOWS_SERVER_2008"></span>

<span data-ttu-id="4c482-254">**Microsoft Windows Server 2008** (76)</span><span class="sxs-lookup"><span data-stu-id="4c482-254">**Microsoft Windows Server 2008** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008_64-Bit"></span><span id="microsoft_windows_server_2008_64-bit"></span><span id="MICROSOFT_WINDOWS_SERVER_2008_64-BIT"></span>

<span data-ttu-id="4c482-255">**Microsoft Windows Server 2008 64** bits (77)</span><span class="sxs-lookup"><span data-stu-id="4c482-255">**Microsoft Windows Server 2008 64-Bit** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD_64-Bit"></span><span id="freebsd_64-bit"></span><span id="FREEBSD_64-BIT"></span>

<span data-ttu-id="4c482-256">**FreeBSD 64** bits (78)</span><span class="sxs-lookup"><span data-stu-id="4c482-256">**FreeBSD 64-Bit** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="RedHat_Enterprise_Linux"></span><span id="redhat_enterprise_linux"></span><span id="REDHAT_ENTERPRISE_LINUX"></span>

<span data-ttu-id="4c482-257">**RedHat Enterprise Linux** (79)</span><span class="sxs-lookup"><span data-stu-id="4c482-257">**RedHat Enterprise Linux** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="RedHat_Enterprise_Linux_64-Bit"></span><span id="redhat_enterprise_linux_64-bit"></span><span id="REDHAT_ENTERPRISE_LINUX_64-BIT"></span>

<span data-ttu-id="4c482-258">**RedHat Enterprise Linux 64-bit** (80)</span><span class="sxs-lookup"><span data-stu-id="4c482-258">**RedHat Enterprise Linux 64-Bit** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris_64-Bit"></span><span id="solaris_64-bit"></span><span id="SOLARIS_64-BIT"></span>

<span data-ttu-id="4c482-259">**Solaris 64** bits (81)</span><span class="sxs-lookup"><span data-stu-id="4c482-259">**Solaris 64-Bit** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="SUSE"></span><span id="suse"></span>

<span data-ttu-id="4c482-260">**SuSE** (82)</span><span class="sxs-lookup"><span data-stu-id="4c482-260">**SUSE** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="SUSE_64-Bit"></span><span id="suse_64-bit"></span><span id="SUSE_64-BIT"></span>

<span data-ttu-id="4c482-261">**SUSE 64** bits (83)</span><span class="sxs-lookup"><span data-stu-id="4c482-261">**SUSE 64-Bit** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="SLES"></span><span id="sles"></span>

<span data-ttu-id="4c482-262">**SLES** (84)</span><span class="sxs-lookup"><span data-stu-id="4c482-262">**SLES** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="SLES_64-Bit"></span><span id="sles_64-bit"></span><span id="SLES_64-BIT"></span>

<span data-ttu-id="4c482-263">**SLES 64** bits (85)</span><span class="sxs-lookup"><span data-stu-id="4c482-263">**SLES 64-Bit** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Novell_OES"></span><span id="novell_oes"></span><span id="NOVELL_OES"></span>

<span data-ttu-id="4c482-264">**Novell ta** (86)</span><span class="sxs-lookup"><span data-stu-id="4c482-264">**Novell OES** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Novell_Linux_Desktop"></span><span id="novell_linux_desktop"></span><span id="NOVELL_LINUX_DESKTOP"></span>

<span data-ttu-id="4c482-265">**Novell Linux Desktop** (87)</span><span class="sxs-lookup"><span data-stu-id="4c482-265">**Novell Linux Desktop** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Sun_Java_Desktop_System"></span><span id="sun_java_desktop_system"></span><span id="SUN_JAVA_DESKTOP_SYSTEM"></span>

<span data-ttu-id="4c482-266">**Sun Java Desktop System** (88)</span><span class="sxs-lookup"><span data-stu-id="4c482-266">**Sun Java Desktop System** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Mandriva"></span><span id="mandriva"></span><span id="MANDRIVA"></span>

<span data-ttu-id="4c482-267">**Mandriva** (89)</span><span class="sxs-lookup"><span data-stu-id="4c482-267">**Mandriva** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Mandriva_64-Bit"></span><span id="mandriva_64-bit"></span><span id="MANDRIVA_64-BIT"></span>

<span data-ttu-id="4c482-268">**Mandriva 64** bits (90)</span><span class="sxs-lookup"><span data-stu-id="4c482-268">**Mandriva 64-Bit** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="TurboLinux"></span><span id="turbolinux"></span><span id="TURBOLINUX"></span>

<span data-ttu-id="4c482-269">**Turbolinux** (91)</span><span class="sxs-lookup"><span data-stu-id="4c482-269">**TurboLinux** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="TurboLinux_64-Bit"></span><span id="turbolinux_64-bit"></span><span id="TURBOLINUX_64-BIT"></span>

<span data-ttu-id="4c482-270">**TurboLinux 64** bits (92)</span><span class="sxs-lookup"><span data-stu-id="4c482-270">**TurboLinux 64-Bit** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Ubuntu"></span><span id="ubuntu"></span><span id="UBUNTU"></span>

<span data-ttu-id="4c482-271">**Ubuntu** (93)</span><span class="sxs-lookup"><span data-stu-id="4c482-271">**Ubuntu** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Ubuntu_64-Bit"></span><span id="ubuntu_64-bit"></span><span id="UBUNTU_64-BIT"></span>

<span data-ttu-id="4c482-272">**Ubuntu 64-bit** (94)</span><span class="sxs-lookup"><span data-stu-id="4c482-272">**Ubuntu 64-Bit** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Debian"></span><span id="debian"></span><span id="DEBIAN"></span>

<span data-ttu-id="4c482-273">**Debian** (95)</span><span class="sxs-lookup"><span data-stu-id="4c482-273">**Debian** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Debian_64-Bit"></span><span id="debian_64-bit"></span><span id="DEBIAN_64-BIT"></span>

<span data-ttu-id="4c482-274">**Debian 64 bits** (96)</span><span class="sxs-lookup"><span data-stu-id="4c482-274">**Debian 64-Bit** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.4.x"></span><span id="linux_2.4.x"></span><span id="LINUX_2.4.X"></span>

<span data-ttu-id="4c482-275">**Linux 2.4. x** (97)</span><span class="sxs-lookup"><span data-stu-id="4c482-275">**Linux 2.4.x** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.4.x_64-Bit"></span><span id="linux_2.4.x_64-bit"></span><span id="LINUX_2.4.X_64-BIT"></span>

<span data-ttu-id="4c482-276">**Linux 2.4. x 64 bits** (98)</span><span class="sxs-lookup"><span data-stu-id="4c482-276">**Linux 2.4.x 64-Bit** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.6.x"></span><span id="linux_2.6.x"></span><span id="LINUX_2.6.X"></span>

<span data-ttu-id="4c482-277">**Linux 2.6. x** (99)</span><span class="sxs-lookup"><span data-stu-id="4c482-277">**Linux 2.6.x** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.6.x_64-Bit"></span><span id="linux_2.6.x_64-bit"></span><span id="LINUX_2.6.X_64-BIT"></span>

<span data-ttu-id="4c482-278">**Linux 2.6. x 64 bits** (100)</span><span class="sxs-lookup"><span data-stu-id="4c482-278">**Linux 2.6.x 64-Bit** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_64-Bit"></span><span id="linux_64-bit"></span><span id="LINUX_64-BIT"></span>

<span data-ttu-id="4c482-279">**Linux 64** bits (101)</span><span class="sxs-lookup"><span data-stu-id="4c482-279">**Linux 64-Bit** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_64-Bit"></span><span id="other_64-bit"></span><span id="OTHER_64-BIT"></span>

<span data-ttu-id="4c482-280">**Outros 64 bits** (102)</span><span class="sxs-lookup"><span data-stu-id="4c482-280">**Other 64-Bit** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008_R2"></span><span id="microsoft_windows_server_2008_r2"></span><span id="MICROSOFT_WINDOWS_SERVER_2008_R2"></span>

<span data-ttu-id="4c482-281">**Microsoft Windows Server 2008 R2** (103)</span><span class="sxs-lookup"><span data-stu-id="4c482-281">**Microsoft Windows Server 2008 R2** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="VMware_ESXi"></span><span id="vmware_esxi"></span><span id="VMWARE_ESXI"></span>

<span data-ttu-id="4c482-282">**VMware ESXi** (104)</span><span class="sxs-lookup"><span data-stu-id="4c482-282">**VMware ESXi** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_7"></span><span id="microsoft_windows_7"></span><span id="MICROSOFT_WINDOWS_7"></span>

<span data-ttu-id="4c482-283">**Microsoft Windows 7** (105)</span><span class="sxs-lookup"><span data-stu-id="4c482-283">**Microsoft Windows 7** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="CentOS_32-bit"></span><span id="centos_32-bit"></span><span id="CENTOS_32-BIT"></span>

<span data-ttu-id="4c482-284">**CentOS 32** bits (106)</span><span class="sxs-lookup"><span data-stu-id="4c482-284">**CentOS 32-bit** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="CentOS_64-bit"></span><span id="centos_64-bit"></span><span id="CENTOS_64-BIT"></span>

<span data-ttu-id="4c482-285">**CentOS 64** bits (107)</span><span class="sxs-lookup"><span data-stu-id="4c482-285">**CentOS 64-bit** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Oracle_Enterprise_Linux_32-bit"></span><span id="oracle_enterprise_linux_32-bit"></span><span id="ORACLE_ENTERPRISE_LINUX_32-BIT"></span>

<span data-ttu-id="4c482-286">**Oracle Enterprise Linux 32-bit** (108)</span><span class="sxs-lookup"><span data-stu-id="4c482-286">**Oracle Enterprise Linux 32-bit** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Oracle_Enterprise_Linux_64-bit"></span><span id="oracle_enterprise_linux_64-bit"></span><span id="ORACLE_ENTERPRISE_LINUX_64-BIT"></span>

<span data-ttu-id="4c482-287">**Oracle Enterprise Linux 64-bit** (109)</span><span class="sxs-lookup"><span data-stu-id="4c482-287">**Oracle Enterprise Linux 64-bit** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="eComStation_32-bitx"></span><span id="ecomstation_32-bitx"></span><span id="ECOMSTATION_32-BITX"></span>

<span data-ttu-id="4c482-288">**eComStation 32-bitx** (110)</span><span class="sxs-lookup"><span data-stu-id="4c482-288">**eComStation 32-bitx** (110)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4c482-289">**Versão**</span><span class="sxs-lookup"><span data-stu-id="4c482-289">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c482-290">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4c482-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c482-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c482-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c482-292">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Software de subcomponente do DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="4c482-292">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software \|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="4c482-293">A versão do software no formato *<Major>* . *<Minor>* .*<Revision>*</span><span class="sxs-lookup"><span data-stu-id="4c482-293">The software version in the format *<Major>*.*<Minor>*.*<Revision>*</span></span> <span data-ttu-id="4c482-294">ou *<Major>* . *<Minor><letter><revision>* .</span><span class="sxs-lookup"><span data-stu-id="4c482-294">or *<Major>*.*<Minor><letter><revision>*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c482-295">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c482-295">Requirements</span></span>



| <span data-ttu-id="4c482-296">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c482-296">Requirement</span></span> | <span data-ttu-id="4c482-297">Valor</span><span class="sxs-lookup"><span data-stu-id="4c482-297">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c482-298">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c482-298">Minimum supported client</span></span><br/> | <span data-ttu-id="4c482-299">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4c482-299">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4c482-300">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c482-300">Minimum supported server</span></span><br/> | <span data-ttu-id="4c482-301">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4c482-301">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4c482-302">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c482-302">Namespace</span></span><br/>                | <span data-ttu-id="4c482-303">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4c482-303">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4c482-304">MOF</span><span class="sxs-lookup"><span data-stu-id="4c482-304">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c482-305"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c482-305"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c482-306">DLL</span><span class="sxs-lookup"><span data-stu-id="4c482-306">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c482-307"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4c482-307"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4c482-308">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c482-308">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c482-309">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="4c482-309">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

