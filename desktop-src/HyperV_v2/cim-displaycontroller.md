---
description: Representa um controlador de vídeo.
ms.assetid: 14598ae6-58e2-46ca-8653-b57e5833a224
title: Classe CIM_DisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DisplayController
- CIM_DisplayController.Description
- CIM_DisplayController.VideoProcessor
- CIM_DisplayController.VideoMemoryType
- CIM_DisplayController.OtherVideoMemoryType
- CIM_DisplayController.NumberOfVideoPages
- CIM_DisplayController.MaxMemorySupported
- CIM_DisplayController.AcceleratorCapabilities
- CIM_DisplayController.CapabilityDescriptions
- CIM_DisplayController.OtherVideoArchitecture
- CIM_DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59db37a89ce1f57e01a6a9a27fb9c24177221b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757850"
---
# <a name="cim_displaycontroller-class"></a><span data-ttu-id="bf14d-103">\_Classe CIM DisplayController</span><span class="sxs-lookup"><span data-stu-id="bf14d-103">CIM\_DisplayController class</span></span>

<span data-ttu-id="bf14d-104">Representa um controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bf14d-104">Represents a display controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf14d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf14d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_DisplayController : CIM_Controller
{
  string Description;
  string VideoProcessor;
  uint16 VideoMemoryType;
  string OtherVideoMemoryType;
  uint32 NumberOfVideoPages;
  uint32 MaxMemorySupported;
  uint16 AcceleratorCapabilities[];
  string CapabilityDescriptions[];
  string OtherVideoArchitecture;
  uint16 VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="bf14d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="bf14d-106">Members</span></span>

<span data-ttu-id="bf14d-107">A classe **CIM \_ DisplayController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bf14d-107">The **CIM\_DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="bf14d-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bf14d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf14d-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bf14d-109">Properties</span></span>

<span data-ttu-id="bf14d-110">A classe **CIM \_ DisplayController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bf14d-110">The **CIM\_DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf14d-111">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bf14d-111">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf14d-112">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bf14d-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf14d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-114">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM DisplayController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="bf14d-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="bf14d-115">Os recursos gráficos e 3D do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bf14d-115">The graphics and 3D capabilities of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bf14d-116">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="bf14d-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bf14d-117">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="bf14d-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="bf14d-118">**Acelerador de gráficos** (2)</span><span class="sxs-lookup"><span data-stu-id="bf14d-118">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="bf14d-119">**acelerador 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="bf14d-119">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Fast_Write"></span><span id="pci_fast_write"></span><span id="PCI_FAST_WRITE"></span>

<span data-ttu-id="bf14d-120">**PCI Fast Write** (4)</span><span class="sxs-lookup"><span data-stu-id="bf14d-120">**PCI Fast Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiMonitor_Support"></span><span id="multimonitor_support"></span><span id="MULTIMONITOR_SUPPORT"></span>

<span data-ttu-id="bf14d-121">**Suporte a monitores multimonitor** (5)</span><span class="sxs-lookup"><span data-stu-id="bf14d-121">**MultiMonitor Support** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Mastering"></span><span id="pci_mastering"></span><span id="PCI_MASTERING"></span>

<span data-ttu-id="bf14d-122">**Mestre de PCI** (6)</span><span class="sxs-lookup"><span data-stu-id="bf14d-122">**PCI Mastering** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Second_Monochrome_Adapter_Support"></span><span id="second_monochrome_adapter_support"></span><span id="SECOND_MONOCHROME_ADAPTER_SUPPORT"></span>

<span data-ttu-id="bf14d-123">**Segundo suporte a adaptador monocromático** (7)</span><span class="sxs-lookup"><span data-stu-id="bf14d-123">**Second Monochrome Adapter Support** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Large_Memory_Address_Support"></span><span id="large_memory_address_support"></span><span id="LARGE_MEMORY_ADDRESS_SUPPORT"></span>

<span data-ttu-id="bf14d-124">**Suporte a endereços de memória grande** (8)</span><span class="sxs-lookup"><span data-stu-id="bf14d-124">**Large Memory Address Support** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf14d-125">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bf14d-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf14d-126">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bf14d-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf14d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-128">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM DisplayController**.**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="bf14d-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="bf14d-129">Explicações detalhadas para os recursos do acelerador de vídeo da matriz **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="bf14d-129">Detailed explanations for video accelerator features of the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="bf14d-130">Os itens nessa matriz correspondem aos itens de matriz em **AcceleratorCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="bf14d-130">The items in this array correspond to the array items in **AcceleratorCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="bf14d-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bf14d-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf14d-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bf14d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf14d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-134">Qualificadores: [**substituem**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,18 ")</span><span class="sxs-lookup"><span data-stu-id="bf14d-134">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.18")</span></span>
</dt> </dl>

<span data-ttu-id="bf14d-135">Uma descrição de texto do objeto.</span><span class="sxs-lookup"><span data-stu-id="bf14d-135">A text description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="bf14d-136">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="bf14d-136">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf14d-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf14d-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf14d-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-139">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")</span><span class="sxs-lookup"><span data-stu-id="bf14d-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="bf14d-140">A quantidade máxima de memória com suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="bf14d-140">The maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="bf14d-141">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="bf14d-141">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf14d-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf14d-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf14d-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf14d-144">O número de páginas de vídeo com suporte dadas as resoluções atuais e a memória disponível.</span><span class="sxs-lookup"><span data-stu-id="bf14d-144">The number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="bf14d-145">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="bf14d-145">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf14d-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bf14d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf14d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-148">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**VideoArchitecture**")</span><span class="sxs-lookup"><span data-stu-id="bf14d-148">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoArchitecture**")</span></span>
</dt> </dl>

