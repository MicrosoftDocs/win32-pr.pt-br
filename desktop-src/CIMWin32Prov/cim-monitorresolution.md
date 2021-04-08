---
description: A \_ classe CIM MonitorResolution representa a relação entre as resoluções horizontal e vertical e a taxa de atualização e o modo de verificação para um monitor de desktop. Os valores são especificados no objeto do controlador de vídeo.
ms.assetid: 064620dd-2d92-42d0-9167-35867830a077
ms.tgt_platform: multiple
title: Classe CIM_MonitorResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorResolution
- CIM_MonitorResolution.Caption
- CIM_MonitorResolution.Description
- CIM_MonitorResolution.SettingID
- CIM_MonitorResolution.HorizontalResolution
- CIM_MonitorResolution.MaxRefreshRate
- CIM_MonitorResolution.MinRefreshRate
- CIM_MonitorResolution.RefreshRate
- CIM_MonitorResolution.ScanMode
- CIM_MonitorResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b359a2e7eccf31b32aced8a2ea9f85fb6dc48b7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920453"
---
# <a name="cim_monitorresolution-class"></a><span data-ttu-id="43717-104">\_Classe CIM MonitorResolution</span><span class="sxs-lookup"><span data-stu-id="43717-104">CIM\_MonitorResolution class</span></span>

<span data-ttu-id="43717-105">A classe **CIM \_ MonitorResolution** representa a relação entre as resoluções horizontal e vertical e a taxa de atualização e o modo de verificação para um monitor de desktop.</span><span class="sxs-lookup"><span data-stu-id="43717-105">The **CIM\_MonitorResolution** class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="43717-106">Os valores são especificados no objeto do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="43717-106">Values are specified in the video controller object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43717-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="43717-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="43717-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="43717-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="43717-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="43717-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="43717-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="43717-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="43717-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43717-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEC-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="43717-112">Membros</span><span class="sxs-lookup"><span data-stu-id="43717-112">Members</span></span>

<span data-ttu-id="43717-113">A classe **CIM \_ MonitorResolution** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="43717-113">The **CIM\_MonitorResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="43717-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43717-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43717-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43717-115">Properties</span></span>

<span data-ttu-id="43717-116">A classe **CIM \_ MonitorResolution** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="43717-116">The **CIM\_MonitorResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43717-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="43717-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43717-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43717-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43717-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43717-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43717-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="43717-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="43717-121">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="43717-121">Short textual description of the current object.</span></span>

<span data-ttu-id="43717-122">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="43717-122">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="43717-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="43717-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43717-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43717-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43717-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43717-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43717-126">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="43717-126">Textual description of the current object.</span></span>

<span data-ttu-id="43717-127">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="43717-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="43717-128">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="43717-128">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43717-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43717-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43717-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43717-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43717-131">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de \| Monitor \| de DMTF 2,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="43717-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="43717-132">Resolução horizontal do monitor, em pixels.</span><span class="sxs-lookup"><span data-stu-id="43717-132">Monitor's horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="43717-133">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="43717-133">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43717-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43717-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43717-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43717-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43717-136">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de monitor de DMTF \| \| 2,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="43717-136">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="43717-137">A taxa de atualização máxima do monitor, em Hertz, quando há suporte para um intervalo de taxas nas resoluções especificadas.</span><span class="sxs-lookup"><span data-stu-id="43717-137">Monitor's maximum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="43717-138">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="43717-138">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43717-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43717-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43717-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43717-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43717-141">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de monitor de DMTF \| \| 2,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="43717-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="43717-142">A taxa de atualização mínima do monitor, em Hertz, quando há suporte para um intervalo de taxas nas resoluções especificadas.</span><span class="sxs-lookup"><span data-stu-id="43717-142">Monitor's minimum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="43717-143">**Taxa_de_atualização**</span><span class="sxs-lookup"><span data-stu-id="43717-143">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43717-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43717-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43717-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43717-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43717-146">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de monitor de DMTF \| \| 2,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="43717-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="43717-147">Taxa de atualização do monitor, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="43717-147">Monitor's refresh rate, in hertz.</span></span> <span data-ttu-id="43717-148">Se houver suporte para um intervalo de taxas, use as propriedades **MinRefreshRate** e **MaxRefreshRate** e defina essa propriedade como 0.</span><span class="sxs-lookup"><span data-stu-id="43717-148">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="43717-149">**Scanmode**</span><span class="sxs-lookup"><span data-stu-id="43717-149">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43717-150">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43717-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="43717-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43717-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43717-152">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de monitor de DMTF \| \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="43717-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="43717-153">Modo de verificação usado pelo monitor.</span><span class="sxs-lookup"><span data-stu-id="43717-153">Scan mode that the monitor uses.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="43717-154">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="43717-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="43717-155">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="43717-155">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="43717-156">**Sem suporte** (3)</span><span class="sxs-lookup"><span data-stu-id="43717-156">**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="43717-157">**Operação não entrelaçada** (4)</span><span class="sxs-lookup"><span data-stu-id="43717-157">**Non-Interlaced Operation** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="43717-158">**Operação entrelaçada** (5)</span><span class="sxs-lookup"><span data-stu-id="43717-158">**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="43717-159">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="43717-159">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43717-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43717-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43717-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43717-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43717-162">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuraid"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="43717-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="43717-163">Serve como parte da chave para a instância atual.</span><span class="sxs-lookup"><span data-stu-id="43717-163">Serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="43717-164">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="43717-164">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43717-165">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43717-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43717-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43717-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43717-167">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Resoluções de \| Monitor \| de DMTF 2,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="43717-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="43717-168">Resolução vertical do monitor em pixels.</span><span class="sxs-lookup"><span data-stu-id="43717-168">Monitor's vertical resolution in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43717-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="43717-169">Remarks</span></span>

<span data-ttu-id="43717-170">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="43717-170">WMI does not implement this class.</span></span>

<span data-ttu-id="43717-171">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="43717-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="43717-172">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="43717-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="43717-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43717-173">Requirements</span></span>



| <span data-ttu-id="43717-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="43717-174">Requirement</span></span> | <span data-ttu-id="43717-175">Valor</span><span class="sxs-lookup"><span data-stu-id="43717-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43717-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43717-176">Minimum supported client</span></span><br/> | <span data-ttu-id="43717-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43717-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43717-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43717-178">Minimum supported server</span></span><br/> | <span data-ttu-id="43717-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43717-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43717-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="43717-180">Namespace</span></span><br/>                | <span data-ttu-id="43717-181">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="43717-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43717-182">MOF</span><span class="sxs-lookup"><span data-stu-id="43717-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43717-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43717-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43717-184">DLL</span><span class="sxs-lookup"><span data-stu-id="43717-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43717-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43717-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43717-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="43717-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43717-187">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="43717-187">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

