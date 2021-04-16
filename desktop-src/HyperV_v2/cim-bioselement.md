---
description: Representa o software de nível baixo que é carregado no armazenamento não volátil e usado para iniciar e configurar um sistema de computador (CIM \_ ComputerSystem).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: Classe CIM_BIOSElement (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758348"
---
# <a name="cim_bioselement-class-hyper-v-management"></a><span data-ttu-id="584d8-103">Classe CIM_BIOSElement (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="584d8-103">CIM_BIOSElement class (Hyper-V management)</span></span>

<span data-ttu-id="584d8-104">Representa o software de nível baixo que é carregado no armazenamento não volátil e usado para iniciar e configurar um sistema de computador ([**CIM \_ ComputerSystem**](cim-computersystem.md)).</span><span class="sxs-lookup"><span data-stu-id="584d8-104">Represents the low-level software that is loaded into non-volatile storage and used to start up and configure a computer system ([**CIM\_ComputerSystem**](cim-computersystem.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="584d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="584d8-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a><span data-ttu-id="584d8-106">Membros</span><span class="sxs-lookup"><span data-stu-id="584d8-106">Members</span></span>

<span data-ttu-id="584d8-107">A classe **CIM \_ bioselement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="584d8-107">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="584d8-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="584d8-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="584d8-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="584d8-109">Properties</span></span>

<span data-ttu-id="584d8-110">A classe **CIM \_ bioselement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="584d8-110">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="584d8-111">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="584d8-111">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584d8-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="584d8-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="584d8-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="584d8-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="584d8-114">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ bioselement**.**ListOfLanguages**")</span><span class="sxs-lookup"><span data-stu-id="584d8-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSElement**.**ListOfLanguages**")</span></span>
</dt> </dl>

<span data-ttu-id="584d8-115">O idioma selecionado no momento para o BIOS.</span><span class="sxs-lookup"><span data-stu-id="584d8-115">The currently selected language for the BIOS.</span></span> <span data-ttu-id="584d8-116">Essas informações podem ser obtidas no BIOS de gerenciamento do sistema (SMBIOS) usando o atributo de idioma atual da estrutura do tipo 13 para indexar na lista de cadeias de caracteres que segue a estrutura.</span><span class="sxs-lookup"><span data-stu-id="584d8-116">This information can be obtained from the System Management BIOS (SMBIOS) using the Current Language attribute of the Type 13 structure to index into the string list that follows the structure.</span></span> <span data-ttu-id="584d8-117">Essa propriedade é formatada usando o nome da linguagem ISO 639 e pode ser seguida pelo nome da região ISO 3166 e pelo método de codificação.</span><span class="sxs-lookup"><span data-stu-id="584d8-117">This property is formatted using the ISO 639 Language Name, and may be followed by the ISO 3166 Territory Name and the encoding method.</span></span>

</dd> <dt>

<span data-ttu-id="584d8-118">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="584d8-118">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584d8-119">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="584d8-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="584d8-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="584d8-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="584d8-121">Uma lista de idiomas instaláveis para o BIOS.</span><span class="sxs-lookup"><span data-stu-id="584d8-121">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="584d8-122">Essas informações podem ser obtidas no SMBIOS, na lista de cadeias de caracteres que segue a estrutura do tipo 13.</span><span class="sxs-lookup"><span data-stu-id="584d8-122">This information can be obtained from SMBIOS, from the string list that follows the Type 13 structure.</span></span> <span data-ttu-id="584d8-123">Um nome de idioma ISO 639 deve ser usado para especificar os idiomas instaláveis do BIOS.</span><span class="sxs-lookup"><span data-stu-id="584d8-123">An ISO 639 Language Name should be used to specify the BIOS' installable languages.</span></span> <span data-ttu-id="584d8-124">O nome da região ISO 3166 e o método de codificação também podem ser especificados, seguindo o nome do idioma.</span><span class="sxs-lookup"><span data-stu-id="584d8-124">The ISO 3166 Territory Name and the encoding method may also be specified, following the Language Name.</span></span>

</dd> <dt>

<span data-ttu-id="584d8-125">**LoadedEndingAddress**</span><span class="sxs-lookup"><span data-stu-id="584d8-125">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584d8-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="584d8-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="584d8-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="584d8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="584d8-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,6 ")</span><span class="sxs-lookup"><span data-stu-id="584d8-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="584d8-129">O endereço final da memória ocupada pelo BIOS.</span><span class="sxs-lookup"><span data-stu-id="584d8-129">The ending address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="584d8-130">**LoadedStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="584d8-130">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584d8-131">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="584d8-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="584d8-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="584d8-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="584d8-133">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="584d8-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="584d8-134">O endereço inicial da memória ocupada pelo BIOS.</span><span class="sxs-lookup"><span data-stu-id="584d8-134">The starting address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="584d8-135">**LoadUtilityInformation**</span><span class="sxs-lookup"><span data-stu-id="584d8-135">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584d8-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="584d8-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="584d8-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="584d8-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="584d8-138">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="584d8-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="584d8-139">Uma cadeia de caracteres de forma livre que descreve o Utilitário Flash/carregamento do BIOS necessário para atualizar o objeto **CIM \_ bioselement** .</span><span class="sxs-lookup"><span data-stu-id="584d8-139">A free form string that describes the BIOS flash/load utility that is required to update the **CIM\_BIOSElement** object.</span></span> <span data-ttu-id="584d8-140">A versão e outras informações podem ser indicadas nesta propriedade.</span><span class="sxs-lookup"><span data-stu-id="584d8-140">Version and other information may be indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="584d8-141">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="584d8-141">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584d8-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="584d8-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="584d8-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="584d8-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="584d8-144">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("fabricante"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="584d8-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="584d8-145">O fabricante do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="584d8-145">The manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="584d8-146">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="584d8-146">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584d8-147">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="584d8-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="584d8-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="584d8-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="584d8-149">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="584d8-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="584d8-150">True se este for o principal BIOS do sistema de computador; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="584d8-150">True if this is the primary BIOS of the computer system; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="584d8-151">**RegistryURIs**</span><span class="sxs-lookup"><span data-stu-id="584d8-151">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584d8-152">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="584d8-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="584d8-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="584d8-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="584d8-154">O local de publicação dos registros de atributo do BIOS para os quais a implementação do BIOS está em conformidade.</span><span class="sxs-lookup"><span data-stu-id="584d8-154">The publication location of the BIOS attribute registries to which the BIOS implementation complies.</span></span>

</dd> <dt>

<span data-ttu-id="584d8-155">**Liberado**</span><span class="sxs-lookup"><span data-stu-id="584d8-155">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584d8-156">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="584d8-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="584d8-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="584d8-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="584d8-158">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,8 ")</span><span class="sxs-lookup"><span data-stu-id="584d8-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="584d8-159">A data em que este BIOS foi lançado.</span><span class="sxs-lookup"><span data-stu-id="584d8-159">The Date on which this BIOS was released.</span></span>

</dd> <dt>

<span data-ttu-id="584d8-160">**Versão**</span><span class="sxs-lookup"><span data-stu-id="584d8-160">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="584d8-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="584d8-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="584d8-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="584d8-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="584d8-163">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="584d8-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="584d8-164">A versão da operação.</span><span class="sxs-lookup"><span data-stu-id="584d8-164">The version of the operation.</span></span> <span data-ttu-id="584d8-165">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="584d8-165">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="584d8-166">*<major>*.*<minor>*.*<revision>*</span><span class="sxs-lookup"><span data-stu-id="584d8-166">*<major>*.*<minor>*.*<revision>*</span></span>
-   <span data-ttu-id="584d8-167">*<major>*.*<minor><letter><revision>*</span><span class="sxs-lookup"><span data-stu-id="584d8-167">*<major>*.*<minor><letter><revision>*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="584d8-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="584d8-168">Requirements</span></span>



| <span data-ttu-id="584d8-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="584d8-169">Requirement</span></span> | <span data-ttu-id="584d8-170">Valor</span><span class="sxs-lookup"><span data-stu-id="584d8-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="584d8-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="584d8-171">Minimum supported client</span></span><br/> | <span data-ttu-id="584d8-172">Windows 8</span><span class="sxs-lookup"><span data-stu-id="584d8-172">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="584d8-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="584d8-173">Minimum supported server</span></span><br/> | <span data-ttu-id="584d8-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="584d8-174">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="584d8-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="584d8-175">Namespace</span></span><br/>                | <span data-ttu-id="584d8-176">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="584d8-176">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="584d8-177">MOF</span><span class="sxs-lookup"><span data-stu-id="584d8-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="584d8-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="584d8-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="584d8-179">DLL</span><span class="sxs-lookup"><span data-stu-id="584d8-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="584d8-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="584d8-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="584d8-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="584d8-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="584d8-182">**\_Software CIM**</span><span class="sxs-lookup"><span data-stu-id="584d8-182">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

