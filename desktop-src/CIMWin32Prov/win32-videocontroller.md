---
description: Representa os recursos e a capacidade de gerenciamento do controlador de vídeo em um sistema de computador executando o Windows.
ms.assetid: 5c81994b-4a84-46ff-8689-09998dc66f91
ms.tgt_platform: multiple
title: Classe Win32_VideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoController
- Win32_VideoController.Reset
- Win32_VideoController.SetPowerState
- Win32_VideoController.AcceleratorCapabilities
- Win32_VideoController.AdapterCompatibility
- Win32_VideoController.AdapterDACType
- Win32_VideoController.AdapterRAM
- Win32_VideoController.Availability
- Win32_VideoController.CapabilityDescriptions
- Win32_VideoController.Caption
- Win32_VideoController.ColorTableEntries
- Win32_VideoController.ConfigManagerErrorCode
- Win32_VideoController.ConfigManagerUserConfig
- Win32_VideoController.CreationClassName
- Win32_VideoController.CurrentBitsPerPixel
- Win32_VideoController.CurrentHorizontalResolution
- Win32_VideoController.CurrentNumberOfColors
- Win32_VideoController.CurrentNumberOfColumns
- Win32_VideoController.CurrentNumberOfRows
- Win32_VideoController.CurrentRefreshRate
- Win32_VideoController.CurrentScanMode
- Win32_VideoController.CurrentVerticalResolution
- Win32_VideoController.Description
- Win32_VideoController.DeviceID
- Win32_VideoController.DeviceSpecificPens
- Win32_VideoController.DitherType
- Win32_VideoController.DriverDate
- Win32_VideoController.DriverVersion
- Win32_VideoController.ErrorCleared
- Win32_VideoController.ErrorDescription
- Win32_VideoController.ICMIntent
- Win32_VideoController.ICMMethod
- Win32_VideoController.InfFilename
- Win32_VideoController.InfSection
- Win32_VideoController.InstallDate
- Win32_VideoController.InstalledDisplayDrivers
- Win32_VideoController.LastErrorCode
- Win32_VideoController.MaxMemorySupported
- Win32_VideoController.MaxNumberControlled
- Win32_VideoController.MaxRefreshRate
- Win32_VideoController.MinRefreshRate
- Win32_VideoController.Monochrome
- Win32_VideoController.Name
- Win32_VideoController.NumberOfColorPlanes
- Win32_VideoController.NumberOfVideoPages
- Win32_VideoController.PNPDeviceID
- Win32_VideoController.PowerManagementCapabilities
- Win32_VideoController.PowerManagementSupported
- Win32_VideoController.ProtocolSupported
- Win32_VideoController.ReservedSystemPaletteEntries
- Win32_VideoController.SpecificationVersion
- Win32_VideoController.Status
- Win32_VideoController.StatusInfo
- Win32_VideoController.SystemCreationClassName
- Win32_VideoController.SystemName
- Win32_VideoController.SystemPaletteEntries
- Win32_VideoController.TimeOfLastReset
- Win32_VideoController.VideoArchitecture
- Win32_VideoController.VideoMemoryType
- Win32_VideoController.VideoMode
- Win32_VideoController.VideoModeDescription
- Win32_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deb6903ba6cf27170539281da90569a14471999c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456887"
---
# <a name="win32_videocontroller-class"></a><span data-ttu-id="93345-103">\_Classe Win32 VideoController</span><span class="sxs-lookup"><span data-stu-id="93345-103">Win32\_VideoController class</span></span>

<span data-ttu-id="93345-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ VideoController do Win32** representa os recursos e a capacidade de gerenciamento do controlador de vídeo em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="93345-104">The **Win32\_VideoController** [WMI class](../wmisdk/retrieving-a-class.md) represents the capabilities and management capacity of the video controller on a computer system running Windows.</span></span>

<span data-ttu-id="93345-105">O hardware que não é compatível com o Windows Display Driver Model (WDDM) retorna valores de propriedade imprecisos para instâncias dessa classe.</span><span class="sxs-lookup"><span data-stu-id="93345-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="93345-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="93345-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="93345-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="93345-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="93345-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93345-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF1-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoController : CIM_PCVideoController
{
  uint16   AcceleratorCapabilities[];
  string   AdapterCompatibility;
  string   AdapterDACType;
  uint32   AdapterRAM;
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ColorTableEntries;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint64   CurrentNumberOfColors;
  uint32   CurrentNumberOfColumns;
  uint32   CurrentNumberOfRows;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  uint32   CurrentVerticalResolution;
  string   Description;
  string   DeviceID;
  uint32   DeviceSpecificPens;
  uint32   DitherType;
  datetime DriverDate;
  string   DriverVersion;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   ICMIntent;
  uint32   ICMMethod;
  string   InfFilename;
  string   InfSection;
  datetime InstallDate;
  string   InstalledDisplayDrivers;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  boolean  Monochrome;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  uint32   ReservedSystemPaletteEntries;
  uint32   SpecificationVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   SystemPaletteEntries;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoModeDescription;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="93345-109">Membros</span><span class="sxs-lookup"><span data-stu-id="93345-109">Members</span></span>

<span data-ttu-id="93345-110">A classe **Win32 \_ VideoController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="93345-110">The **Win32\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="93345-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="93345-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="93345-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="93345-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="93345-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="93345-113">Methods</span></span>

<span data-ttu-id="93345-114">A classe **Win32 \_ VideoController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="93345-114">The **Win32\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="93345-115">Método</span><span class="sxs-lookup"><span data-stu-id="93345-115">Method</span></span>            | <span data-ttu-id="93345-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="93345-116">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93345-117">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="93345-117">**Reset**</span></span>         | <span data-ttu-id="93345-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="93345-118">Not implemented.</span></span> <span data-ttu-id="93345-119">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/>                 |
| <span data-ttu-id="93345-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="93345-120">**SetPowerState**</span></span> | <span data-ttu-id="93345-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="93345-121">Not implemented.</span></span> <span data-ttu-id="93345-122">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="93345-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="93345-123">Properties</span></span>

<span data-ttu-id="93345-124">A classe **Win32 \_ VideoController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="93345-124">The **Win32\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93345-125">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="93345-125">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-126">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93345-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93345-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-128">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="93345-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="93345-129">Matriz de elementos gráficos e recursos 3-D do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-129">Array of graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="93345-130">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-130">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93345-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="93345-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="93345-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="93345-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="93345-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Acelerador de gráficos** (2)</span><span class="sxs-lookup"><span data-stu-id="93345-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="93345-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**acelerador 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="93345-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="93345-135">Acelerador 3D</span><span class="sxs-lookup"><span data-stu-id="93345-135">3-D Accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-136">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="93345-136">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-139">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="93345-139">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="93345-140">O chipset geral usado para esse controlador comparar as compatibilidades com o sistema.</span><span class="sxs-lookup"><span data-stu-id="93345-140">General chipset used for this controller to compare compatibilities with the system.</span></span>

</dd> <dt>

<span data-ttu-id="93345-141">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="93345-141">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-144">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation. DACType")</span><span class="sxs-lookup"><span data-stu-id="93345-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.DACType")</span></span>
</dt> </dl>

