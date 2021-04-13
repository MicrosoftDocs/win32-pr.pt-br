---
description: O \_ PCVIDEOCONTROLLER CIM representa os recursos e o gerenciamento de um controlador de vídeo de computador pessoal, um subtipo de um controlador de vídeo.
ms.assetid: bf937727-a332-445b-9397-7d87d58c4a5b
ms.tgt_platform: multiple
title: Classe CIM_PCVideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController
- CIM_PCVideoController.AcceleratorCapabilities
- CIM_PCVideoController.Availability
- CIM_PCVideoController.CapabilityDescriptions
- CIM_PCVideoController.Caption
- CIM_PCVideoController.ConfigManagerErrorCode
- CIM_PCVideoController.ConfigManagerUserConfig
- CIM_PCVideoController.CreationClassName
- CIM_PCVideoController.CurrentBitsPerPixel
- CIM_PCVideoController.CurrentHorizontalResolution
- CIM_PCVideoController.CurrentNumberOfColors
- CIM_PCVideoController.CurrentNumberOfColumns
- CIM_PCVideoController.CurrentNumberOfRows
- CIM_PCVideoController.CurrentRefreshRate
- CIM_PCVideoController.CurrentScanMode
- CIM_PCVideoController.CurrentVerticalResolution
- CIM_PCVideoController.Description
- CIM_PCVideoController.DeviceID
- CIM_PCVideoController.ErrorCleared
- CIM_PCVideoController.ErrorDescription
- CIM_PCVideoController.InstallDate
- CIM_PCVideoController.LastErrorCode
- CIM_PCVideoController.MaxMemorySupported
- CIM_PCVideoController.MaxNumberControlled
- CIM_PCVideoController.MaxRefreshRate
- CIM_PCVideoController.MinRefreshRate
- CIM_PCVideoController.Name
- CIM_PCVideoController.NumberOfColorPlanes
- CIM_PCVideoController.NumberOfVideoPages
- CIM_PCVideoController.PNPDeviceID
- CIM_PCVideoController.PowerManagementCapabilities
- CIM_PCVideoController.PowerManagementSupported
- CIM_PCVideoController.ProtocolSupported
- CIM_PCVideoController.Status
- CIM_PCVideoController.StatusInfo
- CIM_PCVideoController.SystemCreationClassName
- CIM_PCVideoController.SystemName
- CIM_PCVideoController.TimeOfLastReset
- CIM_PCVideoController.VideoArchitecture
- CIM_PCVideoController.VideoMemoryType
- CIM_PCVideoController.VideoMode
- CIM_PCVideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94465862c34cc9c6fb645f63c0add48d0fded56b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370448"
---
# <a name="cim_pcvideocontroller-class"></a><span data-ttu-id="83e5e-103">\_Classe CIM PCVideoController</span><span class="sxs-lookup"><span data-stu-id="83e5e-103">CIM\_PCVideoController class</span></span>

<span data-ttu-id="83e5e-104">O **\_ PCVideoController CIM** representa os recursos e o gerenciamento de um controlador de vídeo de computador pessoal, um subtipo de um controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-104">The **CIM\_PCVideoController** represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83e5e-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="83e5e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="83e5e-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="83e5e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="83e5e-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="83e5e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="83e5e-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="83e5e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="83e5e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83e5e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE6-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_PCVideoController : CIM_VideoController
{
  uint16   AcceleratorCapabilities[];
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
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
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="83e5e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="83e5e-110">Members</span></span>

<span data-ttu-id="83e5e-111">A classe **CIM \_ PCVideoController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="83e5e-111">The **CIM\_PCVideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="83e5e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="83e5e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="83e5e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="83e5e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="83e5e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="83e5e-114">Methods</span></span>

<span data-ttu-id="83e5e-115">A classe **CIM \_ PCVideoController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="83e5e-115">The **CIM\_PCVideoController** class has these methods.</span></span>



| <span data-ttu-id="83e5e-116">Método</span><span class="sxs-lookup"><span data-stu-id="83e5e-116">Method</span></span>                                                                       | <span data-ttu-id="83e5e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="83e5e-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83e5e-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="83e5e-118">**Reset**</span></span>](reset-method-in-class-cim-pcvideocontroller.md)                 | <span data-ttu-id="83e5e-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="83e5e-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="83e5e-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="83e5e-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="83e5e-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="83e5e-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcvideocontroller.md) | <span data-ttu-id="83e5e-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="83e5e-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="83e5e-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="83e5e-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="83e5e-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="83e5e-124">Properties</span></span>

