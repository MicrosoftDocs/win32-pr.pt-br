---
description: A \_ classe CIM VideoBIOSFeature representa os recursos do software de baixo nível usado para configurar e acessar o controlador de vídeo de um sistema de computador e exibir o.
ms.assetid: a12ca387-5b12-487f-84fd-381afe266338
ms.tgt_platform: multiple
title: Classe CIM_VideoBIOSFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeature
- CIM_VideoBIOSFeature.Caption
- CIM_VideoBIOSFeature.CharacteristicDescriptions
- CIM_VideoBIOSFeature.Characteristics
- CIM_VideoBIOSFeature.Description
- CIM_VideoBIOSFeature.IdentifyingNumber
- CIM_VideoBIOSFeature.InstallDate
- CIM_VideoBIOSFeature.Name
- CIM_VideoBIOSFeature.ProductName
- CIM_VideoBIOSFeature.Status
- CIM_VideoBIOSFeature.Vendor
- CIM_VideoBIOSFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45f9fd2feabdcd1f9e650e7e7a913a394e8ef67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769051"
---
# <a name="cim_videobiosfeature-class"></a><span data-ttu-id="58f66-103">\_Classe CIM VideoBIOSFeature</span><span class="sxs-lookup"><span data-stu-id="58f66-103">CIM\_VideoBIOSFeature class</span></span>

<span data-ttu-id="58f66-104">A classe **CIM \_ VideoBIOSFeature** representa os recursos do software de baixo nível usado para configurar e acessar o controlador de vídeo de um sistema de computador e exibir o.</span><span class="sxs-lookup"><span data-stu-id="58f66-104">The **CIM\_VideoBIOSFeature** class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58f66-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="58f66-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="58f66-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="58f66-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="58f66-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="58f66-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="58f66-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="58f66-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f66-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58f66-109">Syntax</span></span>