<span data-ttu-id="93345-145">Nome ou identificador do chip do conversor digital para analógico (DAC).</span><span class="sxs-lookup"><span data-stu-id="93345-145">Name or identifier of the digital-to-analog converter (DAC) chip.</span></span> <span data-ttu-id="93345-146">O conjunto de caracteres dessa propriedade é alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="93345-146">The character set of this property is alphanumeric.</span></span>

</dd> <dt>

<span data-ttu-id="93345-147">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="93345-147">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-148">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-150">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation. MemorySize"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="93345-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.MemorySize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="93345-151">Tamanho da memória do adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-151">Memory size of the video adapter.</span></span>

<span data-ttu-id="93345-152">Exemplo: 64000</span><span class="sxs-lookup"><span data-stu-id="93345-152">Example: 64000</span></span>

</dd> <dt>

<span data-ttu-id="93345-153">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="93345-153">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-154">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93345-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93345-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-156">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="93345-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="93345-157">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93345-157">Availability and status of the device.</span></span>

<span data-ttu-id="93345-158">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-158">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="93345-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="93345-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93345-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="93345-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="93345-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="93345-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="93345-162">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="93345-162">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="93345-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="93345-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="93345-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="93345-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="93345-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="93345-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="93345-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="93345-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="93345-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="93345-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="93345-168">Offline</span><span class="sxs-lookup"><span data-stu-id="93345-168">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="93345-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="93345-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="93345-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="93345-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="93345-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="93345-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="93345-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="93345-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="93345-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="93345-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="93345-174">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="93345-174">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="93345-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="93345-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="93345-176">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="93345-176">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="93345-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="93345-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="93345-178">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="93345-178">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="93345-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="93345-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="93345-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="93345-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="93345-181">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="93345-181">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="93345-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="93345-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="93345-183">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="93345-183">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="93345-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="93345-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="93345-185">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="93345-185">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="93345-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="93345-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="93345-187">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="93345-187">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="93345-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="93345-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="93345-189">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="93345-189">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-190">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="93345-190">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-191">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="93345-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-193">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ CIM VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="93345-193">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="93345-194">Cadeias de caracteres de forma livre que fornecem explicações mais detalhadas para qualquer um dos recursos do acelerador de vídeo indicados na matriz **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="93345-194">Free-form strings providing more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="93345-195">Observe que cada entrada dessa matriz está relacionada à entrada na matriz **AcceleratorCapabilities** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="93345-195">Note, each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

<span data-ttu-id="93345-196">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-196">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-197">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="93345-197">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-200">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="93345-200">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="93345-201">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="93345-201">Short description of the object.</span></span>

<span data-ttu-id="93345-202">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93345-202">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-203">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="93345-203">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-204">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-206">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="93345-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="93345-207">Tamanho da tabela de cores do sistema.</span><span class="sxs-lookup"><span data-stu-id="93345-207">Size of the system's color table.</span></span> <span data-ttu-id="93345-208">O dispositivo deve ter uma profundidade de cor de no máximo 8 bits por pixel; caso contrário, essa propriedade não será definida.</span><span class="sxs-lookup"><span data-stu-id="93345-208">The device must have a color depth of no more than 8 bits per pixel; otherwise, this property is not set.</span></span>

<span data-ttu-id="93345-209">Exemplo: 256</span><span class="sxs-lookup"><span data-stu-id="93345-209">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="93345-210">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="93345-210">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-211">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-213">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="93345-213">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="93345-214">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="93345-214">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="93345-215">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-215">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="93345-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="93345-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="93345-217"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="93345-217">(0)</span></span>


</dt> <dd>

<span data-ttu-id="93345-218">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="93345-218">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="93345-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="93345-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="93345-220">(1)</span><span class="sxs-lookup"><span data-stu-id="93345-220">(1)</span></span>


</dt> <dd>

<span data-ttu-id="93345-221">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="93345-221">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="93345-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93345-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="93345-223">(2)</span><span class="sxs-lookup"><span data-stu-id="93345-223">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="93345-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="93345-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="93345-225">(3)</span><span class="sxs-lookup"><span data-stu-id="93345-225">(3)</span></span>


</dt> <dd>

<span data-ttu-id="93345-226">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="93345-226">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="93345-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="93345-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="93345-228">(4)</span><span class="sxs-lookup"><span data-stu-id="93345-228">(4)</span></span>


</dt> <dd>

<span data-ttu-id="93345-229">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="93345-229">Device is not working properly.</span></span> <span data-ttu-id="93345-230">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="93345-230">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="93345-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="93345-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="93345-232">(5)</span><span class="sxs-lookup"><span data-stu-id="93345-232">(5)</span></span>


</dt> <dd>

<span data-ttu-id="93345-233">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="93345-233">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="93345-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="93345-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="93345-235"> (6)</span><span class="sxs-lookup"><span data-stu-id="93345-235">(6)</span></span>


</dt> <dd>

<span data-ttu-id="93345-236">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="93345-236">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="93345-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="93345-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="93345-238">(7)</span><span class="sxs-lookup"><span data-stu-id="93345-238">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="93345-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="93345-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="93345-240">(8)</span><span class="sxs-lookup"><span data-stu-id="93345-240">(8)</span></span>


</dt> <dd>

<span data-ttu-id="93345-241">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="93345-241">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="93345-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="93345-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="93345-243">(9)</span><span class="sxs-lookup"><span data-stu-id="93345-243">(9)</span></span>


</dt> <dd>

<span data-ttu-id="93345-244">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="93345-244">Device is not working properly.</span></span> <span data-ttu-id="93345-245">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93345-245">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="93345-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="93345-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="93345-247">(10)</span><span class="sxs-lookup"><span data-stu-id="93345-247">(10)</span></span>


</dt> <dd>

<span data-ttu-id="93345-248">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93345-248">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="93345-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="93345-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="93345-250">(11)</span><span class="sxs-lookup"><span data-stu-id="93345-250">(11)</span></span>


</dt> <dd>

<span data-ttu-id="93345-251">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93345-251">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="93345-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="93345-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="93345-253">12</span><span class="sxs-lookup"><span data-stu-id="93345-253">(12)</span></span>


