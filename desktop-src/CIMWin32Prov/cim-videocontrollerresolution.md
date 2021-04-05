---
description: A \_ classe CIM VideoControllerResolution representa os vários modos de vídeo aos quais um controlador de vídeo pode dar suporte.
ms.assetid: 954ac3fe-9777-460c-8929-853f19379256
ms.tgt_platform: multiple
title: Classe CIM_VideoControllerResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoControllerResolution
- CIM_VideoControllerResolution.Caption
- CIM_VideoControllerResolution.Description
- CIM_VideoControllerResolution.SettingID
- CIM_VideoControllerResolution.HorizontalResolution
- CIM_VideoControllerResolution.MaxRefreshRate
- CIM_VideoControllerResolution.MinRefreshRate
- CIM_VideoControllerResolution.NumberOfColors
- CIM_VideoControllerResolution.RefreshRate
- CIM_VideoControllerResolution.ScanMode
- CIM_VideoControllerResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d448d92d79163bc6a4e1056e88434081c5878159
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826671"
---
# <a name="cim_videocontrollerresolution-class"></a><span data-ttu-id="6e906-103">\_Classe CIM VideoControllerResolution</span><span class="sxs-lookup"><span data-stu-id="6e906-103">CIM\_VideoControllerResolution class</span></span>

<span data-ttu-id="6e906-104">A classe **CIM \_ VideoControllerResolution** representa os vários modos de vídeo aos quais um controlador de vídeo pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="6e906-104">The **CIM\_VideoControllerResolution** class represents the various video modes that a video controller can support.</span></span> <span data-ttu-id="6e906-105">Os modos de vídeo são definidos pelas possíveis resoluções horizontais e verticais, taxa de atualização, modo de verificação e número de configurações de cores com suporte em um controlador.</span><span class="sxs-lookup"><span data-stu-id="6e906-105">Video modes are defined by the possible horizontal and vertical resolutions, refresh rate, scan mode, and number of color settings supported by a controller.</span></span> <span data-ttu-id="6e906-106">As resoluções reais em uso são os valores especificados no objeto [**CIM \_ VideoController**](cim-videocontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="6e906-106">The actual resolutions in use are the values specified in the [**CIM\_VideoController**](cim-videocontroller.md) object.</span></span>

<span data-ttu-id="6e906-107">O hardware que não é compatível com o Windows Display Driver Model (WDDM) retorna valores de propriedade imprecisos para instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="6e906-107">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e906-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="6e906-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6e906-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6e906-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6e906-110">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6e906-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6e906-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6e906-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e906-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e906-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEA-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoControllerResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint64 NumberOfColors;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="6e906-113">Membros</span><span class="sxs-lookup"><span data-stu-id="6e906-113">Members</span></span>

<span data-ttu-id="6e906-114">A classe **CIM \_ VideoControllerResolution** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6e906-114">The **CIM\_VideoControllerResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="6e906-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6e906-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e906-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6e906-116">Properties</span></span>

<span data-ttu-id="6e906-117">A classe **CIM \_ VideoControllerResolution** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6e906-117">The **CIM\_VideoControllerResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e906-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6e906-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e906-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6e906-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e906-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e906-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e906-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6e906-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6e906-122">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="6e906-122">Short textual description of the current object.</span></span>

<span data-ttu-id="6e906-123">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="6e906-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e906-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6e906-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e906-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6e906-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e906-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e906-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e906-127">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="6e906-127">Textual description of the current object.</span></span>

<span data-ttu-id="6e906-128">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="6e906-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="6e906-129">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="6e906-129">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e906-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e906-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e906-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e906-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e906-132">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de \| Monitor \| de DMTF 2,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="6e906-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="6e906-133">Resolução horizontal, em pixels.</span><span class="sxs-lookup"><span data-stu-id="6e906-133">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6e906-134">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="6e906-134">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e906-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e906-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e906-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e906-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e906-137">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de monitor de DMTF \| \| 2,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="6e906-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="6e906-138">Taxa máxima de atualização quando há suporte para um intervalo de taxas nas resoluções especificadas, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="6e906-138">Maximum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="6e906-139">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="6e906-139">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e906-140">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e906-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e906-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e906-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e906-142">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de monitor de DMTF \| \| 2,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="6e906-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="6e906-143">Taxa mínima de atualização quando há suporte para um intervalo de taxas nas resoluções especificadas, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="6e906-143">Minimum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="6e906-144">**NumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="6e906-144">**NumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e906-145">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6e906-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6e906-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e906-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e906-147">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")</span><span class="sxs-lookup"><span data-stu-id="6e906-147">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")</span></span>
</dt> </dl>

