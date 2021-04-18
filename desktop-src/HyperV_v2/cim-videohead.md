---
description: Representa um cabeçalho de um \_ objeto CIM DisplayController.
ms.assetid: 2bb034d9-d1df-4cc8-a6a8-b6ad7289f582
title: Classe CIM_VideoHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHead
- CIM_VideoHead.CurrentBitsPerPixel
- CIM_VideoHead.CurrentHorizontalResolution
- CIM_VideoHead.CurrentVerticalResolution
- CIM_VideoHead.MaxRefreshRate
- CIM_VideoHead.MinRefreshRate
- CIM_VideoHead.CurrentRefreshRate
- CIM_VideoHead.CurrentScanMode
- CIM_VideoHead.OtherCurrentScanMode
- CIM_VideoHead.CurrentNumberOfRows
- CIM_VideoHead.CurrentNumberOfColumns
- CIM_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22f8176c9bdbeae460dfa22ca395e7ed8dd8351e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758805"
---
# <a name="cim_videohead-class"></a><span data-ttu-id="bcd04-103">\_Classe CIM VideoHead</span><span class="sxs-lookup"><span data-stu-id="bcd04-103">CIM\_VideoHead class</span></span>

<span data-ttu-id="bcd04-104">Representa um cabeçalho de um objeto [**CIM \_ DisplayController**](cim-displaycontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="bcd04-104">Represents one head of a [**CIM\_DisplayController**](cim-displaycontroller.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcd04-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bcd04-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHead : CIM_LogicalDevice
{
  uint32 CurrentBitsPerPixel;
  uint32 CurrentHorizontalResolution;
  uint32 CurrentVerticalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 CurrentRefreshRate;
  uint16 CurrentScanMode;
  string OtherCurrentScanMode;
  uint32 CurrentNumberOfRows;
  uint32 CurrentNumberOfColumns;
  uint64 CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="bcd04-106">Membros</span><span class="sxs-lookup"><span data-stu-id="bcd04-106">Members</span></span>

<span data-ttu-id="bcd04-107">A classe **CIM \_ VideoHead** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bcd04-107">The **CIM\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="bcd04-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bcd04-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bcd04-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bcd04-109">Properties</span></span>

<span data-ttu-id="bcd04-110">A classe **CIM \_ VideoHead** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bcd04-110">The **CIM\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bcd04-111">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="bcd04-111">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcd04-112">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bcd04-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcd04-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-114">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,12 "), **PUnit** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="bcd04-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.12"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="bcd04-115">O número de bits usados para exibir cada pixel.</span><span class="sxs-lookup"><span data-stu-id="bcd04-115">The number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="bcd04-116">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="bcd04-116">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcd04-117">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bcd04-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcd04-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-119">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,11 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. HorizontalResolution "), **PUnit** (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="bcd04-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.11"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.HorizontalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="bcd04-120">O número atual de pixels horizontais.</span><span class="sxs-lookup"><span data-stu-id="bcd04-120">The current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="bcd04-121">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="bcd04-121">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcd04-122">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bcd04-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcd04-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-124">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VideoHeadResolution. NumberOfColors")</span><span class="sxs-lookup"><span data-stu-id="bcd04-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.NumberOfColors")</span></span>
</dt> </dl>

<span data-ttu-id="bcd04-125">O número de cores com suporte na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="bcd04-125">The number of colors supported at the current resolution.</span></span>

</dd> <dt>

<span data-ttu-id="bcd04-126">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="bcd04-126">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcd04-127">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bcd04-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcd04-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,14 ")</span><span class="sxs-lookup"><span data-stu-id="bcd04-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.14")</span></span>
</dt> </dl>

<span data-ttu-id="bcd04-130">Se estiver no modo de caractere, o número de colunas para o controlador de vídeo; caso contrário, "0".</span><span class="sxs-lookup"><span data-stu-id="bcd04-130">If in character mode, the number of columns for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="bcd04-131">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="bcd04-131">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcd04-132">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bcd04-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcd04-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-134">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,13 ")</span><span class="sxs-lookup"><span data-stu-id="bcd04-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.13")</span></span>
</dt> </dl>

<span data-ttu-id="bcd04-135">Se estiver no modo de caractere, o número de linhas para o controlador de vídeo; caso contrário, "0".</span><span class="sxs-lookup"><span data-stu-id="bcd04-135">If in character mode, the number of rows for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="bcd04-136">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="bcd04-136">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcd04-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bcd04-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcd04-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-139">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,15 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. Taxa_de_Atualização "), **PUnit** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="bcd04-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.15"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.RefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="bcd04-140">A taxa de atualização atual do controlador de vídeo, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="bcd04-140">The current refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="bcd04-141">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="bcd04-141">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcd04-142">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcd04-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcd04-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-144">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoHead**.**OtherCurrentScanMode**, CIM \_ VideoHeadResolution. scanmode ")</span><span class="sxs-lookup"><span data-stu-id="bcd04-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**OtherCurrentScanMode**, CIM\_VideoHeadResolution.ScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="bcd04-145">O modo de verificação atual do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bcd04-145">The current scan mode of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bcd04-146">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="bcd04-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bcd04-147">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="bcd04-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="bcd04-148">**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="bcd04-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="bcd04-149">**Operação não entrelaçada** (3)</span><span class="sxs-lookup"><span data-stu-id="bcd04-149">**Non-Interlaced Operation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="bcd04-150">**Operação entrelaçada** (4)</span><span class="sxs-lookup"><span data-stu-id="bcd04-150">**Interlaced Operation** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bcd04-151">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="bcd04-151">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcd04-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bcd04-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcd04-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-154">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,10 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. VerticalResolution "), **PUnit** (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="bcd04-154">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.10"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.VerticalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="bcd04-155">O número atual de pixels verticais.</span><span class="sxs-lookup"><span data-stu-id="bcd04-155">The current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="bcd04-156">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="bcd04-156">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcd04-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bcd04-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcd04-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-159">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MaxRefreshRate "), **PUnit** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="bcd04-159">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MaxRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="bcd04-160">A taxa de atualização máxima do controlador de vídeo, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="bcd04-160">The maximum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="bcd04-161">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="bcd04-161">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcd04-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bcd04-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcd04-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-164">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MinRefreshRate "), **PUnit** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="bcd04-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MinRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="bcd04-165">A taxa de atualização mínima do controlador de vídeo, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="bcd04-165">The minimum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="bcd04-166">**OtherCurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="bcd04-166">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcd04-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bcd04-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcd04-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcd04-169">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoHead**.**CurrentScanMode**, CIM \_ VideoHeadResolution. OtherScanMode ")</span><span class="sxs-lookup"><span data-stu-id="bcd04-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**CurrentScanMode**, CIM\_VideoHeadResolution.OtherScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="bcd04-170">Uma descrição do modo de verificação atual quando a propriedade **CurrentScanMode** é "1" (outra).</span><span class="sxs-lookup"><span data-stu-id="bcd04-170">A description of current scan mode when the **CurrentScanMode** property is "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcd04-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcd04-171">Requirements</span></span>



| <span data-ttu-id="bcd04-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcd04-172">Requirement</span></span> | <span data-ttu-id="bcd04-173">Valor</span><span class="sxs-lookup"><span data-stu-id="bcd04-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd04-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcd04-174">Minimum supported client</span></span><br/> | <span data-ttu-id="bcd04-175">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bcd04-175">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bcd04-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcd04-176">Minimum supported server</span></span><br/> | <span data-ttu-id="bcd04-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bcd04-177">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bcd04-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="bcd04-178">Namespace</span></span><br/>                | <span data-ttu-id="bcd04-179">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="bcd04-179">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bcd04-180">MOF</span><span class="sxs-lookup"><span data-stu-id="bcd04-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcd04-181"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcd04-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcd04-182">DLL</span><span class="sxs-lookup"><span data-stu-id="bcd04-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcd04-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bcd04-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bcd04-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcd04-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcd04-185">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="bcd04-185">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