``` syntax
[UUID("{BAE20634-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="58f66-110">Membros</span><span class="sxs-lookup"><span data-stu-id="58f66-110">Members</span></span>

<span data-ttu-id="58f66-111">A classe **CIM \_ VideoBIOSFeature** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="58f66-111">The **CIM\_VideoBIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="58f66-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58f66-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58f66-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58f66-113">Properties</span></span>

<span data-ttu-id="58f66-114">A classe **CIM \_ VideoBIOSFeature** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="58f66-114">The **CIM\_VideoBIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58f66-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="58f66-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f66-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58f66-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f66-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58f66-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f66-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="58f66-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="58f66-119">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="58f66-119">Short textual description of the object.</span></span>

<span data-ttu-id="58f66-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="58f66-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58f66-121">**CharacteristicDescriptions**</span><span class="sxs-lookup"><span data-stu-id="58f66-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f66-122">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58f66-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="58f66-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58f66-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f66-124">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. A \| característica do BIOS \| de vídeo DMTF 1,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**.**Características**")</span><span class="sxs-lookup"><span data-stu-id="58f66-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="58f66-125">Cadeias de caracteres de forma livre que fornecem descrições detalhadas para os recursos do BIOS de vídeo indicados na matriz de **características** .</span><span class="sxs-lookup"><span data-stu-id="58f66-125">Free-form strings that provide detailed descriptions for the video BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="58f66-126">Cada entrada dessa matriz está relacionada à entrada na matriz de **características** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="58f66-126">Each entry of this array is related to the entry in the **Characteristics** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="58f66-127">**Características**</span><span class="sxs-lookup"><span data-stu-id="58f66-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f66-128">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58f66-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="58f66-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58f66-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f66-130">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. A \| característica do BIOS \| de vídeo DMTF 1,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**.**CharacteristicDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="58f66-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="58f66-131">Recursos com suporte no BIOS de vídeo.</span><span class="sxs-lookup"><span data-stu-id="58f66-131">Features supported by the video BIOS.</span></span> <span data-ttu-id="58f66-132">Por exemplo, o suporte para o gerenciamento de energia VESA ou sombra de BIOS de vídeo pode ser indicado.</span><span class="sxs-lookup"><span data-stu-id="58f66-132">For example, support for VESA power management or video BIOS shadowing could be indicated.</span></span> <span data-ttu-id="58f66-133">O valor 3 ("Unknown") não é válido no esquema CIM, pois ele representa que não há suporte para nenhum recurso do BIOS no DMI.</span><span class="sxs-lookup"><span data-stu-id="58f66-133">The value 3 ("Unknown") is not valid in the CIM schema since it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="58f66-134">Nesse caso, o objeto não deve ser instanciado.</span><span class="sxs-lookup"><span data-stu-id="58f66-134">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="58f66-135">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="58f66-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="58f66-136">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="58f66-136">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="58f66-137">**Indefinido** (3)</span><span class="sxs-lookup"><span data-stu-id="58f66-137">**Undefined** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Video_BIOS"></span><span id="standard_video_bios"></span><span id="STANDARD_VIDEO_BIOS"></span>

<span data-ttu-id="58f66-138">**BIOS de vídeo padrão** (4)</span><span class="sxs-lookup"><span data-stu-id="58f66-138">**Standard Video BIOS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_BIOS_Extensions_Supported"></span><span id="vesa_bios_extensions_supported"></span><span id="VESA_BIOS_EXTENSIONS_SUPPORTED"></span>

<span data-ttu-id="58f66-139">**Extensões de BIOS VESA com suporte** (5)</span><span class="sxs-lookup"><span data-stu-id="58f66-139">**VESA BIOS Extensions Supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Power_Management_Supported"></span><span id="vesa_power_management_supported"></span><span id="VESA_POWER_MANAGEMENT_SUPPORTED"></span>

<span data-ttu-id="58f66-140">**Suporte a VESA Power Management** (6)</span><span class="sxs-lookup"><span data-stu-id="58f66-140">**VESA Power Management Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Display_Data_Channel_Supported"></span><span id="vesa_display_data_channel_supported"></span><span id="VESA_DISPLAY_DATA_CHANNEL_SUPPORTED"></span>

<span data-ttu-id="58f66-141">**Canal de dados de exibição VESA com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="58f66-141">**VESA Display Data Channel Supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Shadowing_Allowed"></span><span id="video_bios_shadowing_allowed"></span><span id="VIDEO_BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="58f66-142">**Sombreamento de BIOS de vídeo permitido** (8)</span><span class="sxs-lookup"><span data-stu-id="58f66-142">**Video BIOS Shadowing Allowed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Upgradeable"></span><span id="video_bios_upgradeable"></span><span id="VIDEO_BIOS_UPGRADEABLE"></span>

<span data-ttu-id="58f66-143">**BIOS de vídeo atualizável** (9)</span><span class="sxs-lookup"><span data-stu-id="58f66-143">**Video BIOS Upgradeable** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="58f66-144">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="58f66-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f66-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58f66-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f66-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58f66-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f66-147">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="58f66-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="58f66-148">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="58f66-148">Textual description of the object.</span></span>

<span data-ttu-id="58f66-149">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="58f66-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58f66-150">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="58f66-150">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f66-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58f66-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f66-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58f66-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f66-153">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="58f66-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="58f66-154">Identificação do produto, como um número de série no software ou um número de chip em um chip de hardware.</span><span class="sxs-lookup"><span data-stu-id="58f66-154">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span> <span data-ttu-id="58f66-155">Essa propriedade é herdada do [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="58f66-155">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="58f66-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="58f66-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f66-157">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="58f66-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="58f66-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58f66-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f66-159">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="58f66-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="58f66-160">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="58f66-160">Date and time the object was installed.</span></span> <span data-ttu-id="58f66-161">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="58f66-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="58f66-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="58f66-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58f66-163">**Nome**</span><span class="sxs-lookup"><span data-stu-id="58f66-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f66-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58f66-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f66-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58f66-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f66-166">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="58f66-166">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="58f66-167">Rótulo pelo qual o objeto é conhecido fora do sistema de processamento de dados.</span><span class="sxs-lookup"><span data-stu-id="58f66-167">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="58f66-168">Esse rótulo é um nome que identifica exclusivamente o elemento no contexto do namespace do elemento.</span><span class="sxs-lookup"><span data-stu-id="58f66-168">This label is a name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="58f66-169">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="58f66-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="58f66-170">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="58f66-170">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f66-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58f66-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f66-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58f66-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f66-173">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="58f66-173">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="58f66-174">Nome do produto usado normalmente.</span><span class="sxs-lookup"><span data-stu-id="58f66-174">Commonly used product name.</span></span>

<span data-ttu-id="58f66-175">Essa propriedade é herdada do [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="58f66-175">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="58f66-176">**Status**</span><span class="sxs-lookup"><span data-stu-id="58f66-176">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f66-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58f66-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f66-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58f66-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f66-179">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="58f66-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="58f66-180">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="58f66-180">Current status of the object.</span></span> <span data-ttu-id="58f66-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="58f66-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="58f66-182">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="58f66-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="58f66-183">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="58f66-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="58f66-184">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="58f66-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="58f66-185">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="58f66-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="58f66-186">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="58f66-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="58f66-187">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="58f66-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="58f66-188">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="58f66-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="58f66-189">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="58f66-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="58f66-190">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="58f66-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="58f66-191">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="58f66-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="58f66-192">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="58f66-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="58f66-193">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="58f66-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="58f66-194">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="58f66-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="58f66-195">**Fornecedor**</span><span class="sxs-lookup"><span data-stu-id="58f66-195">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f66-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58f66-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f66-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58f66-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f66-198">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**Vendor**") [**, \_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="58f66-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="58f66-199">Nome do fornecedor do produto, que corresponde à propriedade **Vendor** no objeto Product do padrão de intercâmbio de soluções DMTF (SES).</span><span class="sxs-lookup"><span data-stu-id="58f66-199">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard (SES).</span></span>

<span data-ttu-id="58f66-200">Essa propriedade é herdada do [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="58f66-200">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="58f66-201">**Versão**</span><span class="sxs-lookup"><span data-stu-id="58f66-201">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f66-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58f66-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58f66-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58f66-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f66-204">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="58f66-204">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="58f66-205">Informações de versão do produto, que corresponde à propriedade **version** no objeto Product do ses do DMTF.</span><span class="sxs-lookup"><span data-stu-id="58f66-205">Product version information, which corresponds to the **Version** property in the product object of the DMTF SES.</span></span>

<span data-ttu-id="58f66-206">Essa propriedade é herdada do [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="58f66-206">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58f66-207">Comentários</span><span class="sxs-lookup"><span data-stu-id="58f66-207">Remarks</span></span>

<span data-ttu-id="58f66-208">A classe **CIM \_ VideoBIOSFeature** é derivada de [**\_ SoftwareFeature CIM**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="58f66-208">The **CIM\_VideoBIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="58f66-209">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="58f66-209">WMI does not implement this class.</span></span>

<span data-ttu-id="58f66-210">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="58f66-210">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="58f66-211">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="58f66-211">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="58f66-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58f66-212">Requirements</span></span>



| <span data-ttu-id="58f66-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="58f66-213">Requirement</span></span> | <span data-ttu-id="58f66-214">Valor</span><span class="sxs-lookup"><span data-stu-id="58f66-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58f66-215">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58f66-215">Minimum supported client</span></span><br/> | <span data-ttu-id="58f66-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58f66-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58f66-217">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58f66-217">Minimum supported server</span></span><br/> | <span data-ttu-id="58f66-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58f66-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58f66-219">Namespace</span><span class="sxs-lookup"><span data-stu-id="58f66-219">Namespace</span></span><br/>                | <span data-ttu-id="58f66-220">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="58f66-220">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58f66-221">MOF</span><span class="sxs-lookup"><span data-stu-id="58f66-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58f66-222"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58f66-222"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58f66-223">DLL</span><span class="sxs-lookup"><span data-stu-id="58f66-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58f66-224"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58f66-224"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58f66-225">Confira também</span><span class="sxs-lookup"><span data-stu-id="58f66-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f66-226">**\_SOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="58f66-226">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

