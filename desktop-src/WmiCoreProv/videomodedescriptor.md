---
description: Contém elementos de descritor de modo para a matriz MonitorSourceModes na classe WmiMonitorListedSupportedSourceModes.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: Classe VideoModeDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 06094b24b6b8197eab89b65cd5a9a83f46b39f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297334"
---
# <a name="videomodedescriptor-class"></a><span data-ttu-id="0ba20-103">Classe VideoModeDescriptor</span><span class="sxs-lookup"><span data-stu-id="0ba20-103">VideoModeDescriptor class</span></span>

<span data-ttu-id="0ba20-104">A classe WMI **VideoModeDescriptorVideo** contém elementos do descritor de modo para a matriz **MonitorSourceModes** na classe [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) .</span><span class="sxs-lookup"><span data-stu-id="0ba20-104">The **VideoModeDescriptorVideo** WMI class contains mode descriptor elements for the **MonitorSourceModes** array in the [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) class.</span></span> <span data-ttu-id="0ba20-105">Esses elementos incluem recursos de monitor, como taxa de atualização, características de pixel ou tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="0ba20-105">These elements include monitor features such as refresh rate, pixel characteristics, or image size.</span></span> <span data-ttu-id="0ba20-106">A classe **VideoModeDescriptorVideo** contém informações que são um superconjunto dos dados disponíveis de blocos de tempo estabelecidos, padrão e detalhados.</span><span class="sxs-lookup"><span data-stu-id="0ba20-106">The **VideoModeDescriptorVideo** class contains information that is a superset of the data available from established, standard, and detailed timing blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba20-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ba20-107">Syntax</span></span>

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a><span data-ttu-id="0ba20-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0ba20-108">Members</span></span>

<span data-ttu-id="0ba20-109">A classe **VideoModeDescriptor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0ba20-109">The **VideoModeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="0ba20-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ba20-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ba20-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0ba20-111">Properties</span></span>

<span data-ttu-id="0ba20-112">A classe **VideoModeDescriptor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0ba20-112">The **VideoModeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ba20-113">**CompositePolarityType**</span><span class="sxs-lookup"><span data-stu-id="0ba20-113">**CompositePolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-114">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0ba20-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-116">Tipo de polaridade composta.</span><span class="sxs-lookup"><span data-stu-id="0ba20-116">Composite polarity type.</span></span> <span data-ttu-id="0ba20-117">Essa é a polaridade de pulsos de sincronização horizontal fora da sincronização vertical.</span><span class="sxs-lookup"><span data-stu-id="0ba20-117">This is polarity of horizontal sync pulses outside of vertical sync.</span></span>



| <span data-ttu-id="0ba20-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0ba20-118">Value</span></span>                                                                              | <span data-ttu-id="0ba20-119">Significado</span><span class="sxs-lookup"><span data-stu-id="0ba20-119">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ba20-120"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-120"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0ba20-121">A polaridade composta é positiva.</span><span class="sxs-lookup"><span data-stu-id="0ba20-121">Composite polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0ba20-122"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-122"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0ba20-123">A polaridade composta é negativa.</span><span class="sxs-lookup"><span data-stu-id="0ba20-123">Composite polarity is negative.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0ba20-124"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-124"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0ba20-125">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="0ba20-125">Not applicable.</span></span> <span data-ttu-id="0ba20-126">O tipo de sincronização de sinal deve ser composto digital.</span><span class="sxs-lookup"><span data-stu-id="0ba20-126">The signal sync type must be digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0ba20-127">**HorizontalActivePixels**</span><span class="sxs-lookup"><span data-stu-id="0ba20-127">**HorizontalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-128">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-130">Número de pixels ativos horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="0ba20-130">Number of horizontally active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-131">**HorizontalBlankingPixels**</span><span class="sxs-lookup"><span data-stu-id="0ba20-131">**HorizontalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-132">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-134">Número de pixels horizontalmente em branco</span><span class="sxs-lookup"><span data-stu-id="0ba20-134">Number of horizontally blanking pixels</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-135">**HorizontalBorder**</span><span class="sxs-lookup"><span data-stu-id="0ba20-135">**HorizontalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-136">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-138">Borda horizontal.</span><span class="sxs-lookup"><span data-stu-id="0ba20-138">Horizontal border.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-139">**HorizontalImageSize**</span><span class="sxs-lookup"><span data-stu-id="0ba20-139">**HorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-140">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-142">Tamanho da imagem horizontal em milímetros (mm).</span><span class="sxs-lookup"><span data-stu-id="0ba20-142">Horizontal image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-143">**HorizontalPolarityType**</span><span class="sxs-lookup"><span data-stu-id="0ba20-143">**HorizontalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-144">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0ba20-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-146">Tipo de polaridade horizontal.</span><span class="sxs-lookup"><span data-stu-id="0ba20-146">Horizontal polarity type.</span></span>