<span data-ttu-id="83e5e-125">A classe **CIM \_ PCVideoController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="83e5e-125">The **CIM\_PCVideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83e5e-126">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="83e5e-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-127">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83e5e-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-129">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="83e5e-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-130">Gráficos e recursos 3-D do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-130">Graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="83e5e-131">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-131">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83e5e-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="83e5e-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83e5e-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="83e5e-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="83e5e-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Acelerador de gráficos** (2)</span><span class="sxs-lookup"><span data-stu-id="83e5e-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="83e5e-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**acelerador 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="83e5e-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-136">Acelerador 3D</span><span class="sxs-lookup"><span data-stu-id="83e5e-136">3-D accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83e5e-137">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="83e5e-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-138">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83e5e-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-140">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-141">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-141">Availability and status of the device.</span></span>

<span data-ttu-id="83e5e-142">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83e5e-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="83e5e-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83e5e-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="83e5e-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="83e5e-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="83e5e-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-146">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="83e5e-146">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="83e5e-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="83e5e-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="83e5e-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="83e5e-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="83e5e-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="83e5e-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="83e5e-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="83e5e-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="83e5e-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="83e5e-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="83e5e-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="83e5e-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="83e5e-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="83e5e-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="83e5e-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="83e5e-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="83e5e-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="83e5e-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="83e5e-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="83e5e-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-157">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="83e5e-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="83e5e-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="83e5e-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-159">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="83e5e-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="83e5e-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="83e5e-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-161">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="83e5e-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="83e5e-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="83e5e-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="83e5e-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="83e5e-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-164">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="83e5e-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="83e5e-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="83e5e-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-166">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="83e5e-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="83e5e-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="83e5e-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-168">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="83e5e-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="83e5e-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="83e5e-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-170">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="83e5e-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="83e5e-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="83e5e-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-172">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="83e5e-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83e5e-173">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="83e5e-173">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-174">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-176">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="83e5e-176">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-177">Cadeias de caracteres de forma livre que fornecem explicações detalhadas para os recursos do acelerador de vídeo indicados na matriz **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="83e5e-177">Free-form strings that provide detailed explanations for video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="83e5e-178">Cada entrada de matriz está relacionada à entrada na matriz **AcceleratorCapabilities** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="83e5e-178">Each array entry is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

<span data-ttu-id="83e5e-179">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-179">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-180">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="83e5e-180">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-183">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="83e5e-183">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-184">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="83e5e-184">Short textual description of the object.</span></span>