</dt> <dd>

<span data-ttu-id="93345-254">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="93345-254">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="93345-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93345-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="93345-256">(13)</span><span class="sxs-lookup"><span data-stu-id="93345-256">(13)</span></span>


</dt> <dd>

<span data-ttu-id="93345-257">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93345-257">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="93345-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="93345-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="93345-259">(14)</span><span class="sxs-lookup"><span data-stu-id="93345-259">(14)</span></span>


</dt> <dd>

<span data-ttu-id="93345-260">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="93345-260">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="93345-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="93345-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="93345-262">(15)</span><span class="sxs-lookup"><span data-stu-id="93345-262">(15)</span></span>


</dt> <dd>

<span data-ttu-id="93345-263">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="93345-263">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="93345-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="93345-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="93345-265">(16)</span><span class="sxs-lookup"><span data-stu-id="93345-265">(16)</span></span>


</dt> <dd>

<span data-ttu-id="93345-266">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="93345-266">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="93345-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="93345-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="93345-268">(17)</span><span class="sxs-lookup"><span data-stu-id="93345-268">(17)</span></span>


</dt> <dd>

<span data-ttu-id="93345-269">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="93345-269">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="93345-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93345-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="93345-271">(18)</span><span class="sxs-lookup"><span data-stu-id="93345-271">(18)</span></span>


</dt> <dd>

<span data-ttu-id="93345-272">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="93345-272">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="93345-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="93345-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="93345-274">(19)</span><span class="sxs-lookup"><span data-stu-id="93345-274">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="93345-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="93345-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="93345-276">(20)</span><span class="sxs-lookup"><span data-stu-id="93345-276">(20)</span></span>


</dt> <dd>

<span data-ttu-id="93345-277">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="93345-277">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="93345-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93345-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="93345-279">(21)</span><span class="sxs-lookup"><span data-stu-id="93345-279">(21)</span></span>


</dt> <dd>

<span data-ttu-id="93345-280">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="93345-280">System failure.</span></span> <span data-ttu-id="93345-281">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="93345-281">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="93345-282">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93345-282">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="93345-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="93345-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="93345-284">(22)</span><span class="sxs-lookup"><span data-stu-id="93345-284">(22)</span></span>


</dt> <dd>

<span data-ttu-id="93345-285">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="93345-285">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="93345-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="93345-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="93345-287">(23)</span><span class="sxs-lookup"><span data-stu-id="93345-287">(23)</span></span>


</dt> <dd>

<span data-ttu-id="93345-288">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="93345-288">System failure.</span></span> <span data-ttu-id="93345-289">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="93345-289">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="93345-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="93345-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="93345-291">(24)</span><span class="sxs-lookup"><span data-stu-id="93345-291">(24)</span></span>


</dt> <dd>

<span data-ttu-id="93345-292">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="93345-292">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="93345-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93345-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="93345-294">(25)</span><span class="sxs-lookup"><span data-stu-id="93345-294">(25)</span></span>


</dt> <dd>

<span data-ttu-id="93345-295">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93345-295">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="93345-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93345-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="93345-297">(26)</span><span class="sxs-lookup"><span data-stu-id="93345-297">(26)</span></span>


</dt> <dd>

<span data-ttu-id="93345-298">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93345-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="93345-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="93345-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="93345-300">(27)</span><span class="sxs-lookup"><span data-stu-id="93345-300">(27)</span></span>


</dt> <dd>

<span data-ttu-id="93345-301">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="93345-301">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="93345-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="93345-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="93345-303">(28)</span><span class="sxs-lookup"><span data-stu-id="93345-303">(28)</span></span>


</dt> <dd>

<span data-ttu-id="93345-304">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="93345-304">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="93345-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="93345-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="93345-306">(29)</span><span class="sxs-lookup"><span data-stu-id="93345-306">(29)</span></span>


</dt> <dd>

<span data-ttu-id="93345-307">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="93345-307">Device is disabled.</span></span> <span data-ttu-id="93345-308">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="93345-308">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="93345-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="93345-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="93345-310">(30)</span><span class="sxs-lookup"><span data-stu-id="93345-310">(30)</span></span>


</dt> <dd>

<span data-ttu-id="93345-311">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="93345-311">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="93345-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93345-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="93345-313">(31)</span><span class="sxs-lookup"><span data-stu-id="93345-313">(31)</span></span>


</dt> <dd>

<span data-ttu-id="93345-314">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="93345-314">Device is not working properly.</span></span> <span data-ttu-id="93345-315">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="93345-315">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-316">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="93345-316">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-317">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="93345-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93345-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-319">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="93345-319">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="93345-320">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="93345-320">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="93345-321">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-322">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93345-322">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-323">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-325">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="93345-325">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="93345-326">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="93345-326">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="93345-327">Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="93345-327">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="93345-328">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-329">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="93345-329">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-330">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-332">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 3,12 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="93345-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="93345-333">Número de bits usados para exibir cada pixel.</span><span class="sxs-lookup"><span data-stu-id="93345-333">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="93345-334">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-334">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-335">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="93345-335">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-336">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-338">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 3,11 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="93345-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="93345-339">Número atual de pixels horizontais.</span><span class="sxs-lookup"><span data-stu-id="93345-339">Current number of horizontal pixels.</span></span>

<span data-ttu-id="93345-340">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-340">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-341">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="93345-341">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-342">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93345-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93345-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93345-344">Número de cores com suporte na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="93345-344">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="93345-345">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="93345-345">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="93345-346">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-346">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-347">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="93345-347">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-348">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-350">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 3,14 ")</span><span class="sxs-lookup"><span data-stu-id="93345-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="93345-351">Número de colunas para este controlador de vídeo (se estiver no modo de caractere).</span><span class="sxs-lookup"><span data-stu-id="93345-351">Number of columns for this video controller (if in character mode).</span></span> <span data-ttu-id="93345-352">Caso contrário, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="93345-352">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="93345-353">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-353">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-354">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="93345-354">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-355">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-357">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 3,13 ")</span><span class="sxs-lookup"><span data-stu-id="93345-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="93345-358">Número de linhas para este controlador de vídeo (se estiver no modo de caractere).</span><span class="sxs-lookup"><span data-stu-id="93345-358">Number of rows for this video controller (if in character mode).</span></span> <span data-ttu-id="93345-359">Caso contrário, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="93345-359">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="93345-360">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-360">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-361">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="93345-361">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-362">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-364">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation."), [**Units**](../wmisdk/standard-qualifiers.md) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="93345-364">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation."), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="93345-365">Frequência em que o controlador de vídeo atualiza a imagem para o monitor.</span><span class="sxs-lookup"><span data-stu-id="93345-365">Frequency at which the video controller refreshes the image for the monitor.</span></span> <span data-ttu-id="93345-366">Um valor de 0 (zero) indica que a taxa padrão está sendo usada, enquanto 0xFFFFFFFF indica que a taxa ideal está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="93345-366">A value of 0 (zero) indicates the default rate is being used, while 0xFFFFFFFF indicates the optimal rate is being used.</span></span>

