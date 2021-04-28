---
description: Classe SystemConfig_Video-essa classe é a classe de tipo de evento para eventos de configuração de vídeo.
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: Classe SystemConfig_Video
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716194eb9ceb67b609f886482393795eaef2ef09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105894"
---
# <a name="systemconfig_video-class"></a><span data-ttu-id="92f5b-103">\_Classe de vídeo SystemConfig</span><span class="sxs-lookup"><span data-stu-id="92f5b-103">SystemConfig\_Video class</span></span>

<span data-ttu-id="92f5b-104">Essa classe é a classe de tipo de evento para eventos de configuração de vídeo.</span><span class="sxs-lookup"><span data-stu-id="92f5b-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="92f5b-105">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="92f5b-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="92f5b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92f5b-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a><span data-ttu-id="92f5b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="92f5b-107">Members</span></span>

<span data-ttu-id="92f5b-108">A classe de **\_ vídeo SystemConfig** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="92f5b-108">The **SystemConfig\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="92f5b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="92f5b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92f5b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="92f5b-110">Properties</span></span>

<span data-ttu-id="92f5b-111">A classe de **\_ vídeo SystemConfig** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="92f5b-111">The **SystemConfig\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92f5b-112">**Adaptadorstring**</span><span class="sxs-lookup"><span data-stu-id="92f5b-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f5b-113">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="92f5b-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92f5b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-115">Qualificadores: **WmiDataId** (8), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="92f5b-115">Qualifiers: **WmiDataId** (8), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="92f5b-116">Nome ou descrição do adaptador.</span><span class="sxs-lookup"><span data-stu-id="92f5b-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="92f5b-117">**Biosstring**</span><span class="sxs-lookup"><span data-stu-id="92f5b-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f5b-118">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="92f5b-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92f5b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-120">Qualificadores: **WmiDataId** (9), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="92f5b-120">Qualifiers: **WmiDataId** (9), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="92f5b-121">Nome do BIOS do adaptador.</span><span class="sxs-lookup"><span data-stu-id="92f5b-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="92f5b-122">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="92f5b-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f5b-123">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92f5b-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92f5b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-125">Qualificadores: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="92f5b-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="92f5b-126">Número de bits usados para exibir cada pixel.</span><span class="sxs-lookup"><span data-stu-id="92f5b-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="92f5b-127">**Chiptype**</span><span class="sxs-lookup"><span data-stu-id="92f5b-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f5b-128">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="92f5b-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92f5b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-130">Qualificadores: **WmiDataId** (6), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="92f5b-130">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="92f5b-131">Nome do chip do adaptador.</span><span class="sxs-lookup"><span data-stu-id="92f5b-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="92f5b-132">**DACType**</span><span class="sxs-lookup"><span data-stu-id="92f5b-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f5b-133">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="92f5b-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92f5b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-135">Qualificadores: **WmiDataId** (7), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="92f5b-135">Qualifiers: **WmiDataId** (7), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="92f5b-136">Nome do chip do conversor digital para analógico (DAC) do adaptador.</span><span class="sxs-lookup"><span data-stu-id="92f5b-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="92f5b-137">**deviceId**</span><span class="sxs-lookup"><span data-stu-id="92f5b-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f5b-138">Tipo de dados: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="92f5b-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92f5b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-140">Qualificadores: **WmiDataId** (10), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="92f5b-140">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="92f5b-141">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="92f5b-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="92f5b-142">**Tamanho da memória**</span><span class="sxs-lookup"><span data-stu-id="92f5b-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f5b-143">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92f5b-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92f5b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-145">Qualificadores: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="92f5b-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="92f5b-146">Quantidade máxima de memória com suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="92f5b-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="92f5b-147">**StateFlags**</span><span class="sxs-lookup"><span data-stu-id="92f5b-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f5b-148">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92f5b-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92f5b-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-150">Qualificadores: **WmiDataId** (11), **formato ("x")**</span><span class="sxs-lookup"><span data-stu-id="92f5b-150">Qualifiers: **WmiDataId** (11), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="92f5b-151">Sinalizadores de estado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92f5b-151">Device state flags.</span></span> <span data-ttu-id="92f5b-152">Pode ser qualquer combinação razoável do seguinte.</span><span class="sxs-lookup"><span data-stu-id="92f5b-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="92f5b-153">Valor</span><span class="sxs-lookup"><span data-stu-id="92f5b-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="92f5b-154">Significado</span><span class="sxs-lookup"><span data-stu-id="92f5b-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="92f5b-155"><dt>**Exibir \_ DISPOSITIVO \_ conectado \_ à \_ área de trabalho**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="92f5b-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="92f5b-156">O dispositivo faz parte da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="92f5b-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="92f5b-157"><dt>**Exibir \_ \_ \_ Driver de espelhamento de dispositivo**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="92f5b-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="92f5b-158">Representa um pseudodispositivo usado para espelhar o desenho do aplicativo para se conectar a um computador remoto ou a outras finalidades.</span><span class="sxs-lookup"><span data-stu-id="92f5b-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="92f5b-159">Um pseudo monitor invisível está associado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92f5b-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="92f5b-160">Por exemplo, o NetMeeting o utiliza.</span><span class="sxs-lookup"><span data-stu-id="92f5b-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="92f5b-161"><dt>**Exibir \_ DISPOSITIVO \_ MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="92f5b-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="92f5b-162">O dispositivo tem mais modos de exibição do que seus dispositivos de saída dão suporte.</span><span class="sxs-lookup"><span data-stu-id="92f5b-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="92f5b-163"><dt>**Exibir \_ \_ \_ Dispositivo primário**</dt> <dt>4 do dispositivo (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="92f5b-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="92f5b-164">A área de trabalho principal está no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92f5b-164">The primary desktop is on the device.</span></span> <span data-ttu-id="92f5b-165">Para um sistema com um único cartão de vídeo, ele é sempre definido.</span><span class="sxs-lookup"><span data-stu-id="92f5b-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="92f5b-166">Para um sistema com vários cartões de vídeo, somente um dispositivo pode ter esse conjunto.</span><span class="sxs-lookup"><span data-stu-id="92f5b-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="92f5b-167"><dt>**Exibir \_ \_Removível do dispositivo**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="92f5b-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="92f5b-168">O dispositivo é removível; Ela não pode ser a exibição primária.</span><span class="sxs-lookup"><span data-stu-id="92f5b-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="92f5b-169"><dt>**Exibir \_ DISPOSITIVO \_ \_ compatível com VGA**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="92f5b-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="92f5b-170">O dispositivo é compatível com VGA.</span><span class="sxs-lookup"><span data-stu-id="92f5b-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="92f5b-171">**VRefresh**</span><span class="sxs-lookup"><span data-stu-id="92f5b-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f5b-172">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92f5b-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92f5b-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-174">Qualificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="92f5b-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="92f5b-175">Taxa de atualização atual, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="92f5b-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="92f5b-176">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="92f5b-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f5b-177">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92f5b-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92f5b-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-179">Qualificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="92f5b-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="92f5b-180">Número atual de pixels horizontais.</span><span class="sxs-lookup"><span data-stu-id="92f5b-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="92f5b-181">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="92f5b-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92f5b-182">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92f5b-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92f5b-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92f5b-184">Qualificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="92f5b-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="92f5b-185">Número atual de pixels verticais.</span><span class="sxs-lookup"><span data-stu-id="92f5b-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92f5b-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92f5b-186">Requirements</span></span>



| <span data-ttu-id="92f5b-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="92f5b-187">Requirement</span></span> | <span data-ttu-id="92f5b-188">Valor</span><span class="sxs-lookup"><span data-stu-id="92f5b-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92f5b-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92f5b-189">Minimum supported client</span></span><br/> | <span data-ttu-id="92f5b-190">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92f5b-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92f5b-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92f5b-191">Minimum supported server</span></span><br/> | <span data-ttu-id="92f5b-192">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92f5b-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92f5b-193">Consulte também</span><span class="sxs-lookup"><span data-stu-id="92f5b-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92f5b-194">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="92f5b-194">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