<span data-ttu-id="83e5e-185">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-186">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="83e5e-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-187">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-189">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="83e5e-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-190">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="83e5e-190">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="83e5e-191">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="83e5e-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="83e5e-193"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="83e5e-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-194">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="83e5e-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="83e5e-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="83e5e-196">(1)</span><span class="sxs-lookup"><span data-stu-id="83e5e-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-197">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="83e5e-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="83e5e-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="83e5e-199">(2)</span><span class="sxs-lookup"><span data-stu-id="83e5e-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="83e5e-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="83e5e-201">(3)</span><span class="sxs-lookup"><span data-stu-id="83e5e-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-202">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="83e5e-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="83e5e-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="83e5e-204">(4)</span><span class="sxs-lookup"><span data-stu-id="83e5e-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-205">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="83e5e-205">Device is not working properly.</span></span> <span data-ttu-id="83e5e-206">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="83e5e-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="83e5e-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="83e5e-208">(5)</span><span class="sxs-lookup"><span data-stu-id="83e5e-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-209">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="83e5e-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="83e5e-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="83e5e-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="83e5e-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-212">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="83e5e-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="83e5e-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="83e5e-214">(7)</span><span class="sxs-lookup"><span data-stu-id="83e5e-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="83e5e-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="83e5e-216">(8)</span><span class="sxs-lookup"><span data-stu-id="83e5e-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-217">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="83e5e-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="83e5e-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="83e5e-219">(9)</span><span class="sxs-lookup"><span data-stu-id="83e5e-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-220">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="83e5e-220">Device is not working properly.</span></span> <span data-ttu-id="83e5e-221">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="83e5e-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="83e5e-223">(10)</span><span class="sxs-lookup"><span data-stu-id="83e5e-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-224">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="83e5e-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="83e5e-226">(11)</span><span class="sxs-lookup"><span data-stu-id="83e5e-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-227">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="83e5e-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="83e5e-229">12</span><span class="sxs-lookup"><span data-stu-id="83e5e-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-230">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="83e5e-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="83e5e-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="83e5e-232">(13)</span><span class="sxs-lookup"><span data-stu-id="83e5e-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-233">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="83e5e-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="83e5e-235">(14)</span><span class="sxs-lookup"><span data-stu-id="83e5e-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-236">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="83e5e-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="83e5e-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="83e5e-238">(15)</span><span class="sxs-lookup"><span data-stu-id="83e5e-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-239">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="83e5e-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="83e5e-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="83e5e-241">(16)</span><span class="sxs-lookup"><span data-stu-id="83e5e-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-242">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="83e5e-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="83e5e-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="83e5e-244">(17)</span><span class="sxs-lookup"><span data-stu-id="83e5e-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-245">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="83e5e-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="83e5e-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="83e5e-247">(18)</span><span class="sxs-lookup"><span data-stu-id="83e5e-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-248">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="83e5e-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="83e5e-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="83e5e-250">(19)</span><span class="sxs-lookup"><span data-stu-id="83e5e-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="83e5e-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="83e5e-252">(20)</span><span class="sxs-lookup"><span data-stu-id="83e5e-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-253">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="83e5e-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="83e5e-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="83e5e-255">(21)</span><span class="sxs-lookup"><span data-stu-id="83e5e-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-256">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="83e5e-256">System failure.</span></span> <span data-ttu-id="83e5e-257">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="83e5e-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="83e5e-258">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="83e5e-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="83e5e-260">(22)</span><span class="sxs-lookup"><span data-stu-id="83e5e-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-261">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="83e5e-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="83e5e-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="83e5e-263">(23)</span><span class="sxs-lookup"><span data-stu-id="83e5e-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-264">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="83e5e-264">System failure.</span></span> <span data-ttu-id="83e5e-265">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="83e5e-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="83e5e-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="83e5e-267">(24)</span><span class="sxs-lookup"><span data-stu-id="83e5e-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-268">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="83e5e-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="83e5e-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="83e5e-270">(25)</span><span class="sxs-lookup"><span data-stu-id="83e5e-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-271">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="83e5e-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="83e5e-273">(26)</span><span class="sxs-lookup"><span data-stu-id="83e5e-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-274">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="83e5e-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="83e5e-276">(27)</span><span class="sxs-lookup"><span data-stu-id="83e5e-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-277">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="83e5e-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="83e5e-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="83e5e-279">(28)</span><span class="sxs-lookup"><span data-stu-id="83e5e-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-280">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="83e5e-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="83e5e-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="83e5e-282">(29)</span><span class="sxs-lookup"><span data-stu-id="83e5e-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-283">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="83e5e-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="83e5e-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="83e5e-285">(30)</span><span class="sxs-lookup"><span data-stu-id="83e5e-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-286">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="83e5e-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="83e5e-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="83e5e-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="83e5e-288">(31)</span><span class="sxs-lookup"><span data-stu-id="83e5e-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-289">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="83e5e-289">Device is not working properly.</span></span> <span data-ttu-id="83e5e-290">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="83e5e-290">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83e5e-291">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="83e5e-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-292">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="83e5e-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-294">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="83e5e-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-295">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="83e5e-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="83e5e-296">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="83e5e-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-300">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83e5e-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-301">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="83e5e-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="83e5e-302">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="83e5e-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="83e5e-303">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-304">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="83e5e-304">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-305">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-305">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-307">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-308">Número de bits usados para exibir cada pixel.</span><span class="sxs-lookup"><span data-stu-id="83e5e-308">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="83e5e-309">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-309">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-310">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="83e5e-310">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-311">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-313">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-314">Número atual de pixels horizontais.</span><span class="sxs-lookup"><span data-stu-id="83e5e-314">Current number of horizontal pixels.</span></span>