| <span data-ttu-id="0ba20-147">Valor</span><span class="sxs-lookup"><span data-stu-id="0ba20-147">Value</span></span>                                                                              | <span data-ttu-id="0ba20-148">Significado</span><span class="sxs-lookup"><span data-stu-id="0ba20-148">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ba20-149"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-149"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0ba20-150">A polaridade horizontal é positiva.</span><span class="sxs-lookup"><span data-stu-id="0ba20-150">Horizontal polarity is positive.</span></span><br/>                               |
| <dl> <span data-ttu-id="0ba20-151"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-151"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0ba20-152">A polaridade horizontal é negativa.</span><span class="sxs-lookup"><span data-stu-id="0ba20-152">Horizontal polarity is negative.</span></span><br/>                               |
| <dl> <span data-ttu-id="0ba20-153"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-153"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0ba20-154">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="0ba20-154">Not applicable.</span></span> <span data-ttu-id="0ba20-155">O tipo de sincronização de sinal deve ser separado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="0ba20-155">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0ba20-156">**HorizontalRefreshRateDenominator**</span><span class="sxs-lookup"><span data-stu-id="0ba20-156">**HorizontalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-157">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-159">Denominador da taxa de atualização horizontal.</span><span class="sxs-lookup"><span data-stu-id="0ba20-159">Horizontal refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-160">**HorizontalRefreshRateNumerator**</span><span class="sxs-lookup"><span data-stu-id="0ba20-160">**HorizontalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-161">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-163">Numerador de taxa de atualização horizontal em Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="0ba20-163">Horizontal refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-164">**HorizontalSyncOffset**</span><span class="sxs-lookup"><span data-stu-id="0ba20-164">**HorizontalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-165">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-167">Deslocamento de sincronização horizontal.</span><span class="sxs-lookup"><span data-stu-id="0ba20-167">Horizontal sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-168">**HorizontalSyncPulseWidth**</span><span class="sxs-lookup"><span data-stu-id="0ba20-168">**HorizontalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-169">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-171">Largura de pulso de sincronização horizontal.</span><span class="sxs-lookup"><span data-stu-id="0ba20-171">Horizontal sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-172">**Isentrelaçado**</span><span class="sxs-lookup"><span data-stu-id="0ba20-172">**IsInterlaced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-173">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0ba20-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-175">Indica se o modo de exibição está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="0ba20-175">Indicates whether the display mode is interlaced.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-176">**IsSerrationRequired**</span><span class="sxs-lookup"><span data-stu-id="0ba20-176">**IsSerrationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-177">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0ba20-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-179">Indica que tipo de serration é necessário, se apropriado.</span><span class="sxs-lookup"><span data-stu-id="0ba20-179">Indicates what type of serration is required, if appropriate.</span></span>



