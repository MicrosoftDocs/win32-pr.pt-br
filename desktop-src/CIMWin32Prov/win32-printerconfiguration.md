---
description: A \_ classe WMI PrinterConfiguration do Win32 representa a configuração de um dispositivo de impressora. Isso inclui recursos como resolução, cor, fontes e orientação.
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Classe Win32_PrinterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920490"
---
# <a name="win32_printerconfiguration-class"></a><span data-ttu-id="8e5cf-104">\_Classe Win32 PrinterConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e5cf-104">Win32\_PrinterConfiguration class</span></span>

<span data-ttu-id="8e5cf-105">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterConfiguration do Win32** representa a configuração de um dispositivo de impressora.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-105">The **Win32\_PrinterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the configuration for a printer device.</span></span> <span data-ttu-id="8e5cf-106">Isso inclui recursos como resolução, cor, fontes e orientação.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-106">This includes capabilities such as resolution, color, fonts, and orientation.</span></span>

<span data-ttu-id="8e5cf-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8e5cf-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5cf-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e5cf-109">Syntax</span></span>

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a><span data-ttu-id="8e5cf-110">Membros</span><span class="sxs-lookup"><span data-stu-id="8e5cf-110">Members</span></span>

<span data-ttu-id="8e5cf-111">A classe **Win32 \_ PrinterConfiguration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8e5cf-111">The **Win32\_PrinterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="8e5cf-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8e5cf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e5cf-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8e5cf-113">Properties</span></span>

<span data-ttu-id="8e5cf-114">A classe **Win32 \_ PrinterConfiguration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-114">The **Win32\_PrinterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e5cf-115">**BitsPerPel**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-115">**BitsPerPel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-116">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-118">Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-118">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-119">Número de bits usados para representar a cor nessa configuração (os bits por pixel).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-119">Number of bits used to represent the color in this configuration (the bits per pixel).</span></span> <span data-ttu-id="8e5cf-120">Esta propriedade está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-120">This property is obsolete.</span></span> <span data-ttu-id="8e5cf-121">Em vez disso, use as propriedades nas classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) para determinar como a cor é representada.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-121">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes to determine how color is represented.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-122">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-125">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-126">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-126">Short textual description of the current object.</span></span>

<span data-ttu-id="8e5cf-127">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-128">**Agrupar**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-128">**Collate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-131">Se **for true**, as páginas que são impressas devem ser agrupadas.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-131">If **TRUE**, the pages that are printed should be collated.</span></span> <span data-ttu-id="8e5cf-132">Para se agrupar é imprimir o documento inteiro antes de imprimir a próxima cópia, em vez de imprimir cada página do documento o número necessário de vezes.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-132">To collate is to print out the entire document before printing the next copy, as opposed to printing out each page of the document the required number of times.</span></span>

<span data-ttu-id="8e5cf-133">Essa propriedade é ignorada, a menos que o driver de impressora indique suporte para Agrupamento.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-133">This property is ignored unless the printer driver indicates support for collation.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-134">**Cor**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-134">**Color**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-137">Cor do documento.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-137">Color of the document.</span></span> <span data-ttu-id="8e5cf-138">Algumas impressoras coloridas têm a capacidade de imprimir usando preto em vez de uma combinação de ciano, magenta e amarelo (CMY).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-138">Some color printers have the capability to print using true black instead of a combination of cyan, magenta, and yellow (CMY).</span></span> <span data-ttu-id="8e5cf-139">Isso geralmente cria texto mais escuro e mais nítido para documentos.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-139">This usually creates darker and sharper text for documents.</span></span> <span data-ttu-id="8e5cf-140">Essa opção só é útil para impressoras coloridas que dão suporte à impressão em preto real.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-140">This option is only useful for color printers that support true black printing.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="8e5cf-141"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-141"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-142">Monocromático (preto verdadeiro)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-142">Monochrome (true black)</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="8e5cf-143"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-143"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-144">Cor</span><span class="sxs-lookup"><span data-stu-id="8e5cf-144">Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e5cf-145">**Cópias**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-145">**Copies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-148">Número de cópias a serem impressas.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-148">Number of copies to be printed.</span></span> <span data-ttu-id="8e5cf-149">O driver de impressora deve dar suporte à impressão de cópias de várias páginas.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-149">The printer driver must support printing multi-page copies.</span></span>

