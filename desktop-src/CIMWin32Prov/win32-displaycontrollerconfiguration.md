---
description: A \_ classe WMI DisplayControllerConfiguration do Win32 representa as informações de configuração do adaptador de vídeo de um sistema de computador executando o Windows.
ms.assetid: 36ebd840-5e8c-411a-828d-38972fe956e2
ms.tgt_platform: multiple
title: Classe Win32_DisplayControllerConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DisplayControllerConfiguration
- Win32_DisplayControllerConfiguration.Caption
- Win32_DisplayControllerConfiguration.Description
- Win32_DisplayControllerConfiguration.SettingID
- Win32_DisplayControllerConfiguration.BitsPerPixel
- Win32_DisplayControllerConfiguration.ColorPlanes
- Win32_DisplayControllerConfiguration.DeviceEntriesInAColorTable
- Win32_DisplayControllerConfiguration.DeviceSpecificPens
- Win32_DisplayControllerConfiguration.HorizontalResolution
- Win32_DisplayControllerConfiguration.Name
- Win32_DisplayControllerConfiguration.RefreshRate
- Win32_DisplayControllerConfiguration.ReservedSystemPaletteEntries
- Win32_DisplayControllerConfiguration.SystemPaletteEntries
- Win32_DisplayControllerConfiguration.VerticalResolution
- Win32_DisplayControllerConfiguration.VideoMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e64f99cb4d4715d9b7a0eb88bd2e7629feed853
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089464"
---
# <a name="win32_displaycontrollerconfiguration-class"></a><span data-ttu-id="69124-103">\_Classe Win32 DisplayControllerConfiguration</span><span class="sxs-lookup"><span data-stu-id="69124-103">Win32\_DisplayControllerConfiguration class</span></span>

<span data-ttu-id="69124-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DisplayControllerConfiguration do Win32** representa as informações de configuração do adaptador de vídeo de um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="69124-104">The **Win32\_DisplayControllerConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the video adapter configuration information of a computer system running Windows.</span></span>

<span data-ttu-id="69124-105">Essa classe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="69124-105">This class is obsolete.</span></span> <span data-ttu-id="69124-106">No lugar dessa classe, você deve usar as propriedades nas classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .</span><span class="sxs-lookup"><span data-stu-id="69124-106">In place of this class, you should use the properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes.</span></span>