| <span data-ttu-id="0ba20-180">Valor</span><span class="sxs-lookup"><span data-stu-id="0ba20-180">Value</span></span>                                                                              | <span data-ttu-id="0ba20-181">Significado</span><span class="sxs-lookup"><span data-stu-id="0ba20-181">Meaning</span></span>                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ba20-182"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0ba20-183">O controlador deve fornecer sincronização horizontal durante a sincronização vertical.</span><span class="sxs-lookup"><span data-stu-id="0ba20-183">Controller shall supply horizontal sync during vertical sync.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0ba20-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0ba20-185">O controlador não deve fornecer sincronização horizontal durante a sincronização vertical.</span><span class="sxs-lookup"><span data-stu-id="0ba20-185">Controller shall not supply horizontal sync during vertical sync.</span></span><br/>                             |
| <dl> <span data-ttu-id="0ba20-186"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-186"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0ba20-187">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="0ba20-187">Not applicable.</span></span> <span data-ttu-id="0ba20-188">O tipo de sincronização de sinal deve ser bipolar, analógico composto ou digital composto.</span><span class="sxs-lookup"><span data-stu-id="0ba20-188">The signal sync type must be bipolar, analog composite, or digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0ba20-189">**IsSyncOnRGB**</span><span class="sxs-lookup"><span data-stu-id="0ba20-189">**IsSyncOnRGB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-190">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0ba20-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-192">Indica quais linhas de sinal de vídeo devem ser sincronizadas, se apropriado.</span><span class="sxs-lookup"><span data-stu-id="0ba20-192">Indicates which video signal lines should be synchronized, if appropriate.</span></span>



| <span data-ttu-id="0ba20-193">Valor</span><span class="sxs-lookup"><span data-stu-id="0ba20-193">Value</span></span>                                                                              | <span data-ttu-id="0ba20-194">Significado</span><span class="sxs-lookup"><span data-stu-id="0ba20-194">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ba20-195"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-195"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0ba20-196">O pulso de sincronização deve aparecer em todas as três linhas de sinal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0ba20-196">Sync pulse should appear on all 3 video signal lines.</span></span><br/>                  |
| <dl> <span data-ttu-id="0ba20-197"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-197"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0ba20-198">O pulso de sincronização só deve aparecer na linha verde do sinal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0ba20-198">Sync pulse should only appear on the green video signal line.</span></span><br/>          |
| <dl> <span data-ttu-id="0ba20-199"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-199"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0ba20-200">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="0ba20-200">Not applicable.</span></span> <span data-ttu-id="0ba20-201">O tipo de sincronização de sinal deve ser composto bipolar analógico.</span><span class="sxs-lookup"><span data-stu-id="0ba20-201">The signal sync type must be bipolar analog composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0ba20-202">**PixelClockRate**</span><span class="sxs-lookup"><span data-stu-id="0ba20-202">**PixelClockRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-203">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ba20-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-205">Taxa de relógio de pixel em Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="0ba20-205">Pixel clock rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-206">**StereoModeType**</span><span class="sxs-lookup"><span data-stu-id="0ba20-206">**StereoModeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-207">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0ba20-207">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-209">Tipo de modo estéreo.</span><span class="sxs-lookup"><span data-stu-id="0ba20-209">Stereo mode type.</span></span> <span data-ttu-id="0ba20-210">A tabela a seguir lista os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="0ba20-210">The following table lists the possible values.</span></span>



| <span data-ttu-id="0ba20-211">Valor</span><span class="sxs-lookup"><span data-stu-id="0ba20-211">Value</span></span>                                                                              | <span data-ttu-id="0ba20-212">Significado</span><span class="sxs-lookup"><span data-stu-id="0ba20-212">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ba20-213"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-213"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0ba20-214">Sem estéreo.</span><span class="sxs-lookup"><span data-stu-id="0ba20-214">No stereo.</span></span><br/>                                               |
| <dl> <span data-ttu-id="0ba20-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-215"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0ba20-216">Estéreo sequencial de campo com imagem direita na sincronização de estéreo.</span><span class="sxs-lookup"><span data-stu-id="0ba20-216">Field sequential stereo with right image on stereo sync.</span></span><br/> |
| <dl> <span data-ttu-id="0ba20-217"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-217"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0ba20-218">Campo estéreo sequencial com imagem esquerda na sincronização de estéreo.</span><span class="sxs-lookup"><span data-stu-id="0ba20-218">Field sequential stereo with left image on stereo sync.</span></span><br/>  |
| <dl> <span data-ttu-id="0ba20-219"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-219"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="0ba20-220">Estéreo intercalado de 2 vias com imagem direita em linhas pares.</span><span class="sxs-lookup"><span data-stu-id="0ba20-220">2-way Interleaved Stereo with Right Image on Even Lines.</span></span><br/> |
| <dl> <span data-ttu-id="0ba20-221"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-221"><dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="0ba20-222">Estéreo intercalado de 2 vias com imagem esquerda em linhas pares.</span><span class="sxs-lookup"><span data-stu-id="0ba20-222">2-way Interleaved Stereo with Left Image on Even Lines.</span></span><br/>  |
| <dl> <span data-ttu-id="0ba20-223"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-223"><dt>5 (0x5)</dt></span></span> </dl> | <span data-ttu-id="0ba20-224">Estéreo intercalado de 4 vias.</span><span class="sxs-lookup"><span data-stu-id="0ba20-224">4-way Interleaved Stereo.</span></span><br/>                                |
| <dl> <span data-ttu-id="0ba20-225"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-225"><dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="0ba20-226">Estéreo intercalado lado a lado.</span><span class="sxs-lookup"><span data-stu-id="0ba20-226">Side-by-Side Interleaved Stereo.</span></span><br/>                         |



 