<span data-ttu-id="83e5e-315">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-315">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-316">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="83e5e-316">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-317">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="83e5e-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-319">Número de cores com suporte nas resoluções atuais.</span><span class="sxs-lookup"><span data-stu-id="83e5e-319">Number of colors supported at the current resolutions.</span></span>

<span data-ttu-id="83e5e-320">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-320">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="83e5e-321">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="83e5e-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-322">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="83e5e-322">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-323">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-325">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,14 ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-326">Se estiver no modo de caractere, número de colunas para o controlador de vídeo; caso contrário, insira 0.</span><span class="sxs-lookup"><span data-stu-id="83e5e-326">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="83e5e-327">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-327">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-328">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="83e5e-328">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-329">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-331">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,13 ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-332">Se estiver no modo de caractere, número de linhas para este controlador de vídeo; caso contrário, insira 0.</span><span class="sxs-lookup"><span data-stu-id="83e5e-332">If in character mode, number of rows for this video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="83e5e-333">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-333">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-334">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="83e5e-334">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-335">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-337">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-338">Taxa de atualização atual em Hertz.</span><span class="sxs-lookup"><span data-stu-id="83e5e-338">Current refresh rate in hertz.</span></span>

<span data-ttu-id="83e5e-339">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-339">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-340">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="83e5e-340">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-341">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83e5e-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-343">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,8 ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-344">Modo de verificação atual.</span><span class="sxs-lookup"><span data-stu-id="83e5e-344">Current scan mode.</span></span> <span data-ttu-id="83e5e-345">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-345">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83e5e-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="83e5e-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83e5e-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="83e5e-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="83e5e-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Entrelaçado** (3)</span><span class="sxs-lookup"><span data-stu-id="83e5e-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="83e5e-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Não entrelaçado** (4)</span><span class="sxs-lookup"><span data-stu-id="83e5e-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-350">Não entrelaçado</span><span class="sxs-lookup"><span data-stu-id="83e5e-350">Non-interlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83e5e-351">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="83e5e-351">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-352">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-354">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-355">Número atual de pixels verticais.</span><span class="sxs-lookup"><span data-stu-id="83e5e-355">Current number of vertical pixels.</span></span>

<span data-ttu-id="83e5e-356">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-356">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-357">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="83e5e-357">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-358">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-360">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="83e5e-360">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-361">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="83e5e-361">Textual description of the object.</span></span>

<span data-ttu-id="83e5e-362">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-363">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="83e5e-363">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-364">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-366">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83e5e-366">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-367">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="83e5e-367">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="83e5e-368">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-368">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-369">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="83e5e-369">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-370">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="83e5e-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-372">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="83e5e-372">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="83e5e-373">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-374">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="83e5e-374">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-375">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-377">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="83e5e-377">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="83e5e-378">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-379">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="83e5e-379">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-380">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="83e5e-380">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-382">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-383">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="83e5e-383">Date and time the object was installed.</span></span> <span data-ttu-id="83e5e-384">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="83e5e-384">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="83e5e-385">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-386">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="83e5e-386">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-387">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-389">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="83e5e-389">Last error code reported by the logical device.</span></span>

<span data-ttu-id="83e5e-390">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-391">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="83e5e-391">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-392">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-394">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="83e5e-394">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-395">Quantidade máxima de memória com suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="83e5e-395">Maximum amount of memory supported, in bytes.</span></span>