<span data-ttu-id="6e906-148">Número de cores com suporte na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="6e906-148">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="6e906-149">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6e906-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6e906-150">**Taxa_de_atualização**</span><span class="sxs-lookup"><span data-stu-id="6e906-150">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e906-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e906-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e906-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e906-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e906-153">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de monitor de DMTF \| \| 2,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="6e906-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="6e906-154">Taxa de atualização, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="6e906-154">Refresh rate, in hertz.</span></span> <span data-ttu-id="6e906-155">Se houver suporte para um intervalo de taxas, use as propriedades **MinRefreshRate** e **MaxRefreshRate** e defina essa propriedade como 0.</span><span class="sxs-lookup"><span data-stu-id="6e906-155">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="6e906-156">**Scanmode**</span><span class="sxs-lookup"><span data-stu-id="6e906-156">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e906-157">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e906-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e906-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e906-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e906-159">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de monitor de DMTF \| \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="6e906-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="6e906-160">Modo de verificação no qual o controlador Opera.</span><span class="sxs-lookup"><span data-stu-id="6e906-160">Scan mode at which the controller operates.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6e906-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="6e906-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e906-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="6e906-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6e906-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (3)</span><span class="sxs-lookup"><span data-stu-id="6e906-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="6e906-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Operação não entrelaçada** (4)</span><span class="sxs-lookup"><span data-stu-id="6e906-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6e906-165">Operação não entrelaçada</span><span class="sxs-lookup"><span data-stu-id="6e906-165">Noninterlaced operation</span></span>

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="6e906-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Operação entrelaçada** (5)</span><span class="sxs-lookup"><span data-stu-id="6e906-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6e906-167">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="6e906-167">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e906-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6e906-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e906-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e906-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e906-170">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuraid"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6e906-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6e906-171">Uma ID que serve como parte da chave para a instância atual.</span><span class="sxs-lookup"><span data-stu-id="6e906-171">An ID that serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="6e906-172">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="6e906-172">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e906-173">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e906-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e906-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e906-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e906-175">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de \| Monitor \| de DMTF 2,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="6e906-175">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="6e906-176">Resolução vertical do controlador, em pixels.</span><span class="sxs-lookup"><span data-stu-id="6e906-176">Controller's vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e906-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e906-177">Remarks</span></span>

<span data-ttu-id="6e906-178">O WMI implementa a classe **CIM \_ VideoControllerResolution** .</span><span class="sxs-lookup"><span data-stu-id="6e906-178">WMI implements the **CIM\_VideoControllerResolution** class.</span></span> <span data-ttu-id="6e906-179">A classe **CIM \_ VideoControllerResolution** é uma classe dinâmica.</span><span class="sxs-lookup"><span data-stu-id="6e906-179">The **CIM\_VideoControllerResolution** class is a dynamic class.</span></span>

<span data-ttu-id="6e906-180">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="6e906-180">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6e906-181">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="6e906-181">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="6e906-182">Observe que essa classe é uma classe base.</span><span class="sxs-lookup"><span data-stu-id="6e906-182">Note that this class is a base class.</span></span> <span data-ttu-id="6e906-183">Se você estiver tentando acessar o seu controlador de vídeo por meio do WMI, talvez queira usar o [**Win32 \_ VideoController**](win32-videocontroller.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6e906-183">If you are attempting to access your video controller through WMI, you may wish to use [**Win32\_VideoController**](win32-videocontroller.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e906-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e906-184">Requirements</span></span>



| <span data-ttu-id="6e906-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e906-185">Requirement</span></span> | <span data-ttu-id="6e906-186">Valor</span><span class="sxs-lookup"><span data-stu-id="6e906-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e906-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e906-187">Minimum supported client</span></span><br/> | <span data-ttu-id="6e906-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e906-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e906-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e906-189">Minimum supported server</span></span><br/> | <span data-ttu-id="6e906-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e906-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e906-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e906-191">Namespace</span></span><br/>                | <span data-ttu-id="6e906-192">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6e906-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6e906-193">MOF</span><span class="sxs-lookup"><span data-stu-id="6e906-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e906-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e906-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e906-195">DLL</span><span class="sxs-lookup"><span data-stu-id="6e906-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e906-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e906-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e906-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e906-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e906-198">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="6e906-198">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