<span data-ttu-id="69124-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="69124-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="69124-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="69124-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="69124-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69124-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C4E5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DisplayControllerConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 BitsPerPixel;
  uint32 ColorPlanes;
  uint32 DeviceEntriesInAColorTable;
  uint32 DeviceSpecificPens;
  uint32 HorizontalResolution;
  string Name;
  sint32 RefreshRate;
  uint32 ReservedSystemPaletteEntries;
  uint32 SystemPaletteEntries;
  uint32 VerticalResolution;
  string VideoMode;
};
```

## <a name="members"></a><span data-ttu-id="69124-110">Membros</span><span class="sxs-lookup"><span data-stu-id="69124-110">Members</span></span>

<span data-ttu-id="69124-111">A classe **Win32 \_ DisplayControllerConfiguration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="69124-111">The **Win32\_DisplayControllerConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="69124-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="69124-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69124-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="69124-113">Properties</span></span>

<span data-ttu-id="69124-114">A classe **Win32 \_ DisplayControllerConfiguration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="69124-114">The **Win32\_DisplayControllerConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69124-115">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="69124-115">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-116">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69124-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="69124-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-118">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")</span><span class="sxs-lookup"><span data-stu-id="69124-118">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="69124-119">O número de bits usados para representar a cor nessa configuração ou os bits em cada pixel.</span><span class="sxs-lookup"><span data-stu-id="69124-119">Either the number of bits used to represent the color in this configuration, or the bits in each pixel.</span></span>

<span data-ttu-id="69124-120">Exemplo: 8</span><span class="sxs-lookup"><span data-stu-id="69124-120">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="69124-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="69124-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="69124-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69124-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-124">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="69124-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="69124-125">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="69124-125">Short textual description of the current object.</span></span>

<span data-ttu-id="69124-126">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="69124-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="69124-127">**ColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="69124-127">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69124-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="69124-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-130">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api planos de \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| ")</span><span class="sxs-lookup"><span data-stu-id="69124-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="69124-131">Número atual de planos de cores usados na configuração de exibição.</span><span class="sxs-lookup"><span data-stu-id="69124-131">Current number of color planes used in the display configuration.</span></span> <span data-ttu-id="69124-132">Um plano de cores é outra maneira de representar cores de pixel.</span><span class="sxs-lookup"><span data-stu-id="69124-132">A color plane is another way to represent pixel colors.</span></span> <span data-ttu-id="69124-133">Em vez de atribuir um único valor RGB a cada pixel, os planos de cores separam o gráfico em cada um dos componentes de cor primária (vermelho, verde, azul) e os armazena em seus próprios planos.</span><span class="sxs-lookup"><span data-stu-id="69124-133">Instead of assigning a single RGB value to each pixel, color planes separate the graphic into each of the primary color components (red, green, blue), and stores them in their own planes.</span></span> <span data-ttu-id="69124-134">Isso permite mais profundidades de cor em sistemas de vídeo de 8 e 16 bits.</span><span class="sxs-lookup"><span data-stu-id="69124-134">This allows for greater color depths on 8-bit and 16-bit video systems.</span></span> <span data-ttu-id="69124-135">Os sistemas gráficos presentes têm o bitwidth grande o suficiente para armazenar informações de profundidade de cor, o que significa que apenas um plano de cores é necessário.</span><span class="sxs-lookup"><span data-stu-id="69124-135">Present graphics systems have the bitwidth large enough to store color depth information, meaning only one color plane is needed.</span></span>

<span data-ttu-id="69124-136">Example: 1</span><span class="sxs-lookup"><span data-stu-id="69124-136">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="69124-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="69124-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="69124-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69124-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69124-140">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="69124-140">Textual description of the current object.</span></span>

<span data-ttu-id="69124-141">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="69124-141">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="69124-142">**DeviceEntriesInAColorTable**</span><span class="sxs-lookup"><span data-stu-id="69124-142">**DeviceEntriesInAColorTable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-143">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69124-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="69124-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-145">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")</span><span class="sxs-lookup"><span data-stu-id="69124-145">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="69124-146">Número de índices de cores em uma tabela de cores de um dispositivo de vídeo (se o dispositivo tiver uma profundidade de cor de no máximo 8 bits por pixel).</span><span class="sxs-lookup"><span data-stu-id="69124-146">Number of color indexes in a color table of a display device (if the device has a color depth of no more than 8 bits per pixel).</span></span> <span data-ttu-id="69124-147">Para dispositivos com mais profundidades de cor,-1 é retornado.</span><span class="sxs-lookup"><span data-stu-id="69124-147">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="69124-148">Exemplo: 256</span><span class="sxs-lookup"><span data-stu-id="69124-148">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="69124-149">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="69124-149">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69124-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="69124-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-152">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")</span><span class="sxs-lookup"><span data-stu-id="69124-152">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="69124-153">Número atual de canetas específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69124-153">Current number of device-specific pens.</span></span> <span data-ttu-id="69124-154">Um valor de 0xFFFFFFFF significa que o dispositivo não dá suporte a canetas.</span><span class="sxs-lookup"><span data-stu-id="69124-154">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="69124-155">As canetas são propriedades lógicas que podem ser atribuídas pelo controlador de vídeo para exibir dispositivos e são usadas para desenhar linhas, bordas de polígonos e texto.</span><span class="sxs-lookup"><span data-stu-id="69124-155">Pens are logical properties that can be assigned by the display controller to display devices, and are used to draw lines, borders of polygons, and text.</span></span>

<span data-ttu-id="69124-156">Exemplo: 3</span><span class="sxs-lookup"><span data-stu-id="69124-156">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="69124-157">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="69124-157">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-158">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69124-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="69124-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-160">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span><span class="sxs-lookup"><span data-stu-id="69124-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="69124-161">Número atual de pixels na direção horizontal (eixo x) da exibição.</span><span class="sxs-lookup"><span data-stu-id="69124-161">Current number of pixels in the horizontal direction (x-axis) of the display.</span></span>

<span data-ttu-id="69124-162">Exemplo: 1024</span><span class="sxs-lookup"><span data-stu-id="69124-162">Example: 1024</span></span>

</dd> <dt>

<span data-ttu-id="69124-163">**Nome**</span><span class="sxs-lookup"><span data-stu-id="69124-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="69124-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69124-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-166">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="69124-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="69124-167">Nome do adaptador usado nesta configuração.</span><span class="sxs-lookup"><span data-stu-id="69124-167">Name of the adapter used in this configuration.</span></span>

</dd> <dt>

<span data-ttu-id="69124-168">**Taxa_de_atualização**</span><span class="sxs-lookup"><span data-stu-id="69124-168">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-169">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="69124-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="69124-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-171">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRESVREFRESH"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="69124-171">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRESVREFRESH"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="69124-172">Taxa de atualização do adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="69124-172">Refresh rate of the video adapter.</span></span> <span data-ttu-id="69124-173">Um valor de 0 (zero) ou 1 (um) indica que uma taxa padrão está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="69124-173">A value of 0 (zero) or 1 (one) indicates a default rate is being used.</span></span> <span data-ttu-id="69124-174">Um valor de-1 indica que uma taxa ideal está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="69124-174">A value of -1 indicates that an optimal rate is being used.</span></span>

<span data-ttu-id="69124-175">Exemplo: 72</span><span class="sxs-lookup"><span data-stu-id="69124-175">Example: 72</span></span>

</dd> <dt>

<span data-ttu-id="69124-176">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="69124-176">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-177">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69124-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="69124-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-179">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")</span><span class="sxs-lookup"><span data-stu-id="69124-179">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="69124-180">Número atual de entradas de índice de cor reservadas para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="69124-180">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="69124-181">Esse valor só é válido para configurações de exibição que usam uma paleta indexada.</span><span class="sxs-lookup"><span data-stu-id="69124-181">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="69124-182">As paletas indexadas não são usadas para profundidades de cor maiores que 8 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="69124-182">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="69124-183">Se a profundidade de cor tiver mais de 8 bits por pixel, esse valor será definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="69124-183">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="69124-184">Exemplo: 20</span><span class="sxs-lookup"><span data-stu-id="69124-184">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="69124-185">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="69124-185">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="69124-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69124-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-188">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="69124-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="69124-189">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="69124-189">Identifier by which the current object is known.</span></span>

<span data-ttu-id="69124-190">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="69124-190">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="69124-191">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="69124-191">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-192">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69124-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="69124-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-194">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")</span><span class="sxs-lookup"><span data-stu-id="69124-194">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="69124-195">Número atual de entradas de índice de cor reservadas para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="69124-195">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="69124-196">Esse valor só é válido para configurações de exibição que usam uma paleta indexada.</span><span class="sxs-lookup"><span data-stu-id="69124-196">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="69124-197">As paletas indexadas não são usadas para profundidades de cor maiores que 8 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="69124-197">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="69124-198">Se a profundidade de cor tiver mais de 8 bits por pixel, esse valor será definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="69124-198">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="69124-199">Exemplo: 20</span><span class="sxs-lookup"><span data-stu-id="69124-199">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="69124-200">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="69124-200">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-201">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69124-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="69124-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-203">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span><span class="sxs-lookup"><span data-stu-id="69124-203">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="69124-204">Número atual de pixels na direção vertical (eixo y) da exibição.</span><span class="sxs-lookup"><span data-stu-id="69124-204">Current number of pixels in the vertical direction (y-axis) of the display.</span></span>

<span data-ttu-id="69124-205">Exemplo: 768</span><span class="sxs-lookup"><span data-stu-id="69124-205">Example: 768</span></span>

</dd> <dt>

<span data-ttu-id="69124-206">**Videomode**</span><span class="sxs-lookup"><span data-stu-id="69124-206">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69124-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="69124-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69124-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="69124-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69124-209">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="69124-209">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="69124-210">Descrição legível pelo usuário da atual resolução de tela e configuração de cor da exibição.</span><span class="sxs-lookup"><span data-stu-id="69124-210">User-readable description of the current screen resolution and color setting of the display.</span></span>

<span data-ttu-id="69124-211">Exemplo: "1024 768 com 256 cores"</span><span class="sxs-lookup"><span data-stu-id="69124-211">Example: "1024   768 with 256 colors"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69124-212">Comentários</span><span class="sxs-lookup"><span data-stu-id="69124-212">Remarks</span></span>

<span data-ttu-id="69124-213">A classe **Win32 \_ DisplayControllerConfiguration** é derivada da [**\_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="69124-213">The **Win32\_DisplayControllerConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69124-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69124-214">Requirements</span></span>



| <span data-ttu-id="69124-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="69124-215">Requirement</span></span> | <span data-ttu-id="69124-216">Valor</span><span class="sxs-lookup"><span data-stu-id="69124-216">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69124-217">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69124-217">Minimum supported client</span></span><br/> | <span data-ttu-id="69124-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69124-218">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="69124-219">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69124-219">Minimum supported server</span></span><br/> | <span data-ttu-id="69124-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69124-220">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69124-221">Namespace</span><span class="sxs-lookup"><span data-stu-id="69124-221">Namespace</span></span><br/>                | <span data-ttu-id="69124-222">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="69124-222">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="69124-223">MOF</span><span class="sxs-lookup"><span data-stu-id="69124-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69124-224"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69124-224"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="69124-225">DLL</span><span class="sxs-lookup"><span data-stu-id="69124-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69124-226"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69124-226"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69124-227">Confira também</span><span class="sxs-lookup"><span data-stu-id="69124-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69124-228">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="69124-228">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="69124-229">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="69124-229">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