<span data-ttu-id="bf14d-149">Uma descrição do tipo de arquitetura de vídeo quando a propriedade **VideoArchitecture** contém "1" (outro).</span><span class="sxs-lookup"><span data-stu-id="bf14d-149">A description of the video architecture type when the **VideoArchitecture** property contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="bf14d-150">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="bf14d-150">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf14d-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bf14d-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf14d-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-153">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**VideoMemoryType**")</span><span class="sxs-lookup"><span data-stu-id="bf14d-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="bf14d-154">O tipo de memória de vídeo quando a propriedade **VideoMemoryType** é "1" (outra).</span><span class="sxs-lookup"><span data-stu-id="bf14d-154">The video memory type when the **VideoMemoryType** property is "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="bf14d-155">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="bf14d-155">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf14d-156">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bf14d-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf14d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf14d-158">A arquitetura de vídeo dos controladores de vídeo usada para gerar o sinal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bf14d-158">The display controllers video architecture used to generate the video signal.</span></span> <span data-ttu-id="bf14d-159">Normalmente, um processador de vídeo dedicado gera o sinal de vídeo de acordo com a arquitetura especificada.</span><span class="sxs-lookup"><span data-stu-id="bf14d-159">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="bf14d-160">A arquitetura indica a capacidade de resolução máxima do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bf14d-160">The architecture indicates of the maximum resolution capability of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bf14d-161">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="bf14d-161">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bf14d-162">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="bf14d-162">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="bf14d-163">**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="bf14d-163">**CGA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="bf14d-164">**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="bf14d-164">**EGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="bf14d-165">**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="bf14d-165">**VGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="bf14d-166">**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="bf14d-166">**SVGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="bf14d-167">**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="bf14d-167">**MDA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="bf14d-168">**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="bf14d-168">**HGC** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="bf14d-169">**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="bf14d-169">**MCGA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="bf14d-170">**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="bf14d-170">**8514A** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="bf14d-171">**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="bf14d-171">**XGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="bf14d-172">**Buffer de quadro linear** (11)</span><span class="sxs-lookup"><span data-stu-id="bf14d-172">**Linear Frame Buffer** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="bf14d-173">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="bf14d-173">**PC-98** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="bf14d-174">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="bf14d-174">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="bf14d-175">**Fornecedor reservado** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="bf14d-175">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf14d-176">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="bf14d-176">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf14d-177">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bf14d-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf14d-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-179">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 4,6 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**OtherVideoMemoryType**")</span><span class="sxs-lookup"><span data-stu-id="bf14d-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.6"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**OtherVideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="bf14d-180">O tipo de memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bf14d-180">The type of video memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bf14d-181">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="bf14d-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bf14d-182">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="bf14d-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="bf14d-183">**VRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="bf14d-183">**VRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="bf14d-184">**DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="bf14d-184">**DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="bf14d-185">**SRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="bf14d-185">**SRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="bf14d-186">**WRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="bf14d-186">**WRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="bf14d-187">**Edo RAM** (6)</span><span class="sxs-lookup"><span data-stu-id="bf14d-187">**EDO RAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="bf14d-188">**DRAM síncrona intermitente** (7)</span><span class="sxs-lookup"><span data-stu-id="bf14d-188">**Burst Synchronous DRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="bf14d-189">**SRAM de intermitência em pipeline** (8)</span><span class="sxs-lookup"><span data-stu-id="bf14d-189">**Pipelined Burst SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="bf14d-190">**CDRAM** (9)</span><span class="sxs-lookup"><span data-stu-id="bf14d-190">**CDRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="bf14d-191">**3DRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="bf14d-191">**3DRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="bf14d-192">**SDRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="bf14d-192">**SDRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="bf14d-193">**SGRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="bf14d-193">**SGRAM** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf14d-194">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="bf14d-194">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf14d-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bf14d-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf14d-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf14d-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf14d-197">Uma descrição de texto do controlador/processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bf14d-197">A text description of the video processor/controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf14d-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf14d-198">Requirements</span></span>



| <span data-ttu-id="bf14d-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf14d-199">Requirement</span></span> | <span data-ttu-id="bf14d-200">Valor</span><span class="sxs-lookup"><span data-stu-id="bf14d-200">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf14d-201">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf14d-201">Minimum supported client</span></span><br/> | <span data-ttu-id="bf14d-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bf14d-202">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bf14d-203">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf14d-203">Minimum supported server</span></span><br/> | <span data-ttu-id="bf14d-204">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf14d-204">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bf14d-205">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf14d-205">Namespace</span></span><br/>                | <span data-ttu-id="bf14d-206">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="bf14d-206">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bf14d-207">MOF</span><span class="sxs-lookup"><span data-stu-id="bf14d-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf14d-208"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf14d-208"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf14d-209">DLL</span><span class="sxs-lookup"><span data-stu-id="bf14d-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf14d-210"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf14d-210"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf14d-211">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf14d-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf14d-212">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="bf14d-212">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