<span data-ttu-id="93345-367">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-367">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-368">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="93345-368">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-369">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93345-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93345-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-371">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 3,8 ")</span><span class="sxs-lookup"><span data-stu-id="93345-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="93345-372">Modo de verificação atual.</span><span class="sxs-lookup"><span data-stu-id="93345-372">Current scan mode.</span></span>

<span data-ttu-id="93345-373">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-373">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="93345-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="93345-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93345-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="93345-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="93345-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Entrelaçado** (3)</span><span class="sxs-lookup"><span data-stu-id="93345-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="93345-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Não entrelaçado** (4)</span><span class="sxs-lookup"><span data-stu-id="93345-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="93345-378">Não entrelaçado</span><span class="sxs-lookup"><span data-stu-id="93345-378">Noninterlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-379">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="93345-379">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-380">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-382">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 3,10 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="93345-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="93345-383">Número atual de pixels verticais.</span><span class="sxs-lookup"><span data-stu-id="93345-383">Current number of vertical pixels.</span></span>

<span data-ttu-id="93345-384">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-384">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-385">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="93345-385">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-386">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-388">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="93345-388">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="93345-389">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="93345-389">Description of the object.</span></span>

<span data-ttu-id="93345-390">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93345-390">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-391">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="93345-391">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-392">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-394">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="93345-394">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="93345-395">Identificador (exclusivo para o sistema de computador) deste controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-395">Identifier (unique to the computer system) for this video controller.</span></span>

<span data-ttu-id="93345-396">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-397">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="93345-397">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-398">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-400">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="93345-400">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="93345-401">Número atual de canetas específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93345-401">Current number of device-specific pens.</span></span> <span data-ttu-id="93345-402">Um valor de 0xFFFF significa que o dispositivo não dá suporte a canetas.</span><span class="sxs-lookup"><span data-stu-id="93345-402">A value of 0xffff means that the device does not support pens.</span></span>

<span data-ttu-id="93345-403">Exemplo: 3</span><span class="sxs-lookup"><span data-stu-id="93345-403">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="93345-404">**Pontilhado**</span><span class="sxs-lookup"><span data-stu-id="93345-404">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-405">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-406">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-407">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| EnumDisplaySettings")</span><span class="sxs-lookup"><span data-stu-id="93345-407">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|EnumDisplaySettings")</span></span>
</dt> </dl>

<span data-ttu-id="93345-408">Tipo de pontilhamento do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-408">Dither type of the video controller.</span></span> <span data-ttu-id="93345-409">A propriedade pode ser um dos valores predefinidos ou um valor definido pelo driver maior ou igual a 256.</span><span class="sxs-lookup"><span data-stu-id="93345-409">The property can be one of the predefined values, or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="93345-410">Se o pontilhado da arte de linhas for escolhido, o controlador usará um método de pontilhamento que produz bordas bem definidas entre as escalas preta, branca e cinza.</span><span class="sxs-lookup"><span data-stu-id="93345-410">If line art dithering is chosen, the controller uses a dithering method that produces well-defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="93345-411">O pontilhamento de arte de linha não é adequado para imagens que incluem graduações contínuas em intensidade e matiz, como fotografias digitalizadas.</span><span class="sxs-lookup"><span data-stu-id="93345-411">Line art dithering is not suitable for images that include continuous graduations in intensity and hue such as scanned photographs.</span></span>

<dt>

<span id="No_dithering"></span><span id="no_dithering"></span><span id="NO_DITHERING"></span>

<span data-ttu-id="93345-412">**Sem pontilhamento** (1)</span><span class="sxs-lookup"><span data-stu-id="93345-412">**No dithering** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_coarse_brush"></span><span id="dithering_with_a_coarse_brush"></span><span id="DITHERING_WITH_A_COARSE_BRUSH"></span>

<span data-ttu-id="93345-413">**Pontilhamento com pincel grosso** (2)</span><span class="sxs-lookup"><span data-stu-id="93345-413">**Dithering with a coarse brush** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_fine_brush"></span><span id="dithering_with_a_fine_brush"></span><span id="DITHERING_WITH_A_FINE_BRUSH"></span>

<span data-ttu-id="93345-414">**Pontilhamento com um pincel fino** (3)</span><span class="sxs-lookup"><span data-stu-id="93345-414">**Dithering with a fine brush** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_art_dithering"></span><span id="line_art_dithering"></span><span id="LINE_ART_DITHERING"></span>

<span data-ttu-id="93345-415">**Pontilhamento de arte de linha** (4)</span><span class="sxs-lookup"><span data-stu-id="93345-415">**Line art dithering** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_does_gray_scaling"></span><span id="device_does_gray_scaling"></span><span id="DEVICE_DOES_GRAY_SCALING"></span>

<span data-ttu-id="93345-416">**O dispositivo faz o dimensionamento em cinza** (5)</span><span class="sxs-lookup"><span data-stu-id="93345-416">**Device does gray scaling** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-417">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="93345-417">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-418">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93345-418">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93345-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-420">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="93345-420">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="93345-421">Data e hora da última modificação do driver de vídeo atualmente instalado.</span><span class="sxs-lookup"><span data-stu-id="93345-421">Last modification date and time of the currently installed video driver.</span></span>

</dd> <dt>

<span data-ttu-id="93345-422">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="93345-422">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-423">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-424">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-425">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de biblioteca de instalação de arquivo win32api \| GetFileVersionInfo")</span><span class="sxs-lookup"><span data-stu-id="93345-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Installation Library Functions\|GetFileVersionInfo")</span></span>
</dt> </dl>

<span data-ttu-id="93345-426">Número de versão do driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-426">Version number of the video driver.</span></span>

</dd> <dt>

<span data-ttu-id="93345-427">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="93345-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-428">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="93345-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93345-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93345-430">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="93345-430">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="93345-431">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-432">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="93345-432">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-433">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93345-435">Cadeia de caracteres de forma livre fornecendo mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="93345-435">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="93345-436">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-437">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="93345-437">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-438">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-439">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-440">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de impressão e spooler de impressão de estruturas \| \| dmICMIntent")</span><span class="sxs-lookup"><span data-stu-id="93345-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMIntent")</span></span>
</dt> </dl>

