---
description: A \_ classe Win32 VideoConfiguration não está ativa. Ele não retornará nenhuma instância, pois não há nenhum provedor fazendo backup dele.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Classe Win32_VideoConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96ad4206cc50953a135b23257526ffb5cdc59b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500836"
---
# <a name="win32_videoconfiguration-class"></a><span data-ttu-id="b919b-104">\_Classe Win32 VideoConfiguration</span><span class="sxs-lookup"><span data-stu-id="b919b-104">Win32\_VideoConfiguration class</span></span>

<span data-ttu-id="b919b-105">A classe **Win32 \_ VideoConfiguration** não está ativa.</span><span class="sxs-lookup"><span data-stu-id="b919b-105">The **Win32\_VideoConfiguration** class is not active.</span></span> <span data-ttu-id="b919b-106">Ele não retornará nenhuma instância, pois não há nenhum provedor fazendo backup dele.</span><span class="sxs-lookup"><span data-stu-id="b919b-106">It will not return any instances as there is no provider backing it.</span></span>

<span data-ttu-id="b919b-107">A classe **Win32 \_ VideoConfiguration** representa uma configuração de um subsistema de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-107">The **Win32\_VideoConfiguration** class represents a configuration of a video subsystem.</span></span> <span data-ttu-id="b919b-108">Essa classe foi preterida em favor das propriedades contidas nas classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)</span><span class="sxs-lookup"><span data-stu-id="b919b-108">This class has been deprecated in favor of the properties contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes</span></span>

<span data-ttu-id="b919b-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b919b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b919b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b919b-110">Syntax</span></span>

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="b919b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b919b-111">Members</span></span>

<span data-ttu-id="b919b-112">A classe **Win32 \_ VideoConfiguration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b919b-112">The **Win32\_VideoConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="b919b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b919b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b919b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b919b-114">Properties</span></span>

<span data-ttu-id="b919b-115">A classe **Win32 \_ VideoConfiguration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b919b-115">The **Win32\_VideoConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b919b-116">**ActualColorResolution**</span><span class="sxs-lookup"><span data-stu-id="b919b-116">**ActualColorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-117">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-119">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| COLORRES"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por pixel")</span><span class="sxs-lookup"><span data-stu-id="b919b-119">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|COLORRES"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per pixel")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-120">Indica a intensidade de cor atual da exibição do vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-120">Indicates the current color depth of the video display.</span></span>

<span data-ttu-id="b919b-121">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-121">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-122">**AdapterChipType**</span><span class="sxs-lookup"><span data-stu-id="b919b-122">**AdapterChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-125">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| chiptype")</span><span class="sxs-lookup"><span data-stu-id="b919b-125">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|ChipType")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-126">Contém o nome do chip do adaptador.</span><span class="sxs-lookup"><span data-stu-id="b919b-126">Contains the name of the adapter chip.</span></span>

<span data-ttu-id="b919b-127">Exemplo: S3</span><span class="sxs-lookup"><span data-stu-id="b919b-127">Example: s3</span></span>

<span data-ttu-id="b919b-128">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-128">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-129">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="b919b-129">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-132">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**chave**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b919b-132">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-133">Especifica o nome do fabricante do adaptador.</span><span class="sxs-lookup"><span data-stu-id="b919b-133">Specifies the name of the manufacturer of the adapter.</span></span> <span data-ttu-id="b919b-134">Esse nome pode ser usado para comparar a compatibilidade desse dispositivo com as necessidades do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="b919b-134">This name can be used to compare the compatibility of this device with the needs of the computer system.</span></span>

<span data-ttu-id="b919b-135">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-135">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-136">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="b919b-136">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-139">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| DACType")</span><span class="sxs-lookup"><span data-stu-id="b919b-139">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|DACType")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-140">Indica o nome do chip digital para analógico (DAC) usado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="b919b-140">Indicates the name of the digital-to-analog chip (DAC) used in the adapter.</span></span>