</dd> <dt>

<span data-ttu-id="0ba20-227">**SyncSignalType**</span><span class="sxs-lookup"><span data-stu-id="0ba20-227">**SyncSignalType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-228">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0ba20-228">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-230">Tipo de sincronização de sinal.</span><span class="sxs-lookup"><span data-stu-id="0ba20-230">Signal sync type.</span></span> <span data-ttu-id="0ba20-231">A tabela a seguir lista os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="0ba20-231">The following table lists the possible values.</span></span>



| <span data-ttu-id="0ba20-232">Valor</span><span class="sxs-lookup"><span data-stu-id="0ba20-232">Value</span></span>                                                                              | <span data-ttu-id="0ba20-233">Significado</span><span class="sxs-lookup"><span data-stu-id="0ba20-233">Meaning</span></span>                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="0ba20-234"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-234"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0ba20-235">Composto analógico</span><span class="sxs-lookup"><span data-stu-id="0ba20-235">Analog Composite</span></span><br/>         |
| <dl> <span data-ttu-id="0ba20-236"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-236"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0ba20-237">Bipolar analógico composto</span><span class="sxs-lookup"><span data-stu-id="0ba20-237">Bipolar Analog Composite</span></span><br/> |
| <dl> <span data-ttu-id="0ba20-238"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-238"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0ba20-239">Composto digital</span><span class="sxs-lookup"><span data-stu-id="0ba20-239">Digital Composite</span></span><br/>        |
| <dl> <span data-ttu-id="0ba20-240"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-240"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="0ba20-241">Separado digital</span><span class="sxs-lookup"><span data-stu-id="0ba20-241">Digital Separate</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="0ba20-242">**VerticalActivePixels**</span><span class="sxs-lookup"><span data-stu-id="0ba20-242">**VerticalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-243">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-245">Número de pixels ativos verticalmente.</span><span class="sxs-lookup"><span data-stu-id="0ba20-245">Number of vertically active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-246">**VerticalBlankingPixels**</span><span class="sxs-lookup"><span data-stu-id="0ba20-246">**VerticalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-247">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-249">Número de pixels em branco verticalmente.</span><span class="sxs-lookup"><span data-stu-id="0ba20-249">Number of vertically blanking pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-250">**VerticalBorder**</span><span class="sxs-lookup"><span data-stu-id="0ba20-250">**VerticalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-251">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-253">Borda vertical.</span><span class="sxs-lookup"><span data-stu-id="0ba20-253">Vertical border.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-254">**VerticalImageSize**</span><span class="sxs-lookup"><span data-stu-id="0ba20-254">**VerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-255">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-257">Tamanho vertical da imagem em milímetros (mm).</span><span class="sxs-lookup"><span data-stu-id="0ba20-257">Vertical image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-258">**VerticalPolarityType**</span><span class="sxs-lookup"><span data-stu-id="0ba20-258">**VerticalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-259">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0ba20-259">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-261">Tipo de polaridade vertical.</span><span class="sxs-lookup"><span data-stu-id="0ba20-261">Vertical polarity type.</span></span>