<span data-ttu-id="93345-441">Valor específico de um dos três métodos possíveis de correspondência de cor ou tentativas que devem ser usadas por padrão.</span><span class="sxs-lookup"><span data-stu-id="93345-441">Specific value of one of the three possible color-matching methods or intents that should be used by default.</span></span> <span data-ttu-id="93345-442">Essa propriedade é usada principalmente para aplicativos não ICM.</span><span class="sxs-lookup"><span data-stu-id="93345-442">This property is used primarily for non-ICM applications.</span></span> <span data-ttu-id="93345-443">Os aplicativos ICM estabelecem tentativas usando as funções ICM.</span><span class="sxs-lookup"><span data-stu-id="93345-443">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="93345-444">Essa propriedade pode ser um valor predefinido ou um valor definido pelo driver maior ou igual a 256.</span><span class="sxs-lookup"><span data-stu-id="93345-444">This property can be a predefined value or a driver defined value greater than or equal to 256.</span></span> <span data-ttu-id="93345-445">A correspondência de cores com base na saturação é a opção mais apropriada para grafos de negócios quando o pontilhado não é desejado.</span><span class="sxs-lookup"><span data-stu-id="93345-445">Color matching based on saturation is the most appropriate choice for business graphs when dithering is not desired.</span></span> <span data-ttu-id="93345-446">A correspondência de cores com base no contraste é a opção mais apropriada para imagens digitalizadas ou fotográficas quando o pontilhado é desejado.</span><span class="sxs-lookup"><span data-stu-id="93345-446">Color matching based on contrast is the most appropriate choice for scanned or photographic images when dithering is desired.</span></span> <span data-ttu-id="93345-447">A correspondência de cores otimizada para corresponder à cor exata solicitada é mais apropriada para uso com logotipos de negócios ou outras imagens quando uma correspondência exata de cor é desejada.</span><span class="sxs-lookup"><span data-stu-id="93345-447">Color matching optimized to match the exact color requested is most appropriate for use with business logos or other images when an exact color match is desired.</span></span>

<dt>

<span id="Saturation"></span><span id="saturation"></span><span id="SATURATION"></span>

<span data-ttu-id="93345-448">**Saturação** (1)</span><span class="sxs-lookup"><span data-stu-id="93345-448">**Saturation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Contrast"></span><span id="contrast"></span><span id="CONTRAST"></span>

<span data-ttu-id="93345-449">**Contraste** (2)</span><span class="sxs-lookup"><span data-stu-id="93345-449">**Contrast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Exact_Color"></span><span id="exact_color"></span><span id="EXACT_COLOR"></span>

<span data-ttu-id="93345-450">**Cor exata** (3)</span><span class="sxs-lookup"><span data-stu-id="93345-450">**Exact Color** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-451">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="93345-451">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-452">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-454">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de impressão e spooler de impressão de estruturas \| \| dmICMMethod")</span><span class="sxs-lookup"><span data-stu-id="93345-454">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMMethod")</span></span>
</dt> </dl>

<span data-ttu-id="93345-455">Método de tratamento de ICM.</span><span class="sxs-lookup"><span data-stu-id="93345-455">Method of handling ICM.</span></span> <span data-ttu-id="93345-456">Para aplicativos não ICM, essa propriedade determina se o ICM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="93345-456">For non-ICM applications, this property determines if ICM is enabled.</span></span> <span data-ttu-id="93345-457">Para aplicativos ICM, o sistema examina essa propriedade para determinar como lidar com o suporte a ICM.</span><span class="sxs-lookup"><span data-stu-id="93345-457">For ICM applications, the system examines this property to determine how to handle ICM support.</span></span> <span data-ttu-id="93345-458">Essa propriedade pode ser um valor predefinido ou um valor definido pelo driver maior ou igual a 256.</span><span class="sxs-lookup"><span data-stu-id="93345-458">This property can be a predefined value or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="93345-459">O valor determina qual sistema manipula a correspondência de cores da imagem.</span><span class="sxs-lookup"><span data-stu-id="93345-459">The value determines which system handles image color matching.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="93345-460">**Desabilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="93345-460">**Disabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows"></span><span id="windows"></span><span id="WINDOWS"></span>

<span data-ttu-id="93345-461">**Windows** (2)</span><span class="sxs-lookup"><span data-stu-id="93345-461">**Windows** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Driver"></span><span id="device_driver"></span><span id="DEVICE_DRIVER"></span>

<span data-ttu-id="93345-462">**Driver de dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="93345-462">**Device Driver** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination_Device"></span><span id="destination_device"></span><span id="DESTINATION_DEVICE"></span>

<span data-ttu-id="93345-463">**Dispositivo de destino** (4)</span><span class="sxs-lookup"><span data-stu-id="93345-463">**Destination Device** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-464">**InfFilename**</span><span class="sxs-lookup"><span data-stu-id="93345-464">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-465">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-466">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-467">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="93345-467">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="93345-468">Caminho para o arquivo. inf do adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-468">Path to the video adapter's .inf file.</span></span>

<span data-ttu-id="93345-469">Exemplo: "C: \\ Windows \\ System32 \\ drivers"</span><span class="sxs-lookup"><span data-stu-id="93345-469">Example: "C:\\Windows\\SYSTEM32\\DRIVERS"</span></span>

</dd> <dt>

<span data-ttu-id="93345-470">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="93345-470">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-471">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-473">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="93345-473">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="93345-474">Seção do arquivo. inf onde residem as informações de vídeo do Windows.</span><span class="sxs-lookup"><span data-stu-id="93345-474">Section of the .inf file where the Windows video information resides.</span></span>

</dd> <dt>

<span data-ttu-id="93345-475">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="93345-475">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-476">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93345-476">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93345-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-478">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="93345-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="93345-479">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="93345-479">Date and time the object was installed.</span></span> <span data-ttu-id="93345-480">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="93345-480">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="93345-481">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93345-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-482">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="93345-482">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-483">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-484">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-485">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="93345-485">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="93345-486">Nome do driver de dispositivo de vídeo instalado.</span><span class="sxs-lookup"><span data-stu-id="93345-486">Name of the installed display device driver.</span></span>

</dd> <dt>

<span data-ttu-id="93345-487">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="93345-487">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-488">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-489">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93345-490">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93345-490">Last error code reported by the logical device.</span></span>

<span data-ttu-id="93345-491">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-492">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="93345-492">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-493">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-494">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-495">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="93345-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="93345-496">Quantidade máxima de memória suportada em bytes.</span><span class="sxs-lookup"><span data-stu-id="93345-496">Maximum amount of memory supported in bytes.</span></span>