<span data-ttu-id="b919b-141">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-141">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-142">**AdapterDescription**</span><span class="sxs-lookup"><span data-stu-id="b919b-142">**AdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-145">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b919b-145">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-146">Contém uma descrição ou um nome descritivo do adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-146">Contains a description or descriptive name of the video adapter.</span></span>

<span data-ttu-id="b919b-147">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-147">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-148">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="b919b-148">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-151">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b919b-151">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-152">Indica o tamanho da memória do adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-152">Indicates the memory size of the video adapter.</span></span>

<span data-ttu-id="b919b-153">Exemplo: 16777216</span><span class="sxs-lookup"><span data-stu-id="b919b-153">Example: 16777216</span></span>

<span data-ttu-id="b919b-154">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-154">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-155">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="b919b-155">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-158">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry o \| sistema de descrição de hardware \\ \\ \\ \\ \\ \\ DisplayController \\ \\ 0 \\ \\ identificador")</span><span class="sxs-lookup"><span data-stu-id="b919b-158">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\DisplayController\\\\0\\\\Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-159">Indica o tipo de adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-159">Indicates the type of video adapter.</span></span>

<span data-ttu-id="b919b-160">Conjunto de caracteres: alfanumérico</span><span class="sxs-lookup"><span data-stu-id="b919b-160">Character Set: Alphanumeric</span></span>

<span data-ttu-id="b919b-161">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-161">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-162">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="b919b-162">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-163">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-165">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")</span><span class="sxs-lookup"><span data-stu-id="b919b-165">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-166">Indica o número real de bits por pixel que representa a exibição.</span><span class="sxs-lookup"><span data-stu-id="b919b-166">Indicates the actual number of bits per pixel representing the display.</span></span> <span data-ttu-id="b919b-167">Isso pode ser dimensionado para a configuração de vídeo atual (representada pela propriedade ActualColorResolution) do usuário.</span><span class="sxs-lookup"><span data-stu-id="b919b-167">This may be scaled to the current video setting (represented by the ActualColorResolution property) of the user.</span></span>

<span data-ttu-id="b919b-168">Exemplo: 8</span><span class="sxs-lookup"><span data-stu-id="b919b-168">Example: 8</span></span>

<span data-ttu-id="b919b-169">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-169">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-170">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b919b-170">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-173">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="b919b-173">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b919b-174">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="b919b-174">Short textual description of the current object.</span></span>

<span data-ttu-id="b919b-175">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-175">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-176">**ColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="b919b-176">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-177">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-179">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api planos de \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| ")</span><span class="sxs-lookup"><span data-stu-id="b919b-179">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-180">Indica o número atual de planos de cores usados na exibição do vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-180">Indicates the current number of color planes used in the video display.</span></span> <span data-ttu-id="b919b-181">Um plano de cores é outra maneira de representar cores de pixel; em vez de atribuir um único valor RGB a cada pixel, os planos de cores separam o gráfico em cada um dos componentes de cor primária (vermelho verde azul) e os armazenam em seus próprios planos.</span><span class="sxs-lookup"><span data-stu-id="b919b-181">A color plane is another way to represent pixel colors; instead of assigning a single RGB value to each a pixel, color planes separate the graphic into each of the primary color components (red green blue), and store them in their own planes.</span></span> <span data-ttu-id="b919b-182">Isso permite mais profundidades de cor em sistemas de vídeo de 8 e 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b919b-182">This allows for greater color depths on 8 and 16 bit video systems.</span></span> <span data-ttu-id="b919b-183">Os sistemas gráficos apresentam o bitwidth grande o suficiente para armazenar informações de profundidade de cor, tornando apenas um plano de cores necessário.</span><span class="sxs-lookup"><span data-stu-id="b919b-183">Present graphics systems have the bitwidth large enough to store color depth information, making only one color plane necessary.</span></span>

<span data-ttu-id="b919b-184">Example: 1</span><span class="sxs-lookup"><span data-stu-id="b919b-184">Example: 1</span></span>

