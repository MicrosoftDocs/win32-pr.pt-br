---
description: Representa os recursos do software de nível baixo que é usado para iniciar e configurar um sistema de computador.
ms.assetid: 54d03539-d908-4571-b8fd-934b972e8d84
ms.tgt_platform: multiple
title: Classe CIM_BIOSFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeature
- CIM_BIOSFeature.Caption
- CIM_BIOSFeature.Description
- CIM_BIOSFeature.InstallDate
- CIM_BIOSFeature.Status
- CIM_BIOSFeature.IdentifyingNumber
- CIM_BIOSFeature.ProductName
- CIM_BIOSFeature.Vendor
- CIM_BIOSFeature.Version
- CIM_BIOSFeature.Name
- CIM_BIOSFeature.CharacteristicDescriptions
- CIM_BIOSFeature.Characteristics
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 538dc9e4c18d976901519ae0e2d6f5249fd25c35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826538"
---
# <a name="cim_biosfeature-class"></a><span data-ttu-id="8eef0-103">\_Classe CIM BIOSFeature</span><span class="sxs-lookup"><span data-stu-id="8eef0-103">CIM\_BIOSFeature class</span></span>

<span data-ttu-id="8eef0-104">A classe **CIM \_ BIOSFeature** representa os recursos do software de nível baixo que é usado para iniciar e configurar um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="8eef0-104">The **CIM\_BIOSFeature** class represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8eef0-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="8eef0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8eef0-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8eef0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8eef0-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8eef0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8eef0-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8eef0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eef0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8eef0-109">Syntax</span></span>