<span data-ttu-id="83e5e-396">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-396">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-397">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="83e5e-397">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-398">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-400">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-401">Número máximo de entidades diretamente endereçáveis com suporte pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="83e5e-401">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="83e5e-402">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="83e5e-402">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="83e5e-403">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-403">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-404">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="83e5e-404">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-405">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-406">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-407">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-408">Taxa máxima de atualização do controlador de vídeo em Hertz.</span><span class="sxs-lookup"><span data-stu-id="83e5e-408">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="83e5e-409">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-409">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-410">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="83e5e-410">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-411">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-412">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-413">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-413">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-414">Taxa mínima de atualização do controlador de vídeo em Hertz.</span><span class="sxs-lookup"><span data-stu-id="83e5e-414">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="83e5e-415">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-415">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-416">**Nome**</span><span class="sxs-lookup"><span data-stu-id="83e5e-416">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-417">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-419">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="83e5e-419">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-420">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="83e5e-420">Label by which the object is known.</span></span> <span data-ttu-id="83e5e-421">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="83e5e-421">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="83e5e-422">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-423">**NumberOfColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="83e5e-423">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-424">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83e5e-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-426">Número atual de planos de cores.</span><span class="sxs-lookup"><span data-stu-id="83e5e-426">Current number of color planes.</span></span> <span data-ttu-id="83e5e-427">Se esse valor não for aplicável para a configuração de vídeo atual, insira 0.</span><span class="sxs-lookup"><span data-stu-id="83e5e-427">If this value is not applicable for the current video configuration, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-428">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="83e5e-428">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-429">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83e5e-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-431">Número de páginas de vídeo com suporte dadas as resoluções atuais e a memória disponível.</span><span class="sxs-lookup"><span data-stu-id="83e5e-431">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="83e5e-432">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-432">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-433">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="83e5e-433">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-436">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="83e5e-436">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-437">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="83e5e-437">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="83e5e-438">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="83e5e-439">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="83e5e-439">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-440">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="83e5e-440">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-441">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83e5e-441">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-443">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="83e5e-443">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="83e5e-444">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="83e5e-444">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83e5e-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="83e5e-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="83e5e-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="83e5e-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="83e5e-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="83e5e-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="83e5e-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="83e5e-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-449">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="83e5e-449">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="83e5e-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="83e5e-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-451">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="83e5e-451">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="83e5e-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="83e5e-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-453">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="83e5e-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="83e5e-454">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="83e5e-454">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="83e5e-455">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="83e5e-455">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="83e5e-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="83e5e-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-457">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="83e5e-457">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="83e5e-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="83e5e-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="83e5e-459">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="83e5e-459">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="83e5e-460">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="83e5e-460">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-461">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="83e5e-461">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-462">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-463">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="83e5e-463">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="83e5e-464">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="83e5e-464">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="83e5e-465">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="83e5e-465">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="83e5e-466">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="83e5e-466">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="83e5e-467">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-468">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="83e5e-468">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-469">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83e5e-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-471">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-471">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-472">Protocolo usado pelo controlador para acessar os dispositivos ' controlados '.</span><span class="sxs-lookup"><span data-stu-id="83e5e-472">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="83e5e-473">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-473">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="83e5e-474">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="83e5e-474">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83e5e-475">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="83e5e-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83e5e-476">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="83e5e-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="83e5e-477">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="83e5e-477">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="83e5e-478">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="83e5e-478">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="83e5e-479">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="83e5e-479">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="83e5e-480">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="83e5e-480">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="83e5e-481">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="83e5e-481">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="83e5e-482">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="83e5e-482">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="83e5e-483">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="83e5e-483">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="83e5e-484">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="83e5e-484">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="83e5e-485">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="83e5e-485">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="83e5e-486">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="83e5e-486">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="83e5e-487">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="83e5e-487">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="83e5e-488">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="83e5e-488">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="83e5e-489">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="83e5e-489">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="83e5e-490">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="83e5e-490">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="83e5e-491">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="83e5e-491">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="83e5e-492">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="83e5e-492">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="83e5e-493">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="83e5e-493">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="83e5e-494">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="83e5e-494">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="83e5e-495">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="83e5e-495">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="83e5e-496">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="83e5e-496">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="83e5e-497">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="83e5e-497">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="83e5e-498">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="83e5e-498">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="83e5e-499">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="83e5e-499">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="83e5e-500">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="83e5e-500">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="83e5e-501">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="83e5e-501">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="83e5e-502">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="83e5e-502">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="83e5e-503">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="83e5e-503">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="83e5e-504">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="83e5e-504">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="83e5e-505">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="83e5e-505">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="83e5e-506">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="83e5e-506">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="83e5e-507">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="83e5e-507">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="83e5e-508">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="83e5e-508">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="83e5e-509">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="83e5e-509">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="83e5e-510">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="83e5e-510">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="83e5e-511">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="83e5e-511">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="83e5e-512">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="83e5e-512">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="83e5e-513">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="83e5e-513">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="83e5e-514">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="83e5e-514">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="83e5e-515">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="83e5e-515">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="83e5e-516">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="83e5e-516">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="83e5e-517">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="83e5e-517">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="83e5e-518">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="83e5e-518">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="83e5e-519">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="83e5e-519">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="83e5e-520">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="83e5e-520">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="83e5e-521">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="83e5e-521">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83e5e-522">**Status**</span><span class="sxs-lookup"><span data-stu-id="83e5e-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-523">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-524">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-525">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="83e5e-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-526">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="83e5e-526">Current status of the object.</span></span> <span data-ttu-id="83e5e-527">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-527">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="83e5e-528">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="83e5e-528">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="83e5e-529">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="83e5e-529">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="83e5e-530">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="83e5e-530">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="83e5e-531">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="83e5e-531">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83e5e-532">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="83e5e-532">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="83e5e-533">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="83e5e-533">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="83e5e-534">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="83e5e-534">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="83e5e-535">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="83e5e-535">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="83e5e-536">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="83e5e-536">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="83e5e-537">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="83e5e-537">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="83e5e-538">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="83e5e-538">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="83e5e-539">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="83e5e-539">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="83e5e-540">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="83e5e-540">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83e5e-541">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="83e5e-541">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-542">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83e5e-542">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-543">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-544">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-545">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="83e5e-545">State of the logical device.</span></span> <span data-ttu-id="83e5e-546">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="83e5e-546">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="83e5e-547">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-547">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83e5e-548">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="83e5e-548">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83e5e-549">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="83e5e-549">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="83e5e-550">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="83e5e-550">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="83e5e-551">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="83e5e-551">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="83e5e-552">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="83e5e-552">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83e5e-553">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="83e5e-553">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-554">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-554">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-555">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-555">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-556">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83e5e-556">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-557">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-557">Scoping system's creation class name.</span></span>