<span data-ttu-id="b919b-185">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-185">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-186">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="b919b-186">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-187">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-189">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")</span><span class="sxs-lookup"><span data-stu-id="b919b-189">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-190">Indica o número de índices de cores em uma tabela de cores para uma exibição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-190">Indicates the number of color indexes in a color table for a video display.</span></span> <span data-ttu-id="b919b-191">Essa propriedade será usada se o dispositivo tiver uma profundidade de cor de no máximo 8 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="b919b-191">This property is used if the device has a color depth of no more than 8 bits per pixel.</span></span> <span data-ttu-id="b919b-192">Para dispositivos com mais profundidades de cor,-1 é retornado.</span><span class="sxs-lookup"><span data-stu-id="b919b-192">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="b919b-193">Exemplo: 256</span><span class="sxs-lookup"><span data-stu-id="b919b-193">Example: 256</span></span>

<span data-ttu-id="b919b-194">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-194">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-195">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b919b-195">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b919b-198">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="b919b-198">Textual description of the current object.</span></span>

<span data-ttu-id="b919b-199">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-199">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-200">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="b919b-200">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-201">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-203">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")</span><span class="sxs-lookup"><span data-stu-id="b919b-203">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-204">Indica o número atual de canetas específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b919b-204">Indicates the current number of device-specific pens.</span></span> <span data-ttu-id="b919b-205">Um valor de 0xFFFFFFFF significa que o dispositivo não dá suporte a canetas.</span><span class="sxs-lookup"><span data-stu-id="b919b-205">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="b919b-206">As canetas são usadas para desenhar linhas e bordas de objetos poligonal.</span><span class="sxs-lookup"><span data-stu-id="b919b-206">Pens are used to draw lines and theborders of polygonal objects.</span></span>

<span data-ttu-id="b919b-207">Exemplo: 3</span><span class="sxs-lookup"><span data-stu-id="b919b-207">Example: 3</span></span>

<span data-ttu-id="b919b-208">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-208">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-209">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="b919b-209">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-210">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b919b-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-212">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ AdapterDescription \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="b919b-212">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\AdapterDescription\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-213">Indica a data e a hora em que o driver de vídeo atual foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b919b-213">Indicates the date and time the current video driver was installed.</span></span>

<span data-ttu-id="b919b-214">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-214">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-215">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="b919b-215">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-216">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-218">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES")</span><span class="sxs-lookup"><span data-stu-id="b919b-218">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-219">Indica o número atual de pixels na direção horizontal (eixo X) da exibição.</span><span class="sxs-lookup"><span data-stu-id="b919b-219">Indicates the current number of pixels in the horizontal direction (X axis) of the display.</span></span>

<span data-ttu-id="b919b-220">Exemplo: 1024</span><span class="sxs-lookup"><span data-stu-id="b919b-220">Example: 1024</span></span>

<span data-ttu-id="b919b-221">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-221">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-222">**InfFilename**</span><span class="sxs-lookup"><span data-stu-id="b919b-222">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-225">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="b919b-225">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-226">Especifica o caminho para o arquivo. inf do driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-226">Specifies the path to the .inf file of the video driver.</span></span>

<span data-ttu-id="b919b-227">Exemplo: C: \\ drivers do Windows \\ System32 \\</span><span class="sxs-lookup"><span data-stu-id="b919b-227">Example: C:\\Windows\\System32\\Drivers</span></span>

<span data-ttu-id="b919b-228">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-228">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-229">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="b919b-229">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-232">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="b919b-232">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-233">Indica a seção do arquivo. inf onde residem as informações de vídeo do Win32.</span><span class="sxs-lookup"><span data-stu-id="b919b-233">Indicates the section of the .inf file where the Win32 video information resides.</span></span>

<span data-ttu-id="b919b-234">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-234">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-235">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="b919b-235">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-236">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-238">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Defaule \| drv")</span><span class="sxs-lookup"><span data-stu-id="b919b-238">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Defaule\|drv")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-239">Indica o nome do driver de vídeo instalado.</span><span class="sxs-lookup"><span data-stu-id="b919b-239">Indicates the name of the installed video driver.</span></span>