``` syntax
[UUID("{7D33100E-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   IdentifyingNumber;
  string   ProductName;
  string   Vendor;
  string   Version;
  string   Name;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="8eef0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="8eef0-110">Members</span></span>

<span data-ttu-id="8eef0-111">A classe **CIM \_ BIOSFeature** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8eef0-111">The **CIM\_BIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="8eef0-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8eef0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8eef0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8eef0-113">Properties</span></span>

<span data-ttu-id="8eef0-114">A classe **CIM \_ BIOSFeature** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8eef0-114">The **CIM\_BIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8eef0-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8eef0-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eef0-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8eef0-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8eef0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8eef0-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8eef0-119">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8eef0-119">A short textual description of the object.</span></span>

<span data-ttu-id="8eef0-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8eef0-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eef0-121">**CharacteristicDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8eef0-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eef0-122">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8eef0-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8eef0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-124">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Característica do BIOS \| de DMTF 3,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**.**Características**")</span><span class="sxs-lookup"><span data-stu-id="8eef0-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="8eef0-125">Matriz de cadeias de caracteres de forma livre que fornece explicações detalhadas dos recursos do BIOS indicados na matriz **características** .</span><span class="sxs-lookup"><span data-stu-id="8eef0-125">Array of free-form strings that provides detailed explanations of the BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="8eef0-126">Cada entrada nessa matriz está relacionada à entrada na matriz de **características** , que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="8eef0-126">Each entry in this array is related to the entry in the **Characteristics** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="8eef0-127">**Características**</span><span class="sxs-lookup"><span data-stu-id="8eef0-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eef0-128">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8eef0-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8eef0-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-130">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Característica do BIOS \| de DMTF 3,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**.**CharacteristicDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="8eef0-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="8eef0-131">Matriz de inteiros que especifica os recursos com suporte no BIOS.</span><span class="sxs-lookup"><span data-stu-id="8eef0-131">Array of integers that specifies the features supported by the BIOS.</span></span> <span data-ttu-id="8eef0-132">O valor 3 não é válido no esquema CIM porque ele representa que não há suporte para nenhum recurso do BIOS no DMI.</span><span class="sxs-lookup"><span data-stu-id="8eef0-132">The value 3 is not valid in the CIM schema because it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="8eef0-133">Nesse caso, esse objeto não deve ser instanciado.</span><span class="sxs-lookup"><span data-stu-id="8eef0-133">In which case, this object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8eef0-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8eef0-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-135">Outros.</span><span class="sxs-lookup"><span data-stu-id="8eef0-135">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8eef0-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="8eef0-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-137">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="8eef0-137">Unknown.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="8eef0-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (3)</span><span class="sxs-lookup"><span data-stu-id="8eef0-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-139">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="8eef0-139">Undefined.</span></span>

</dd> <dt>

<span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>

<span data-ttu-id="8eef0-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**Suporte ao ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="8eef0-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**ISA Support** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-141">Suporte a ISA.</span><span class="sxs-lookup"><span data-stu-id="8eef0-141">ISA support.</span></span>

</dd> <dt>

<span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>

<span data-ttu-id="8eef0-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**Suporte a MCA** (5)</span><span class="sxs-lookup"><span data-stu-id="8eef0-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**MCA Support** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-143">Suporte a MCA.</span><span class="sxs-lookup"><span data-stu-id="8eef0-143">MCA support.</span></span>

</dd> <dt>

<span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>

<span data-ttu-id="8eef0-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**Suporte a EISA** (6)</span><span class="sxs-lookup"><span data-stu-id="8eef0-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**EISA Support** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-145">Suporte a EISA.</span><span class="sxs-lookup"><span data-stu-id="8eef0-145">EISA support.</span></span>

</dd> <dt>

<span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>

<span data-ttu-id="8eef0-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**Suporte a PCI** (7)</span><span class="sxs-lookup"><span data-stu-id="8eef0-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**PCI Support** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-147">Suporte a PCI.</span><span class="sxs-lookup"><span data-stu-id="8eef0-147">PCI support.</span></span>

</dd> <dt>

<span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>

<span data-ttu-id="8eef0-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**Suporte a PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="8eef0-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**PCMCIA Support** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-149">Suporte a PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="8eef0-149">PCMCIA support.</span></span>

</dd> <dt>

<span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>

<span data-ttu-id="8eef0-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**Suporte a PNP** (9)</span><span class="sxs-lookup"><span data-stu-id="8eef0-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**PnP Support** (9)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-151">Suporte a PnP.</span><span class="sxs-lookup"><span data-stu-id="8eef0-151">PnP support.</span></span>

</dd> <dt>

<span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>

<span data-ttu-id="8eef0-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**Suporte a APM** (10)</span><span class="sxs-lookup"><span data-stu-id="8eef0-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**APM Support** (10)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-153">Suporte a APM.</span><span class="sxs-lookup"><span data-stu-id="8eef0-153">APM support.</span></span>

</dd> <dt>

<span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>

<span data-ttu-id="8eef0-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**BIOS atualizável** (11)</span><span class="sxs-lookup"><span data-stu-id="8eef0-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**Upgradeable BIOS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-155">BIOS atualizável.</span><span class="sxs-lookup"><span data-stu-id="8eef0-155">Upgradeable BIOS.</span></span>

</dd> <dt>

<span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="8eef0-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**Sombra do BIOS permitida** (12)</span><span class="sxs-lookup"><span data-stu-id="8eef0-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**BIOS Shadowing Allowed** (12)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-157">Sombra do BIOS permitida.</span><span class="sxs-lookup"><span data-stu-id="8eef0-157">BIOS shadowing allowed.</span></span>

</dd> <dt>

<span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>

<span data-ttu-id="8eef0-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**Suporte a VL VESA** (13)</span><span class="sxs-lookup"><span data-stu-id="8eef0-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**VL VESA Support** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-159">Suporte a VL VESA.</span><span class="sxs-lookup"><span data-stu-id="8eef0-159">VL VESA support.</span></span>

</dd> <dt>

<span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>

<span data-ttu-id="8eef0-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**Suporte a ESCD** (14)</span><span class="sxs-lookup"><span data-stu-id="8eef0-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**ESCD Support** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-161">Suporte a ESCD.</span><span class="sxs-lookup"><span data-stu-id="8eef0-161">ESCD support.</span></span>

</dd> <dt>

<span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>

<span data-ttu-id="8eef0-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**Suporte a LS-120** (15)</span><span class="sxs-lookup"><span data-stu-id="8eef0-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**LS-120 Support** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-163">Suporte a LS-120.</span><span class="sxs-lookup"><span data-stu-id="8eef0-163">LS-120 support.</span></span>

</dd> <dt>

<span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>

<span data-ttu-id="8eef0-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**Suporte a ACPI** (16)</span><span class="sxs-lookup"><span data-stu-id="8eef0-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**ACPI Support** (16)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-165">Suporte a ACPI.</span><span class="sxs-lookup"><span data-stu-id="8eef0-165">ACPI support.</span></span>

</dd> <dt>

<span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>

<span data-ttu-id="8eef0-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**Suporte à inicialização I2O** (17)</span><span class="sxs-lookup"><span data-stu-id="8eef0-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**I2O Boot Support** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-167">Suporte à inicialização I2O.</span><span class="sxs-lookup"><span data-stu-id="8eef0-167">I2O boot support.</span></span>

</dd> <dt>

<span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>

<span data-ttu-id="8eef0-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**Suporte a USB herdado** (18)</span><span class="sxs-lookup"><span data-stu-id="8eef0-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**USB Legacy Support** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-169">Suporte a USB herdado.</span><span class="sxs-lookup"><span data-stu-id="8eef0-169">USB legacy support.</span></span>

</dd> <dt>

<span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>

<span data-ttu-id="8eef0-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**Suporte a AGP** (19)</span><span class="sxs-lookup"><span data-stu-id="8eef0-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**AGP Support** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-171">Suporte a AGP.</span><span class="sxs-lookup"><span data-stu-id="8eef0-171">AGP support.</span></span>

</dd> <dt>

<span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>

<span data-ttu-id="8eef0-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**Placa de PC** (20)</span><span class="sxs-lookup"><span data-stu-id="8eef0-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**PC Card** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-173">Placa de PC.</span><span class="sxs-lookup"><span data-stu-id="8eef0-173">PC card.</span></span>

</dd> <dt>

<span id="IR"></span><span id="ir"></span>

<span data-ttu-id="8eef0-174"><span id="IR"></span><span id="ir"></span>**Ir** (21)</span><span class="sxs-lookup"><span data-stu-id="8eef0-174"><span id="IR"></span><span id="ir"></span>**IR** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-175">Receptor.</span><span class="sxs-lookup"><span data-stu-id="8eef0-175">IR.</span></span>

</dd> <dt>

<span id="1394"></span>

<span data-ttu-id="8eef0-176"><span id="1394"></span>**1394** (22)</span><span class="sxs-lookup"><span data-stu-id="8eef0-176"><span id="1394"></span>**1394** (22)</span></span>


</dt> <dd>

1394.

</dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="8eef0-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span><span class="sxs-lookup"><span data-stu-id="8eef0-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-178">I2C.</span><span class="sxs-lookup"><span data-stu-id="8eef0-178">I2C.</span></span>

</dd> <dt>

<span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>

<span data-ttu-id="8eef0-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Bateria inteligente** (24)</span><span class="sxs-lookup"><span data-stu-id="8eef0-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Smart Battery** (24)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-180">Bateria inteligente.</span><span class="sxs-lookup"><span data-stu-id="8eef0-180">Smart battery.</span></span>

</dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="8eef0-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="8eef0-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>


</dt> <dd>

<span data-ttu-id="8eef0-182">PC-98.</span><span class="sxs-lookup"><span data-stu-id="8eef0-182">PC-98.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8eef0-183">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8eef0-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eef0-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8eef0-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8eef0-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-186">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="8eef0-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8eef0-187">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8eef0-187">A textual description of the object.</span></span>

<span data-ttu-id="8eef0-188">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8eef0-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eef0-189">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="8eef0-189">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eef0-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8eef0-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8eef0-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-192">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="8eef0-192">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="8eef0-193">Identificação do produto, como um número de série no software ou um número de chip em um chip de hardware.</span><span class="sxs-lookup"><span data-stu-id="8eef0-193">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

<span data-ttu-id="8eef0-194">Essa propriedade é herdada do [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="8eef0-194">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eef0-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8eef0-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eef0-196">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8eef0-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8eef0-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-198">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="8eef0-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8eef0-199">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="8eef0-199">Indicates when the object was installed.</span></span> <span data-ttu-id="8eef0-200">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="8eef0-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8eef0-201">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8eef0-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eef0-202">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8eef0-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eef0-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8eef0-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8eef0-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-205">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8eef0-205">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8eef0-206">A propriedade Name define o rótulo pelo qual o objeto é conhecido pelo mundo fora do sistema de processamento de dados.</span><span class="sxs-lookup"><span data-stu-id="8eef0-206">The Name property defines the label by which the object is known to the world outside the data processing system.</span></span> <span data-ttu-id="8eef0-207">Esse rótulo é um nome legível que identifica exclusivamente o elemento no contexto do namespace do elemento.</span><span class="sxs-lookup"><span data-stu-id="8eef0-207">This label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="8eef0-208">Essa propriedade é herdada do [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="8eef0-208">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eef0-209">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="8eef0-209">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eef0-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8eef0-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8eef0-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-212">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="8eef0-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="8eef0-213">Nome do produto usado normalmente.</span><span class="sxs-lookup"><span data-stu-id="8eef0-213">Commonly used product name.</span></span>

<span data-ttu-id="8eef0-214">Essa propriedade é herdada do [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="8eef0-214">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eef0-215">**Status**</span><span class="sxs-lookup"><span data-stu-id="8eef0-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eef0-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8eef0-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8eef0-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-218">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="8eef0-218">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8eef0-219">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8eef0-219">String that indicates the current status of the object.</span></span> <span data-ttu-id="8eef0-220">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="8eef0-220">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8eef0-221">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="8eef0-221">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8eef0-222">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="8eef0-222">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8eef0-223">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="8eef0-223">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8eef0-224">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="8eef0-224">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8eef0-225">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="8eef0-225">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8eef0-226">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8eef0-226">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8eef0-227">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8eef0-227">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8eef0-228">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8eef0-228">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8eef0-229">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="8eef0-229">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8eef0-230">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="8eef0-230">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8eef0-231">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="8eef0-231">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8eef0-232">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8eef0-232">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8eef0-233">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="8eef0-233">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8eef0-234">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="8eef0-234">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8eef0-235">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="8eef0-235">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8eef0-236">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="8eef0-236">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8eef0-237">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="8eef0-237">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8eef0-238">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="8eef0-238">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8eef0-239">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="8eef0-239">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8eef0-240">**Fornecedor**</span><span class="sxs-lookup"><span data-stu-id="8eef0-240">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eef0-241">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8eef0-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8eef0-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-243">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**Vendor**") [**, \_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="8eef0-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="8eef0-244">Nome do fornecedor do produto, que corresponde à propriedade **Vendor** no objeto Product do padrão de troca de solução DMTF.</span><span class="sxs-lookup"><span data-stu-id="8eef0-244">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="8eef0-245">Essa propriedade é herdada do [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="8eef0-245">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eef0-246">**Versão**</span><span class="sxs-lookup"><span data-stu-id="8eef0-246">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8eef0-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8eef0-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8eef0-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8eef0-249">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="8eef0-249">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="8eef0-250">Informações de versão do produto, que corresponde à propriedade **version** no objeto Product do padrão de troca de solução DMTF.</span><span class="sxs-lookup"><span data-stu-id="8eef0-250">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="8eef0-251">Essa propriedade é herdada do [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="8eef0-251">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8eef0-252">Comentários</span><span class="sxs-lookup"><span data-stu-id="8eef0-252">Remarks</span></span>

<span data-ttu-id="8eef0-253">A classe **CIM \_ BIOSFeature** é derivada de [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="8eef0-253">The **CIM\_BIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="8eef0-254">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="8eef0-254">WMI does not implement this class.</span></span>

<span data-ttu-id="8eef0-255">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="8eef0-255">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8eef0-256">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="8eef0-256">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eef0-257">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eef0-257">Requirements</span></span>



| <span data-ttu-id="8eef0-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eef0-258">Requirement</span></span> | <span data-ttu-id="8eef0-259">Valor</span><span class="sxs-lookup"><span data-stu-id="8eef0-259">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8eef0-260">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eef0-260">Minimum supported client</span></span><br/> | <span data-ttu-id="8eef0-261">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8eef0-261">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8eef0-262">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eef0-262">Minimum supported server</span></span><br/> | <span data-ttu-id="8eef0-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8eef0-263">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8eef0-264">Namespace</span><span class="sxs-lookup"><span data-stu-id="8eef0-264">Namespace</span></span><br/>                | <span data-ttu-id="8eef0-265">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8eef0-265">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8eef0-266">MOF</span><span class="sxs-lookup"><span data-stu-id="8eef0-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8eef0-267"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8eef0-267"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8eef0-268">DLL</span><span class="sxs-lookup"><span data-stu-id="8eef0-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eef0-269"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eef0-269"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eef0-270">Confira também</span><span class="sxs-lookup"><span data-stu-id="8eef0-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eef0-271">**\_SOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="8eef0-271">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