| <span data-ttu-id="0ba20-262">Valor</span><span class="sxs-lookup"><span data-stu-id="0ba20-262">Value</span></span>                                                                              | <span data-ttu-id="0ba20-263">Significado</span><span class="sxs-lookup"><span data-stu-id="0ba20-263">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ba20-264"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-264"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0ba20-265">A polaridade vertical é positiva.</span><span class="sxs-lookup"><span data-stu-id="0ba20-265">Vertical polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0ba20-266"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-266"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0ba20-267">A polaridade vertical é negativa</span><span class="sxs-lookup"><span data-stu-id="0ba20-267">Vertical polarity is negative</span></span><br/>                                  |
| <dl> <span data-ttu-id="0ba20-268"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-268"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0ba20-269">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="0ba20-269">Not applicable.</span></span> <span data-ttu-id="0ba20-270">O tipo de sincronização de sinal deve ser separado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="0ba20-270">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0ba20-271">**VerticalRefreshRateDenominator**</span><span class="sxs-lookup"><span data-stu-id="0ba20-271">**VerticalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-272">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-274">Denominador de taxa de atualização vertical.</span><span class="sxs-lookup"><span data-stu-id="0ba20-274">Vertical refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-275">**VerticalRefreshRateNumerator**</span><span class="sxs-lookup"><span data-stu-id="0ba20-275">**VerticalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-276">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-278">Numerador de taxa de atualização vertical em Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="0ba20-278">Vertical refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-279">**VerticalSyncOffset**</span><span class="sxs-lookup"><span data-stu-id="0ba20-279">**VerticalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-280">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-282">Deslocamento de sincronização vertical.</span><span class="sxs-lookup"><span data-stu-id="0ba20-282">Vertical sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-283">**VerticalSyncPulseWidth**</span><span class="sxs-lookup"><span data-stu-id="0ba20-283">**VerticalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-284">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ba20-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-286">Largura vertical de pulso de sincronização.</span><span class="sxs-lookup"><span data-stu-id="0ba20-286">Vertical sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="0ba20-287">VideoStandardType</span><span class="sxs-lookup"><span data-stu-id="0ba20-287">VideoStandardType</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba20-288">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0ba20-288">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0ba20-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0ba20-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ba20-290">Tipo padrão de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0ba20-290">Video standard type.</span></span>