<span data-ttu-id="b919b-240">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-240">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-241">**MonitorManufacturer**</span><span class="sxs-lookup"><span data-stu-id="b919b-241">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-244">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b919b-244">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-245">Indica o nome do fabricante do dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-245">Indicates the name of the manufacturer of the display device.</span></span>

<span data-ttu-id="b919b-246">Exemplo: NEC</span><span class="sxs-lookup"><span data-stu-id="b919b-246">Example: NEC</span></span>

<span data-ttu-id="b919b-247">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-247">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-248">**Monitor**</span><span class="sxs-lookup"><span data-stu-id="b919b-248">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-251">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry o \| sistema de descrição de hardware \\ \\ \\ \\ \\ \\ MonitorPeripheral \\ \\ 0 \| identificador")</span><span class="sxs-lookup"><span data-stu-id="b919b-251">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\MonitorPeripheral\\\\0\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-252">Indica o nome do modelo do dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-252">Indicates the model name of the display device.</span></span>

<span data-ttu-id="b919b-253">Exemplo: NEC 5FGp</span><span class="sxs-lookup"><span data-stu-id="b919b-253">Example: NEC 5FGp</span></span>

<span data-ttu-id="b919b-254">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-254">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-255">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b919b-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-256">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-258">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**chave**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b919b-258">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-259">Contém um nome de identificação para a classe de configuração de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-259">Contains an identifying name for the video configuration class.</span></span>

<span data-ttu-id="b919b-260">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-260">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-261">**PixelsPerXLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="b919b-261">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-262">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-264">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSX")</span><span class="sxs-lookup"><span data-stu-id="b919b-264">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSX")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-265">Indica o número de pixels por polegada lógica ao longo do eixo X (direção horizontal) da exibição.</span><span class="sxs-lookup"><span data-stu-id="b919b-265">Indicates the number of pixels per logical inch along the X axis (horizontal direction) of the display.</span></span>

<span data-ttu-id="b919b-266">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-266">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-267">**PixelsPerYLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="b919b-267">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-268">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-270">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSY")</span><span class="sxs-lookup"><span data-stu-id="b919b-270">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSY")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-271">Indica o número de pixels por polegada lógica ao longo do eixo Y (direção vertical) da exibição.</span><span class="sxs-lookup"><span data-stu-id="b919b-271">Indicates the number of pixels per logical inch along the Y axis (vertical direction) of the display.</span></span>

<span data-ttu-id="b919b-272">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-272">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-273">**Taxa_de_atualização**</span><span class="sxs-lookup"><span data-stu-id="b919b-273">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-274">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-276">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VREFRESH")</span><span class="sxs-lookup"><span data-stu-id="b919b-276">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VREFRESH")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-277">Indica a taxa de atualização da configuração de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b919b-277">Indicates the refresh rate of the video configuration.</span></span> <span data-ttu-id="b919b-278">Um valor de 0 ou 1 indica que uma taxa padrão está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="b919b-278">A value of 0 or 1 indicates a default rate is being used.</span></span>

<span data-ttu-id="b919b-279">Exemplo: 72</span><span class="sxs-lookup"><span data-stu-id="b919b-279">Example: 72</span></span>

<span data-ttu-id="b919b-280">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-280">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-281">**Scanmode**</span><span class="sxs-lookup"><span data-stu-id="b919b-281">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-284">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| DefaultSettings. entrelaçado")</span><span class="sxs-lookup"><span data-stu-id="b919b-284">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Device0\|DefaultSettings.Interlaced")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-285">Indica se o dispositivo de vídeo está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="b919b-285">Indicates whether the display device is interlaced.</span></span>