<span data-ttu-id="93345-497">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-497">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-498">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="93345-498">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-499">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-499">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-500">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-501">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="93345-501">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="93345-502">Número máximo de entidades diretamente endereçáveis com suporte por este controlador.</span><span class="sxs-lookup"><span data-stu-id="93345-502">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="93345-503">Um valor de 0 (zero) deve ser usado se o número for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="93345-503">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="93345-504">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-504">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-505">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="93345-505">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-506">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-508">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 3,5 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="93345-508">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="93345-509">Taxa máxima de atualização do controlador de vídeo em Hertz.</span><span class="sxs-lookup"><span data-stu-id="93345-509">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="93345-510">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-510">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-511">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="93345-511">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-512">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-512">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-513">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-514">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 3,4 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="93345-514">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="93345-515">Taxa mínima de atualização do controlador de vídeo em Hertz.</span><span class="sxs-lookup"><span data-stu-id="93345-515">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="93345-516">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-516">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-517">**Monocromático**</span><span class="sxs-lookup"><span data-stu-id="93345-517">**Monochrome**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-518">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="93345-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93345-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-520">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="93345-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="93345-521">Se for **true**, a escala de cinza será usada para exibir imagens.</span><span class="sxs-lookup"><span data-stu-id="93345-521">If **TRUE**, gray scale is used to display images.</span></span>

</dd> <dt>

<span data-ttu-id="93345-522">**Nome**</span><span class="sxs-lookup"><span data-stu-id="93345-522">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-523">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-524">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-525">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="93345-525">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="93345-526">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="93345-526">Label by which the object is known.</span></span> <span data-ttu-id="93345-527">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="93345-527">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="93345-528">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93345-528">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-529">**NumberOfColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="93345-529">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-530">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93345-530">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93345-531">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93345-532">Número atual de planos de cores.</span><span class="sxs-lookup"><span data-stu-id="93345-532">Current number of color planes.</span></span> <span data-ttu-id="93345-533">Se esse valor não for aplicável para a configuração de vídeo atual, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="93345-533">If this value is not applicable for the current video configuration, enter 0 (zero).</span></span>

<span data-ttu-id="93345-534">Essa propriedade é herdada do [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-534">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-535">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="93345-535">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-536">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-536">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-537">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93345-538">Número de páginas de vídeo com suporte dadas as resoluções atuais e a memória disponível.</span><span class="sxs-lookup"><span data-stu-id="93345-538">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="93345-539">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-539">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-540">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="93345-540">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-541">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-542">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-543">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="93345-543">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="93345-544">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93345-544">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="93345-545">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="93345-545">Example: "\*PNP030b"</span></span>

<span data-ttu-id="93345-546">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-546">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-547">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="93345-547">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-548">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93345-548">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93345-549">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93345-550">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93345-550">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="93345-551">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-551">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93345-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="93345-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="93345-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="93345-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="93345-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="93345-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="93345-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="93345-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="93345-556">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="93345-556">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="93345-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="93345-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="93345-558">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="93345-558">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="93345-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="93345-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="93345-560">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="93345-560">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="93345-561">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="93345-561">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="93345-562">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="93345-562">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="93345-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="93345-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="93345-564">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="93345-564">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="93345-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="93345-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="93345-566">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="93345-566">Timed Power-On Supported</span></span>

<span data-ttu-id="93345-567">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="93345-567">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-568">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="93345-568">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-569">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="93345-569">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93345-570">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-570">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93345-571">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="93345-571">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="93345-572">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="93345-572">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="93345-573">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-574">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="93345-574">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-575">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93345-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93345-576">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-577">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="93345-577">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="93345-578">Protocolo usado pelo controlador para acessar dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="93345-578">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="93345-579">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-579">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="93345-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="93345-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93345-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="93345-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="93345-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="93345-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="93345-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="93345-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="93345-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="93345-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="93345-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="93345-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="93345-586">ATA ou ATAPI</span><span class="sxs-lookup"><span data-stu-id="93345-586">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="93345-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="93345-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="93345-588"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="93345-588"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="93345-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="93345-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="93345-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="93345-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="93345-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="93345-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="93345-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="93345-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="93345-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="93345-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="93345-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="93345-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="93345-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="93345-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="93345-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="93345-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="93345-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="93345-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="93345-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="93345-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="93345-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="93345-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="93345-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="93345-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="93345-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="93345-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="93345-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="93345-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="93345-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="93345-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="93345-604"><span id="VME"></span><span id="vme"></span>**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="93345-604"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="93345-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="93345-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="93345-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="93345-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="93345-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="93345-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="93345-608"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="93345-608"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="93345-609"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="93345-609"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="93345-610"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="93345-610"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="93345-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="93345-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="93345-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="93345-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="93345-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="93345-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="93345-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="93345-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="93345-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="93345-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="93345-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="93345-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="93345-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="93345-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="93345-618"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="93345-618"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="93345-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="93345-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="93345-620"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="93345-620"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="93345-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="93345-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="93345-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="93345-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="93345-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="93345-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="93345-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="93345-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="93345-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="93345-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="93345-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="93345-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="93345-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="93345-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-628">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="93345-628">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-629">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-629">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-630">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-631">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="93345-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="93345-632">Número de entradas reservadas na paleta do sistema.</span><span class="sxs-lookup"><span data-stu-id="93345-632">Number of reserved entries in the system palette.</span></span> <span data-ttu-id="93345-633">O sistema operacional pode reservar entradas para dar suporte a cores padrão para barras de tarefas e outros itens de exibição da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="93345-633">The operating system may reserve entries to support standard colors for task bars and other desktop display items.</span></span> <span data-ttu-id="93345-634">Esse índice será válido somente se o driver de dispositivo definir o bit da **\_ paleta RC** no índice RASTERCAPS e estiver disponível somente se o driver for compatível com o Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="93345-634">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="93345-635">Se o sistema não estiver usando uma paleta, **ReservedSystemPaletteEntries** não será definido.</span><span class="sxs-lookup"><span data-stu-id="93345-635">If the system is not using a palette, **ReservedSystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="93345-636">Exemplo: 20</span><span class="sxs-lookup"><span data-stu-id="93345-636">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="93345-637">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="93345-637">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-638">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-638">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-639">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-639">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-640">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de impressão e spooler de impressão de estruturas \| \| dmSpecVersion")</span><span class="sxs-lookup"><span data-stu-id="93345-640">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmSpecVersion")</span></span>
</dt> </dl>

<span data-ttu-id="93345-641">Número de versão da especificação de dados de inicialização (na qual a estrutura é baseada).</span><span class="sxs-lookup"><span data-stu-id="93345-641">Version number of the initialization data specification (upon which the structure is based).</span></span>

</dd> <dt>