<span data-ttu-id="83e5e-558">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-558">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-559">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="83e5e-559">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-560">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-561">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-562">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="83e5e-562">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-563">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-563">Scoping system's name.</span></span>

<span data-ttu-id="83e5e-564">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-564">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-565">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="83e5e-565">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-566">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="83e5e-566">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-567">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-567">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-568">Data e hora da última redefinição deste controlador, o que significa que o controlador foi desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="83e5e-568">Date and time this controller was last reset meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="83e5e-569">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-569">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-570">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="83e5e-570">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-571">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83e5e-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-572">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-573">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,2 ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-574">Arquitetura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-574">Video architecture.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83e5e-575">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="83e5e-575">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83e5e-576">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="83e5e-576">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="83e5e-577">**CGA** (3)</span><span class="sxs-lookup"><span data-stu-id="83e5e-577">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="83e5e-578">**EGA** (4)</span><span class="sxs-lookup"><span data-stu-id="83e5e-578">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="83e5e-579">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="83e5e-579">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="83e5e-580">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="83e5e-580">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="83e5e-581">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="83e5e-581">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="83e5e-582">**HGC** (8)</span><span class="sxs-lookup"><span data-stu-id="83e5e-582">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="83e5e-583">**MCGA** (9)</span><span class="sxs-lookup"><span data-stu-id="83e5e-583">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="83e5e-584">**8514A** (10)</span><span class="sxs-lookup"><span data-stu-id="83e5e-584">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="83e5e-585">**XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="83e5e-585">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="83e5e-586">**Buffer de quadro linear** (12)</span><span class="sxs-lookup"><span data-stu-id="83e5e-586">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="83e5e-587">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="83e5e-587">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83e5e-588">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="83e5e-588">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-589">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83e5e-589">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-590">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-591">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,6 ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-591">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-592">Tipo de memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-592">Type of video memory.</span></span>