<span data-ttu-id="b919b-286">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-286">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="b919b-287">**Não entrelaçado** ("não entrelaçado")</span><span class="sxs-lookup"><span data-stu-id="b919b-287">**Non Interlaced** ("Non Interlaced")</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="b919b-288">**Entrelaçado** ("entrelaçado")</span><span class="sxs-lookup"><span data-stu-id="b919b-288">**Interlaced** ("Interlaced")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b919b-289">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="b919b-289">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-290">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-292">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTSIZE"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milímetros")</span><span class="sxs-lookup"><span data-stu-id="b919b-292">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-293">Especifica a altura da tela física.</span><span class="sxs-lookup"><span data-stu-id="b919b-293">Specifies the height of the physical screen.</span></span>

<span data-ttu-id="b919b-294">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-294">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-295">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="b919b-295">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-296">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-298">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZSIZE"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milímetros")</span><span class="sxs-lookup"><span data-stu-id="b919b-298">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-299">Especifica a largura da tela física.</span><span class="sxs-lookup"><span data-stu-id="b919b-299">Specifies the width of the physical screen.</span></span>

<span data-ttu-id="b919b-300">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-300">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-301">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="b919b-301">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-302">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b919b-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-304">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="b919b-304">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b919b-305">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b919b-305">Identifier by which the current object is known.</span></span>

<span data-ttu-id="b919b-306">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-306">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-307">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="b919b-307">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-308">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-310">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE")</span><span class="sxs-lookup"><span data-stu-id="b919b-310">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|SIZEPALETTE")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-311">Iindicates o número atual de entradas de índice de cor reservadas para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="b919b-311">Iindicates the current number of color index entries reserved for system use.</span></span> <span data-ttu-id="b919b-312">Esse valor só é válido para configurações de exibição que usam uma paleta indexada.</span><span class="sxs-lookup"><span data-stu-id="b919b-312">This value is only valid for display settings that use an indexed palette .</span></span> <span data-ttu-id="b919b-313">As paletas indexadas não são usadas para profundidades de cor maiores que 8 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="b919b-313">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="b919b-314">Se a profundidade de cor tiver mais de 8 bits por pixel, esse valor será definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b919b-314">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="b919b-315">Exemplo: 20</span><span class="sxs-lookup"><span data-stu-id="b919b-315">Example: 20</span></span>

<span data-ttu-id="b919b-316">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-316">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="b919b-317">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="b919b-317">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b919b-318">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b919b-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b919b-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b919b-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b919b-320">Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES")</span><span class="sxs-lookup"><span data-stu-id="b919b-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES")</span></span>
</dt> </dl>

<span data-ttu-id="b919b-321">Indica o número atual de pixels na direção vertical (eixo Y) da exibição.</span><span class="sxs-lookup"><span data-stu-id="b919b-321">Indicates the current number of pixels in the vertical direction (Y axis) of the display.</span></span>

<span data-ttu-id="b919b-322">Exemplo: 768</span><span class="sxs-lookup"><span data-stu-id="b919b-322">Example: 768</span></span>

<span data-ttu-id="b919b-323">Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="b919b-323">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b919b-324">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b919b-324">Requirements</span></span>



| <span data-ttu-id="b919b-325">Requisito</span><span class="sxs-lookup"><span data-stu-id="b919b-325">Requirement</span></span> | <span data-ttu-id="b919b-326">Valor</span><span class="sxs-lookup"><span data-stu-id="b919b-326">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b919b-327">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b919b-327">Minimum supported client</span></span><br/> | <span data-ttu-id="b919b-328">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b919b-328">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b919b-329">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b919b-329">Minimum supported server</span></span><br/> | <span data-ttu-id="b919b-330">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b919b-330">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b919b-331">Namespace</span><span class="sxs-lookup"><span data-stu-id="b919b-331">Namespace</span></span><br/>                | <span data-ttu-id="b919b-332">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b919b-332">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b919b-333">MOF</span><span class="sxs-lookup"><span data-stu-id="b919b-333">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b919b-334"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b919b-334"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b919b-335">DLL</span><span class="sxs-lookup"><span data-stu-id="b919b-335">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b919b-336"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b919b-336"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b919b-337">Confira também</span><span class="sxs-lookup"><span data-stu-id="b919b-337">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b919b-338">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b919b-338">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

 