| <span data-ttu-id="0ba20-291">Valor</span><span class="sxs-lookup"><span data-stu-id="0ba20-291">Value</span></span>                                                                                | <span data-ttu-id="0ba20-292">Significado</span><span class="sxs-lookup"><span data-stu-id="0ba20-292">Meaning</span></span>                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ba20-293"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-293"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="0ba20-294">Outro</span><span class="sxs-lookup"><span data-stu-id="0ba20-294">Other</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0ba20-295"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-295"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="0ba20-296">VESA DMT.</span><span class="sxs-lookup"><span data-stu-id="0ba20-296">VESA DMT.</span></span> <span data-ttu-id="0ba20-297">Na especificação de tempos do monitor de exibição da VESA (Video Electronics Standard Association).</span><span class="sxs-lookup"><span data-stu-id="0ba20-297">From Video Electronics Standard Association (VESA) Display Monitor Timings specification.</span></span><br/> |
| <dl> <span data-ttu-id="0ba20-298"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-298"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="0ba20-299">VESA GTF.</span><span class="sxs-lookup"><span data-stu-id="0ba20-299">VESA GTF.</span></span> <span data-ttu-id="0ba20-300">Do padrão de fórmula de tempo generalizado VESA.</span><span class="sxs-lookup"><span data-stu-id="0ba20-300">From VESA Generalized Timing Formula standard.</span></span><br/>                                            |
| <dl> <span data-ttu-id="0ba20-301"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-301"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="0ba20-302">Padrão de temporizações de vídeo coordenado VESA CVT/da VESA.</span><span class="sxs-lookup"><span data-stu-id="0ba20-302">VESA CVT/ From VESA Coordinated Video Timings standard.</span></span><br/>                                             |
| <dl> <span data-ttu-id="0ba20-303"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-303"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="0ba20-304">IBM</span><span class="sxs-lookup"><span data-stu-id="0ba20-304">IBM</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="0ba20-305"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-305"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="0ba20-306">LARANJA</span><span class="sxs-lookup"><span data-stu-id="0ba20-306">APPLE</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0ba20-307"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-307"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="0ba20-308">NTSC M</span><span class="sxs-lookup"><span data-stu-id="0ba20-308">NTSC M</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="0ba20-309"><dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-309"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="0ba20-310">J NTSC</span><span class="sxs-lookup"><span data-stu-id="0ba20-310">NTSC J</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="0ba20-311"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-311"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="0ba20-312">NTSC 433</span><span class="sxs-lookup"><span data-stu-id="0ba20-312">NTSC 433</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="0ba20-313"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-313"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="0ba20-314">PAL B</span><span class="sxs-lookup"><span data-stu-id="0ba20-314">PAL B</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0ba20-315"><dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-315"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="0ba20-316">PAL B1</span><span class="sxs-lookup"><span data-stu-id="0ba20-316">PAL B1</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="0ba20-317"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-317"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="0ba20-318">PAL G</span><span class="sxs-lookup"><span data-stu-id="0ba20-318">PAL G</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0ba20-319"><dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-319"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="0ba20-320">PAL H</span><span class="sxs-lookup"><span data-stu-id="0ba20-320">PAL H</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0ba20-321"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-321"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="0ba20-322">PAL I</span><span class="sxs-lookup"><span data-stu-id="0ba20-322">PAL I</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0ba20-323"><dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-323"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="0ba20-324">PAL D</span><span class="sxs-lookup"><span data-stu-id="0ba20-324">PAL D</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0ba20-325"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-325"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="0ba20-326">PAL N</span><span class="sxs-lookup"><span data-stu-id="0ba20-326">PAL N</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="0ba20-327"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-327"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="0ba20-328">NC DE PAL</span><span class="sxs-lookup"><span data-stu-id="0ba20-328">PAL NC</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="0ba20-329"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-329"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="0ba20-330">SECAM B</span><span class="sxs-lookup"><span data-stu-id="0ba20-330">SECAM B</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0ba20-331"><dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-331"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="0ba20-332">SECAM D</span><span class="sxs-lookup"><span data-stu-id="0ba20-332">SECAM D</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0ba20-333"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-333"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="0ba20-334">SECAM G</span><span class="sxs-lookup"><span data-stu-id="0ba20-334">SECAM G</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0ba20-335"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-335"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="0ba20-336">SECAM H</span><span class="sxs-lookup"><span data-stu-id="0ba20-336">SECAM H</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0ba20-337"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-337"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="0ba20-338">SECAM K</span><span class="sxs-lookup"><span data-stu-id="0ba20-338">SECAM K</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0ba20-339"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-339"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="0ba20-340">SECAM K1</span><span class="sxs-lookup"><span data-stu-id="0ba20-340">SECAM K1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="0ba20-341"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-341"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="0ba20-342">SECAM L</span><span class="sxs-lookup"><span data-stu-id="0ba20-342">SECAM L</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0ba20-343"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-343"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="0ba20-344">SECAM L1</span><span class="sxs-lookup"><span data-stu-id="0ba20-344">SECAM L1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="0ba20-345"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-345"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="0ba20-346">EIA861</span><span class="sxs-lookup"><span data-stu-id="0ba20-346">EIA861</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="0ba20-347"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-347"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="0ba20-348">EIA861A</span><span class="sxs-lookup"><span data-stu-id="0ba20-348">EIA861A</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0ba20-349"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-349"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="0ba20-350">EIA861B</span><span class="sxs-lookup"><span data-stu-id="0ba20-350">EIA861B</span></span><br/>                                                                                             |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ba20-351">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ba20-351">Requirements</span></span>



| <span data-ttu-id="0ba20-352">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ba20-352">Requirement</span></span> | <span data-ttu-id="0ba20-353">Valor</span><span class="sxs-lookup"><span data-stu-id="0ba20-353">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba20-354">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ba20-354">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba20-355">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ba20-355">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0ba20-356">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ba20-356">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba20-357">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ba20-357">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0ba20-358">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ba20-358">Namespace</span></span><br/>                | <span data-ttu-id="0ba20-359">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="0ba20-359">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="0ba20-360">MOF</span><span class="sxs-lookup"><span data-stu-id="0ba20-360">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ba20-361"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-361"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ba20-362">DLL</span><span class="sxs-lookup"><span data-stu-id="0ba20-362">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ba20-363"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ba20-363"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba20-364">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ba20-364">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba20-365">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="0ba20-365">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