<span data-ttu-id="83e5e-593">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-593">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="83e5e-594">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="83e5e-594">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="83e5e-595">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="83e5e-595">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="83e5e-596">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="83e5e-596">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="83e5e-597">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="83e5e-597">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="83e5e-598">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="83e5e-598">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="83e5e-599">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="83e5e-599">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="83e5e-600">**Edo RAM** (7)</span><span class="sxs-lookup"><span data-stu-id="83e5e-600">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="83e5e-601">**DRAM síncrona intermitente** (8)</span><span class="sxs-lookup"><span data-stu-id="83e5e-601">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="83e5e-602">**SRAM de intermitência em pipeline** (9)</span><span class="sxs-lookup"><span data-stu-id="83e5e-602">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="83e5e-603">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="83e5e-603">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="83e5e-604">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="83e5e-604">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="83e5e-605">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="83e5e-605">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="83e5e-606">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="83e5e-606">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="83e5e-607">**Videomode**</span><span class="sxs-lookup"><span data-stu-id="83e5e-607">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-608">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="83e5e-608">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-609">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-609">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-610">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="83e5e-610">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-611">Modo de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="83e5e-611">Current video mode.</span></span>

</dd> <dt>

<span data-ttu-id="83e5e-612">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="83e5e-612">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83e5e-613">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="83e5e-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="83e5e-614">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83e5e-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="83e5e-615">Cadeia de caracteres de forma livre que descreve o controlador/processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="83e5e-615">Free-form string that describes the video processor/controller.</span></span>

<span data-ttu-id="83e5e-616">Essa propriedade é herdada do [**CIM \_ VideoController**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-616">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83e5e-617">Comentários</span><span class="sxs-lookup"><span data-stu-id="83e5e-617">Remarks</span></span>

<span data-ttu-id="83e5e-618">A classe **CIM \_ PCVideoController** é derivada de [**\_ VideoController CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-618">The **CIM\_PCVideoController** class is derived from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="83e5e-619">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="83e5e-619">WMI does not implement this class.</span></span> <span data-ttu-id="83e5e-620">Para classes WMI derivadas do [**CIM \_ PCVideoController**](cim-videocontroller.md), consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="83e5e-620">For WMI classes derived from [**CIM\_PCVideoController**](cim-videocontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="83e5e-621">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="83e5e-621">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="83e5e-622">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="83e5e-622">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="83e5e-623">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83e5e-623">Requirements</span></span>



| <span data-ttu-id="83e5e-624">Requisito</span><span class="sxs-lookup"><span data-stu-id="83e5e-624">Requirement</span></span> | <span data-ttu-id="83e5e-625">Valor</span><span class="sxs-lookup"><span data-stu-id="83e5e-625">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83e5e-626">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83e5e-626">Minimum supported client</span></span><br/> | <span data-ttu-id="83e5e-627">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83e5e-627">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83e5e-628">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83e5e-628">Minimum supported server</span></span><br/> | <span data-ttu-id="83e5e-629">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83e5e-629">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83e5e-630">Namespace</span><span class="sxs-lookup"><span data-stu-id="83e5e-630">Namespace</span></span><br/>                | <span data-ttu-id="83e5e-631">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="83e5e-631">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="83e5e-632">MOF</span><span class="sxs-lookup"><span data-stu-id="83e5e-632">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83e5e-633"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83e5e-633"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="83e5e-634">DLL</span><span class="sxs-lookup"><span data-stu-id="83e5e-634">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83e5e-635"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83e5e-635"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83e5e-636">Confira também</span><span class="sxs-lookup"><span data-stu-id="83e5e-636">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83e5e-637">**\_VIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="83e5e-637">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> </dl>

 