<span data-ttu-id="8e5cf-150">Exemplo: 2</span><span class="sxs-lookup"><span data-stu-id="8e5cf-150">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-151">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-154">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-154">Textual description of the current object.</span></span>

<span data-ttu-id="8e5cf-155">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-155">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-156">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-156">**DeviceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-159">Nome amigável da impressora.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-159">Friendly name of the printer.</span></span> <span data-ttu-id="8e5cf-160">Esse nome é exclusivo para o tipo de impressora e pode ser truncado devido às limitações da cadeia de caracteres da qual ela é derivada.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-160">This name is unique to the type of printer and may be truncated because of the limitations of the string from which it is derived.</span></span>

<span data-ttu-id="8e5cf-161">Exemplo: "PCL/HP LaserJet"</span><span class="sxs-lookup"><span data-stu-id="8e5cf-161">Example: "PCL/HP LaserJet"</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-162">**DisplayFlags**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-162">**DisplayFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-163">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-165">Indica se o dispositivo de vídeo é colorido ou monocromático e se o tipo de verificação é não entrelaçado ou entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-165">Indicates whether the display device is color or monochrome and whether the type of scanning is noninterlaced or interlaced.</span></span> <span data-ttu-id="8e5cf-166">Esta propriedade está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-166">This property is obsolete.</span></span> <span data-ttu-id="8e5cf-167">Em vez disso, use Propriedades de exibição, como a propriedade **DisplayType** da classe **Win32 \_ DesktopMonitor** .</span><span class="sxs-lookup"><span data-stu-id="8e5cf-167">Instead, use display properties such as the **DisplayType** property of the **Win32\_DesktopMonitor** class.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-168">**DisplayFrequency**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-168">**DisplayFrequency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-169">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-171">Exibe a taxa de atualização vertical.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-171">Displays the vertical refresh rate.</span></span> <span data-ttu-id="8e5cf-172">A taxa de atualização para um monitor é o número de vezes que a tela é redesenhada por segundo (frequência).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-172">The refresh rate for a monitor is the number of times the screen is redrawn per second (frequency).</span></span> <span data-ttu-id="8e5cf-173">Esta propriedade está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-173">This property is obsolete.</span></span> <span data-ttu-id="8e5cf-174">Em vez disso, use as propriedades na classe [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .</span><span class="sxs-lookup"><span data-stu-id="8e5cf-174">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-175">**Pontilhado**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-175">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-176">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-178">Tipo de pontilhamento da impressora.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-178">Dither type of the printer.</span></span> <span data-ttu-id="8e5cf-179">Essa propriedade pode assumir valores predefinidos de 1 a 5 ou valores definidos pelo driver de 6 a 256.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-179">This property can assume predefined values of 1 to 5, or driver-defined values from 6 to 256.</span></span> <span data-ttu-id="8e5cf-180">O pontilhamento de arte de linha é um método especial de pontilhamento que produz bordas bem definidas entre as escalas preta, branca e cinza.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-180">Line art dithering is a special dithering method that produces well defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="8e5cf-181">Ele não é adequado para imagens que incluem graduações contínuas em intensidade e matiz, como fotografias digitalizadas.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-181">It is not suitable for images that include continuous graduations in intensity and hue, such as scanned photographs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="8e5cf-182"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-182"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-183">Sem pontilhamento</span><span class="sxs-lookup"><span data-stu-id="8e5cf-183">No Dithering</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="8e5cf-184"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-184"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-185">Pincel grosso</span><span class="sxs-lookup"><span data-stu-id="8e5cf-185">Coarse Brush</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="8e5cf-186"><span id="3"></span>**Beta**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-186"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-187">Pincel fino</span><span class="sxs-lookup"><span data-stu-id="8e5cf-187">Fine Brush</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="8e5cf-188"><span id="4"></span>**quatro**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-188"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-189">Arte de linhas</span><span class="sxs-lookup"><span data-stu-id="8e5cf-189">Line Art</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="8e5cf-190"><span id="5"></span>**05**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-190"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-191">Escala de cinza</span><span class="sxs-lookup"><span data-stu-id="8e5cf-191">Grayscale</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e5cf-192">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-192">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-193">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-195">Número de versão do driver de impressora baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-195">Version number of the Windows-based printer driver.</span></span> <span data-ttu-id="8e5cf-196">Os números de versão são criados e mantidos pelo fabricante do driver.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-196">The version numbers are created and maintained by the driver manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-197">**Duplex**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-197">**Duplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-198">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-200">Se for **true**, a impressão será feita em ambos os lados.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-200">If **TRUE**, printing is done on both sides.</span></span> <span data-ttu-id="8e5cf-201">Se for **false**, a impressão será feita em apenas um lado da mídia.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-201">If **FALSE**, printing is done on only one side of the media.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-202">**Tipo de formulário**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-202">**FormName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-205">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-205">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-206">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-206">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-207">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-209">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (pontos por polegada)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-209">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-210">Resolução de impressão em pontos por polegada ao longo do eixo x (largura) do trabalho de impressão (semelhante à propriedade **XResolution** obsoleta).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-210">Print resolution in dots per inch along the x-axis (width) of the print job (similar to the obsolete **XResolution** property).</span></span> <span data-ttu-id="8e5cf-211">Esse valor só é definido quando a propriedade **PrintQuality** dessa classe é positiva.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-211">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-212">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-212">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-213">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-213">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-215">Valor específico de um dos três métodos de correspondência de cor possíveis (chamados de tentativas) que devem ser usados por padrão.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-215">Specific value of one of the three possible color matching methods (called intents) that should be used by default.</span></span> <span data-ttu-id="8e5cf-216">Os aplicativos ICM estabelecem tentativas usando as funções ICM.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-216">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="8e5cf-217">Essa propriedade pode assumir valores predefinidos de 1 a 3 ou valores definidos pelo driver de 4 a 256.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-217">This property can assume predefined values of 1 to 3, or driver-defined values from 4 to 256.</span></span> <span data-ttu-id="8e5cf-218">Aplicativos não ICM podem usar esse valor para determinar como a impressora trata os trabalhos de impressão colorida.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-218">Non-ICM applications can use this value to determine how the printer handles color printing jobs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="8e5cf-219"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-219"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-220">Saturação</span><span class="sxs-lookup"><span data-stu-id="8e5cf-220">Saturation</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="8e5cf-221"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-221"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-222">Contraste</span><span class="sxs-lookup"><span data-stu-id="8e5cf-222">Contrast</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="8e5cf-223"><span id="3"></span>**Beta**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-223"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-224">Cor exata</span><span class="sxs-lookup"><span data-stu-id="8e5cf-224">Exact Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e5cf-225">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-225">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-226">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-228">Como o ICM é manipulado.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-228">How ICM is handled.</span></span> <span data-ttu-id="8e5cf-229">Para um aplicativo não ICM, essa propriedade determina se o ICM está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-229">For a non-ICM application, this property determines if ICM is enabled or disabled.</span></span> <span data-ttu-id="8e5cf-230">Para aplicativos ICM, o sistema examina essa propriedade para determinar qual parte do sistema de computador trata do suporte a ICM.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-230">For ICM applications, the system examines this property to determine which part of the computer system handles ICM support.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="8e5cf-231"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-231"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-232">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="8e5cf-232">Disabled</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="8e5cf-233"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-233"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-234">Windows</span><span class="sxs-lookup"><span data-stu-id="8e5cf-234">Windows</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="8e5cf-235"><span id="3"></span>**Beta**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-235"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-236">Driver de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8e5cf-236">Device Driver</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="8e5cf-237"><span id="4"></span>**quatro**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-237"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-238">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="8e5cf-238">Device</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e5cf-239">**LogPixels**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-239">**LogPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-240">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-242">Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-242">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-243">Número de pixels por polegada lógica.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-243">Number of pixels per logical inch.</span></span> <span data-ttu-id="8e5cf-244">Essa propriedade obsoleta é válida somente com dispositivos que funcionam com pixels, o que exclui dispositivos como impressoras.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-244">This obsolete property is valid only with devices that work with pixels, which excludes devices such as printers.</span></span> <span data-ttu-id="8e5cf-245">Não há nenhum valor de substituição que se aplica a impressoras.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-245">There is no replacement value that applies to printers.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-246">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-246">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-247">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-249">Tipo de mídia na qual a impressora é impressa.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-249">Type of media on which the printer prints.</span></span> <span data-ttu-id="8e5cf-250">A propriedade pode ser definida como um valor predefinido ou um valor definido pelo driver maior ou igual a 256.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-250">The property can be set to a predefined value or a driver-defined value greater than or equal to 256.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="8e5cf-251"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-251"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-252">Standard</span><span class="sxs-lookup"><span data-stu-id="8e5cf-252">Standard</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="8e5cf-253"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-253"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-254">Transparência</span><span class="sxs-lookup"><span data-stu-id="8e5cf-254">Transparency</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="8e5cf-255"><span id="3"></span>**Beta**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-255"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-256">Acetinado</span><span class="sxs-lookup"><span data-stu-id="8e5cf-256">Glossy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e5cf-257">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-257">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-260">Qualificadores: [**chave**](../wmisdk/standard-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-260">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-261">Nome da impressora à qual esta configuração está associada.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-261">Name of the printer with which this configuration is associated.</span></span> <span data-ttu-id="8e5cf-262">Esse valor corresponde à propriedade **Name** da instância de [**\_ impressora Win32**](win32-printer.md) associada.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-262">This value matches the **Name** property of the associated [**Win32\_Printer**](win32-printer.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-263">**Direção**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-263">**Orientation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-264">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-266">Orientação de impressão do papel.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-266">Printing orientation of the paper.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="8e5cf-267"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-267"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-268">Retrato</span><span class="sxs-lookup"><span data-stu-id="8e5cf-268">Portrait</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="8e5cf-269"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-269"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-270">Paisagem</span><span class="sxs-lookup"><span data-stu-id="8e5cf-270">Landscape</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e5cf-271">**PaperLength**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-271">**PaperLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-272">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-274">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimos de milímetro)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-274">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-275">Comprimento do papel.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-275">Length of the paper.</span></span> <span data-ttu-id="8e5cf-276">Para determinar o tamanho do papel em polegadas, divida esse valor por 254.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-276">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="8e5cf-277">Exemplo: 2794</span><span class="sxs-lookup"><span data-stu-id="8e5cf-277">Example: 2794</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-278">**Papel**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-278">**PaperSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-281">Tamanho do papel.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-281">Size of the paper.</span></span> <span data-ttu-id="8e5cf-282">Os tamanhos possíveis são encontrados na propriedade **PaperSizesSupported** da classe de [**\_ impressora Win32**](win32-printer.md) associada.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-282">The possible sizes are found in the **PaperSizesSupported** property of the associated [**Win32\_Printer**](win32-printer.md) class.</span></span>

<span data-ttu-id="8e5cf-283">Exemplo: "A4 ou letra".</span><span class="sxs-lookup"><span data-stu-id="8e5cf-283">Example: "A4 or Letter".</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-284">**PaperWidth**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-284">**PaperWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-285">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-287">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimos de milímetro)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-287">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-288">Largura do papel.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-288">Width of the paper.</span></span> <span data-ttu-id="8e5cf-289">Para determinar o tamanho do papel em polegadas, divida esse valor por 254.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-289">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="8e5cf-290">Exemplo: 2159</span><span class="sxs-lookup"><span data-stu-id="8e5cf-290">Example: 2159</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-291">**PelsHeight**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-291">**PelsHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-292">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-294">Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-294">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-295">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-295">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-296">**PelsWidth**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-296">**PelsWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-297">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-299">Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-299">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-300">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-300">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-301">**PrintQuality**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-301">**PrintQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-302">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-304">Um dos quatro níveis de qualidade do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-304">One of four quality levels of the print job.</span></span> <span data-ttu-id="8e5cf-305">Se um valor positivo for especificado, a qualidade será medida em pontos por polegada.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-305">If a positive value is specified, the quality is measured in dots per inch.</span></span>

<dt>

<span id="-1"></span>

<span data-ttu-id="8e5cf-306"><span id="-1"></span>**-1**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-306"><span id="-1"></span>**-1**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-307">Rascunho</span><span class="sxs-lookup"><span data-stu-id="8e5cf-307">Draft</span></span>

</dd> <dt>

<span id="-2"></span>

<span data-ttu-id="8e5cf-308"><span id="-2"></span>**-2**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-308"><span id="-2"></span>**-2**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-309">Baixo</span><span class="sxs-lookup"><span data-stu-id="8e5cf-309">Low</span></span>

</dd> <dt>

<span id="-3"></span>

<span data-ttu-id="8e5cf-310"><span id="-3"></span>**-3**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-310"><span id="-3"></span>**-3**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-311">Médio</span><span class="sxs-lookup"><span data-stu-id="8e5cf-311">Medium</span></span>

</dd> <dt>

<span id="-4"></span>

<span data-ttu-id="8e5cf-312"><span id="-4"></span>**-4**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-312"><span id="-4"></span>**-4**</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-313">Alto</span><span class="sxs-lookup"><span data-stu-id="8e5cf-313">High</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e5cf-314">**Escala**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-314">**Scale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-315">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-317">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (porcentagem)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-317">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Percent)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-318">Fator pelo qual a saída impressa deve ser dimensionada.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-318">Factor by which the printed output is to be scaled.</span></span> <span data-ttu-id="8e5cf-319">Por exemplo, uma escala de 75 reduz a saída de impressão para 3/4 sua altura e largura originais.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-319">For example, a scale of 75 reduces the print output to 3/4 its original height and width.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-320">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-320">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-323">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-324">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-324">Identifier by which the current object is known.</span></span>

<span data-ttu-id="8e5cf-325">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-325">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-326">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-326">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-327">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-329">Número de versão dos dados de inicialização para o dispositivo associado à impressora baseada no Windows.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-329">Version number of the initialization data for the device associated with the Windows-based printer.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-330">**TTOption**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-330">**TTOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-331">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-333">Indica como as fontes TrueType devem ser impressas.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-333">Indicates how TrueType fonts should be printed.</span></span>

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span data-ttu-id="8e5cf-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-335">Imprime fontes TrueType como elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-335">Prints TrueType fonts as graphics.</span></span> <span data-ttu-id="8e5cf-336">Essa é a ação padrão para impressoras de matriz de pontos.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-336">This is the default action for dot-matrix printers.</span></span>

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span data-ttu-id="8e5cf-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Baixar** (2)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Download** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-338">Baixa fontes TrueType como fontes de disco.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-338">Downloads TrueType fonts as soft fonts.</span></span> <span data-ttu-id="8e5cf-339">Essa é a ação padrão para impressoras que usam a PCL (linguagem de controle de impressora).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-339">This is the default action for printers that use the Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span data-ttu-id="8e5cf-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Substituir** (3)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Substitute** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8e5cf-341">Substitui as fontes de dispositivo por fontes TrueType.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-341">Substitutes device fonts for TrueType fonts.</span></span> <span data-ttu-id="8e5cf-342">Essa é a ação padrão para impressoras PostScript.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-342">This is the default action for PostScript printers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e5cf-343">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-343">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-344">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-346">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (pontos por polegada)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-346">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-347">Resolução de impressão ao longo do eixo y (altura) do trabalho de impressão (semelhante à propriedade **YResolution** obsoleta).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-347">Print resolution along the y-axis (height) of the print job (similar to the obsolete **YResolution** property).</span></span> <span data-ttu-id="8e5cf-348">Esse valor só é definido quando a propriedade **PrintQuality** dessa classe é positiva.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-348">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-349">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-349">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-350">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-350">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-352">Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-352">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-353">Esta propriedade está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-353">This property is obsolete.</span></span> <span data-ttu-id="8e5cf-354">Em vez disso, use a propriedade **HorizontalResolution** .</span><span class="sxs-lookup"><span data-stu-id="8e5cf-354">Use the **HorizontalResolution** property instead.</span></span>

</dd> <dt>

<span data-ttu-id="8e5cf-355">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-355">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e5cf-356">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e5cf-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e5cf-358">Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-358">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e5cf-359">Esta propriedade está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-359">This property is obsolete.</span></span> <span data-ttu-id="8e5cf-360">Em vez disso, use a propriedade **VerticalResolution** .</span><span class="sxs-lookup"><span data-stu-id="8e5cf-360">Use the **VerticalResolution** property instead.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e5cf-361">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e5cf-361">Remarks</span></span>

<span data-ttu-id="8e5cf-362">A classe **Win32 \_ PrinterConfiguration** é derivada da [**\_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-362">The **Win32\_PrinterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="8e5cf-363">**Visão geral**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-363">**Overview**</span></span>

<span data-ttu-id="8e5cf-364">Antes de poder determinar como melhor distribuir e usar seus recursos de impressão, você deve ter um conhecimento detalhado desses recursos.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-364">Before you can determine how to best distribute and use your printing resources, you must have a detailed knowledge of those resources.</span></span> <span data-ttu-id="8e5cf-365">Por exemplo, o departamento A pode ter apenas três impressoras comparadas com cinco impressoras no departamento B. No entanto, se as impressoras no departamento A podem imprimir 20 páginas por minuto e as impressoras no departamento B puderem imprimir apenas 5 páginas por minuto, os usuários no departamento A terão mais capacidade de impressão.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-365">For example, Department A might have only three printers compared with five printers in Department B. However, if the printers in Department A can print 20 pages per minute and the printers in Department B can print only 5 pages per minute, users in Department A actually have more printing capacity.</span></span> <span data-ttu-id="8e5cf-366">Sem conhecer os recursos detalhados dessas impressoras, você pode concluir erroneamente que o departamento A é um pouco da capacidade de impressão e, portanto, comprar impressoras adicionais que acabam ficando sem uso.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-366">Without knowing the detailed capabilities of these printers, you might erroneously conclude that Department A is short on printing capacity and thus purchase additional printers that end up going unused.</span></span>

<span data-ttu-id="8e5cf-367">O WMI inclui duas classes, a [**\_ impressora Win32**](win32-printer.md) e o **Win32 \_ PrinterConfiguration**, que podem ser usados para retornar informações detalhadas sobre todas as impressoras instaladas em um computador.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-367">WMI includes two classes, [**Win32\_Printer**](win32-printer.md) and **Win32\_PrinterConfiguration**, which can be used to return detailed information about all the printers installed on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="8e5cf-368">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e5cf-368">Examples</span></span>

<span data-ttu-id="8e5cf-369">O exemplo de código a seguir recupera as informações da impressora.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-369">The following code sample retrieves printer information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a><span data-ttu-id="8e5cf-370">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e5cf-370">Requirements</span></span>



| <span data-ttu-id="8e5cf-371">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e5cf-371">Requirement</span></span> | <span data-ttu-id="8e5cf-372">Valor</span><span class="sxs-lookup"><span data-stu-id="8e5cf-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5cf-373">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e5cf-373">Minimum supported client</span></span><br/> | <span data-ttu-id="8e5cf-374">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e5cf-374">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="8e5cf-375">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e5cf-375">Minimum supported server</span></span><br/> | <span data-ttu-id="8e5cf-376">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e5cf-376">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="8e5cf-377">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e5cf-377">Namespace</span></span><br/>                | <span data-ttu-id="8e5cf-378">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8e5cf-378">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="8e5cf-379">MOF</span><span class="sxs-lookup"><span data-stu-id="8e5cf-379">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e5cf-380"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="8e5cf-380"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e5cf-381">DLL</span><span class="sxs-lookup"><span data-stu-id="8e5cf-381">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e5cf-382"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e5cf-382"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="8e5cf-383">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e5cf-383">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e5cf-384">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-384">**CIM\_Setting**</span></span>](./cim-setting.md)
</dt> <dt>

[<span data-ttu-id="8e5cf-385">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="8e5cf-385">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