<span data-ttu-id="93345-642">**Status**</span><span class="sxs-lookup"><span data-stu-id="93345-642">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-643">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-644">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-644">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-645">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="93345-645">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="93345-646">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="93345-646">Current status of the object.</span></span> <span data-ttu-id="93345-647">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="93345-647">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="93345-648">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="93345-648">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="93345-649">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="93345-649">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="93345-650">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="93345-650">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="93345-651">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="93345-651">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="93345-652">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93345-652">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="93345-653">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="93345-653">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="93345-654">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="93345-654">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="93345-655">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="93345-655">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="93345-656">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="93345-656">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93345-657">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="93345-657">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="93345-658">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="93345-658">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="93345-659">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="93345-659">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="93345-660">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="93345-660">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="93345-661">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="93345-661">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="93345-662">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="93345-662">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="93345-663">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="93345-663">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="93345-664">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="93345-664">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="93345-665">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="93345-665">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-666">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="93345-666">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-667">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93345-667">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93345-668">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-668">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-669">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="93345-669">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="93345-670">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93345-670">State of the logical device.</span></span> <span data-ttu-id="93345-671">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="93345-671">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="93345-672">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-672">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="93345-673">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="93345-673">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93345-674">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="93345-674">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="93345-675">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="93345-675">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="93345-676">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="93345-676">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="93345-677">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="93345-677">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-678">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93345-678">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-679">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-679">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-680">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-681">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="93345-681">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="93345-682">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="93345-682">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="93345-683">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-683">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-684">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="93345-684">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-685">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-685">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-686">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-687">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="93345-687">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="93345-688">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="93345-688">Name of the scoping system.</span></span>

<span data-ttu-id="93345-689">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93345-689">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-690">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="93345-690">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-691">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93345-691">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93345-692">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-692">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-693">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="93345-693">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="93345-694">Número atual de entradas de índice de cor na paleta do sistema.</span><span class="sxs-lookup"><span data-stu-id="93345-694">Current number of color index entries in the system palette.</span></span> <span data-ttu-id="93345-695">Esse índice será válido somente se o driver de dispositivo definir o bit da **\_ paleta RC** no índice RASTERCAPS e estiver disponível somente se o driver for compatível com o Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="93345-695">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="93345-696">Se o sistema não estiver usando uma paleta, **SystemPaletteEntries** não será definido.</span><span class="sxs-lookup"><span data-stu-id="93345-696">If the system is not using a palette, **SystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="93345-697">Exemplo: 20</span><span class="sxs-lookup"><span data-stu-id="93345-697">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="93345-698">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="93345-698">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-699">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93345-699">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93345-700">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-700">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93345-701">Data e hora da última redefinição deste controlador.</span><span class="sxs-lookup"><span data-stu-id="93345-701">Date and time this controller was last reset.</span></span> <span data-ttu-id="93345-702">Isso pode significar que o controlador foi desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="93345-702">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="93345-703">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-703">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-704">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="93345-704">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-705">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93345-705">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93345-706">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-706">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-707">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 3,2 ")</span><span class="sxs-lookup"><span data-stu-id="93345-707">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="93345-708">Tipo de arquitetura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-708">Type of video architecture.</span></span>

<span data-ttu-id="93345-709">Essa propriedade é herdada do [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-709">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="93345-710">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="93345-710">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93345-711">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="93345-711">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="93345-712">**CGA** (3)</span><span class="sxs-lookup"><span data-stu-id="93345-712">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="93345-713">**EGA** (4)</span><span class="sxs-lookup"><span data-stu-id="93345-713">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="93345-714">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="93345-714">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="93345-715">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="93345-715">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="93345-716">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="93345-716">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="93345-717">**HGC** (8)</span><span class="sxs-lookup"><span data-stu-id="93345-717">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="93345-718">**MCGA** (9)</span><span class="sxs-lookup"><span data-stu-id="93345-718">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="93345-719">**8514A** (10)</span><span class="sxs-lookup"><span data-stu-id="93345-719">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="93345-720">**XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="93345-720">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="93345-721">**Buffer de quadro linear** (12)</span><span class="sxs-lookup"><span data-stu-id="93345-721">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="93345-722">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="93345-722">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-723">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="93345-723">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-724">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93345-724">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93345-725">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-726">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 3,6 ")</span><span class="sxs-lookup"><span data-stu-id="93345-726">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="93345-727">Tipo de memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-727">Type of video memory.</span></span>

<span data-ttu-id="93345-728">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-728">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="93345-729">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="93345-729">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93345-730">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="93345-730">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="93345-731">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="93345-731">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="93345-732">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="93345-732">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="93345-733">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="93345-733">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="93345-734">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="93345-734">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="93345-735">**Edo RAM** (7)</span><span class="sxs-lookup"><span data-stu-id="93345-735">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="93345-736">**DRAM síncrona intermitente** (8)</span><span class="sxs-lookup"><span data-stu-id="93345-736">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="93345-737">**SRAM de intermitência em pipeline** (9)</span><span class="sxs-lookup"><span data-stu-id="93345-737">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="93345-738">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="93345-738">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="93345-739">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="93345-739">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="93345-740">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="93345-740">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="93345-741">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="93345-741">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93345-742">**Videomode**</span><span class="sxs-lookup"><span data-stu-id="93345-742">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-743">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93345-743">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93345-744">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-744">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-745">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="93345-745">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="93345-746">Modo de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="93345-746">Current video mode.</span></span>

<span data-ttu-id="93345-747">Essa propriedade é herdada do [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-747">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="93345-748">**VideoModeDescription**</span><span class="sxs-lookup"><span data-stu-id="93345-748">**VideoModeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-749">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-750">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-750">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93345-751">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="93345-751">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="93345-752">Resolução atual, cor e configurações do modo de verificação do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-752">Current resolution, color, and scan mode settings of the video controller.</span></span>

<span data-ttu-id="93345-753">Exemplo: "1024 x 768 x 256 cores"</span><span class="sxs-lookup"><span data-stu-id="93345-753">Example: "1024 x 768 x 256 colors"</span></span>

</dd> <dt>

<span data-ttu-id="93345-754">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="93345-754">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93345-755">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93345-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93345-756">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93345-756">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93345-757">Cadeia de caracteres de forma livre que descreve o processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-757">Free-form string describing the video processor.</span></span>

<span data-ttu-id="93345-758">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-758">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93345-759">Comentários</span><span class="sxs-lookup"><span data-stu-id="93345-759">Remarks</span></span>

<span data-ttu-id="93345-760">A classe **Win32 \_ VideoController** é derivada de [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="93345-760">The **Win32\_VideoController** class is derived from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<span data-ttu-id="93345-761">Para obter mais informações sobre como usar essa classe, como recuperar informações de vários monitores, consulte [usar o PowerShell para descobrir informações de vários](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx)monitores.</span><span class="sxs-lookup"><span data-stu-id="93345-761">For more information about using this class, such as retrieving information from multiple monitors, see [Use PowerShell to Discover Multi-Monitor Information](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx).</span></span>

## <a name="examples"></a><span data-ttu-id="93345-762">Exemplos</span><span class="sxs-lookup"><span data-stu-id="93345-762">Examples</span></span>

<span data-ttu-id="93345-763">A exemplo [listar Propriedades do controlador de vídeo](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) VBScript lista as propriedades do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-763">The [List Video Controller Properties](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) VBScript sample lists the video controller properties.</span></span>

<span data-ttu-id="93345-764">O exemplo do PowerShell a seguir lista as propriedades do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93345-764">The following PowerShell example lists the video controller properties.</span></span>


```VB
$strComputer = "." 
 
$colItems = get-wmiobject -class "Win32_VideoController" -namespace "root\CIMV2" ` 
-computername $strComputer 
 
foreach ($objItem in $colItems) { 
      write-host "Accelerator Capabilities: " $objItem.AcceleratorCapabilities 
      write-host "Adapter Compatibility: " $objItem.AdapterCompatibility 
      write-host "Adapter DAC Type: " $objItem.AdapterDACType 
      write-host "Adapter RAM: " $objItem.AdapterRAM 
      write-host "Availability: " $objItem.Availability 
      write-host "Capability Descriptions: " $objItem.CapabilityDescriptions 
      write-host "Caption: " $objItem.Caption 
      write-host "Color Table Entries: " $objItem.ColorTableEntries 
      write-host "Configuration Manager Error Code: " $objItem.ConfigManagerErrorCode 
      write-host "Configuration Manager User Configuration: " $objItem.ConfigManagerUserConfig 
      write-host "Creation Class Name: " $objItem.CreationClassName 
      write-host "Current Bits Per Pixel: " $objItem.CurrentBitsPerPixel 
      write-host "Current Horizontal Resolution: " $objItem.CurrentHorizontalResolution 
      write-host "Current Number Of Colors: " $objItem.CurrentNumberOfColors 
      write-host "Current Number Of Columns: " $objItem.CurrentNumberOfColumns 
      write-host "Current Number Of Rows: " $objItem.CurrentNumberOfRows 
      write-host "Current Refresh Rate: " $objItem.CurrentRefreshRate 
      write-host "Current Scan Mode: " $objItem.CurrentScanMode 
      write-host "Current Vertical Resolution: " $objItem.CurrentVerticalResolution 
      write-host "Description: " $objItem.Description 
      write-host "Device ID: " $objItem.DeviceID 
      write-host "Device Specific Pens: " $objItem.DeviceSpecificPens 
      write-host "Dither Type: " $objItem.DitherType 
      write-host "Driver Date: " $objItem.DriverDate 
      write-host "Driver Version: " $objItem.DriverVersion 
      write-host "Error Cleared: " $objItem.ErrorCleared 
      write-host "Error Description: " $objItem.ErrorDescription 
      write-host "ICM Intent: " $objItem.ICMIntent 
      write-host "ICM Method: " $objItem.ICMMethod 
      write-host "Inf File Name: " $objItem.InfFilename 
      write-host "Inf Section: " $objItem.InfSection 
      write-host "Installation Date: " $objItem.InstallDate 
      write-host "Installed Display Drivers: " $objItem.InstalledDisplayDrivers 
      write-host "Last Error Code: " $objItem.LastErrorCode 
      write-host "Maximum Memory Supported: " $objItem.MaxMemorySupported 
      write-host "Maximum Number Controlled: " $objItem.MaxNumberControlled 
      write-host "Maximum Refresh Rate: " $objItem.MaxRefreshRate 
      write-host "Minimum Refresh Rate: " $objItem.MinRefreshRate 
      write-host "Monochrome: " $objItem.Monochrome 
      write-host "Name: " $objItem.Name 
      write-host "Number Of Color Planes: " $objItem.NumberOfColorPlanes 
      write-host "Number Of Video Pages: " $objItem.NumberOfVideoPages 
      write-host "PNP Device ID: " $objItem.PNPDeviceID 
      write-host "Power Management Capabilities: " $objItem.PowerManagementCapabilities 
      write-host "Power Management Supported: " $objItem.PowerManagementSupported 
      write-host "Protocol Supported: " $objItem.ProtocolSupported 
      write-host "Reserved System Palette Entries: " $objItem.ReservedSystemPaletteEntries 
      write-host "Specification Version: " $objItem.SpecificationVersion 
      write-host "Status: " $objItem.Status 
      write-host "Status Information: " $objItem.StatusInfo 
      write-host "System Creation Class Name: " $objItem.SystemCreationClassName 
      write-host "System Name: " $objItem.SystemName 
      write-host "System Palette Entries: " $objItem.SystemPaletteEntries 
      write-host "Time Of Last Reset: " $objItem.TimeOfLastReset 
      write-host "Video Architecture: " $objItem.VideoArchitecture 
      write-host "Video Memory Type: " $objItem.VideoMemoryType 
      write-host "Video Mode: " $objItem.VideoMode 
      write-host "Video Mode Description: " $objItem.VideoModeDescription 
      write-host "Video Processor: " $objItem.VideoProcessor 
      write-host 
} 
```



## <a name="requirements"></a><span data-ttu-id="93345-765">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93345-765">Requirements</span></span>



| <span data-ttu-id="93345-766">Requisito</span><span class="sxs-lookup"><span data-stu-id="93345-766">Requirement</span></span> | <span data-ttu-id="93345-767">Valor</span><span class="sxs-lookup"><span data-stu-id="93345-767">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93345-768">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93345-768">Minimum supported client</span></span><br/> | <span data-ttu-id="93345-769">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93345-769">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93345-770">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93345-770">Minimum supported server</span></span><br/> | <span data-ttu-id="93345-771">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93345-771">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93345-772">Namespace</span><span class="sxs-lookup"><span data-stu-id="93345-772">Namespace</span></span><br/>                | <span data-ttu-id="93345-773">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="93345-773">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93345-774">MOF</span><span class="sxs-lookup"><span data-stu-id="93345-774">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93345-775"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93345-775"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93345-776">DLL</span><span class="sxs-lookup"><span data-stu-id="93345-776">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93345-777"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93345-777"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93345-778">Confira também</span><span class="sxs-lookup"><span data-stu-id="93345-778">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93345-779">**\_PCVIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="93345-779">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dt>

[<span data-ttu-id="93345-780">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="93345-780">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
