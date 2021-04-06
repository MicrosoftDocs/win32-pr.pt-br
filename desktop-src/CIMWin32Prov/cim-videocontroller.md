---
description: A \_ classe CIM VideoController representa os recursos e o gerenciamento do controlador de vídeo.
ms.assetid: 7cf6bf2a-62a5-46fa-8c8f-976604360461
ms.tgt_platform: multiple
title: Classe CIM_VideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoController
- CIM_VideoController.AcceleratorCapabilities
- CIM_VideoController.Availability
- CIM_VideoController.CapabilityDescriptions
- CIM_VideoController.Caption
- CIM_VideoController.ConfigManagerErrorCode
- CIM_VideoController.ConfigManagerUserConfig
- CIM_VideoController.CreationClassName
- CIM_VideoController.CurrentBitsPerPixel
- CIM_VideoController.CurrentHorizontalResolution
- CIM_VideoController.CurrentNumberOfColors
- CIM_VideoController.CurrentNumberOfColumns
- CIM_VideoController.CurrentNumberOfRows
- CIM_VideoController.CurrentRefreshRate
- CIM_VideoController.CurrentScanMode
- CIM_VideoController.CurrentVerticalResolution
- CIM_VideoController.Description
- CIM_VideoController.DeviceID
- CIM_VideoController.ErrorCleared
- CIM_VideoController.ErrorDescription
- CIM_VideoController.InstallDate
- CIM_VideoController.LastErrorCode
- CIM_VideoController.MaxMemorySupported
- CIM_VideoController.MaxNumberControlled
- CIM_VideoController.MaxRefreshRate
- CIM_VideoController.MinRefreshRate
- CIM_VideoController.Name
- CIM_VideoController.NumberOfVideoPages
- CIM_VideoController.PNPDeviceID
- CIM_VideoController.PowerManagementCapabilities
- CIM_VideoController.PowerManagementSupported
- CIM_VideoController.ProtocolSupported
- CIM_VideoController.Status
- CIM_VideoController.StatusInfo
- CIM_VideoController.SystemCreationClassName
- CIM_VideoController.SystemName
- CIM_VideoController.TimeOfLastReset
- CIM_VideoController.VideoMemoryType
- CIM_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6475c99e7a6f2ee1bef56bf2c266c788efc0b805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826594"
---
# <a name="cim_videocontroller-class"></a><span data-ttu-id="79bd3-103">\_Classe CIM VideoController</span><span class="sxs-lookup"><span data-stu-id="79bd3-103">CIM\_VideoController class</span></span>

<span data-ttu-id="79bd3-104">A classe **CIM \_ VideoController** representa os recursos e o gerenciamento do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-104">The **CIM\_VideoController** class represents the capabilities and management of the video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79bd3-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="79bd3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="79bd3-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="79bd3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="79bd3-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="79bd3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="79bd3-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="79bd3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="79bd3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79bd3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE5-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoController : CIM_Controller
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
  uint16   VideoMemoryType;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="79bd3-110">Membros</span><span class="sxs-lookup"><span data-stu-id="79bd3-110">Members</span></span>

<span data-ttu-id="79bd3-111">A classe **CIM \_ VideoController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="79bd3-111">The **CIM\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="79bd3-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="79bd3-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="79bd3-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="79bd3-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="79bd3-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="79bd3-114">Methods</span></span>

<span data-ttu-id="79bd3-115">A classe **CIM \_ VideoController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="79bd3-115">The **CIM\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="79bd3-116">Método</span><span class="sxs-lookup"><span data-stu-id="79bd3-116">Method</span></span>                                                                     | <span data-ttu-id="79bd3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="79bd3-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79bd3-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="79bd3-118">**Reset**</span></span>](reset-method-in-class-cim-videocontroller.md)                 | <span data-ttu-id="79bd3-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79bd3-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="79bd3-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="79bd3-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="79bd3-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="79bd3-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-videocontroller.md) | <span data-ttu-id="79bd3-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="79bd3-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="79bd3-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="79bd3-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="79bd3-124">Properties</span></span>

<span data-ttu-id="79bd3-125">A classe **CIM \_ VideoController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="79bd3-125">The **CIM\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79bd3-126">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="79bd3-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-127">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79bd3-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-129">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="79bd3-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-130">Gráficos e recursos 3-D do controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-130">Graphics and 3-D capabilities of the video controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79bd3-131">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="79bd3-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79bd3-132">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="79bd3-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="79bd3-133">**Acelerador de gráficos** (2)</span><span class="sxs-lookup"><span data-stu-id="79bd3-133">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="79bd3-134">**acelerador 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="79bd3-134">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79bd3-135">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="79bd3-135">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-136">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79bd3-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-138">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-139">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-139">Availability and status of the device.</span></span>

<span data-ttu-id="79bd3-140">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-140">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79bd3-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="79bd3-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79bd3-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="79bd3-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="79bd3-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="79bd3-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="79bd3-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="79bd3-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="79bd3-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="79bd3-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="79bd3-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="79bd3-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="79bd3-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="79bd3-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="79bd3-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="79bd3-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="79bd3-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="79bd3-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="79bd3-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="79bd3-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="79bd3-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="79bd3-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="79bd3-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="79bd3-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="79bd3-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="79bd3-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-154">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="79bd3-154">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="79bd3-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="79bd3-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-156">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-156">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="79bd3-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="79bd3-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-158">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="79bd3-158">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="79bd3-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="79bd3-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="79bd3-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="79bd3-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-161">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="79bd3-161">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="79bd3-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="79bd3-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-163">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="79bd3-163">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="79bd3-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="79bd3-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-165">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="79bd3-165">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="79bd3-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="79bd3-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-167">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-167">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="79bd3-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="79bd3-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-169">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="79bd3-169">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="79bd3-170">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="79bd3-170">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-171">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-173">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM VideoController**.**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="79bd3-173">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-174">Cadeias de caracteres de forma livre que fornecem descrições detalhadas para os recursos do acelerador de vídeo indicados na matriz **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="79bd3-174">Free-form strings that provide detailed descriptions for the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="79bd3-175">Cada entrada dessa matriz está relacionada à entrada na matriz **AcceleratorCapabilities** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="79bd3-175">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="79bd3-176">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="79bd3-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-179">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="79bd3-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-180">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="79bd3-180">Short textual description of the object.</span></span>

<span data-ttu-id="79bd3-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-182">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="79bd3-182">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-183">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-185">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="79bd3-185">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-186">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="79bd3-186">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="79bd3-187">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-187">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="79bd3-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="79bd3-189"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="79bd3-189">(0)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-190">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="79bd3-190">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="79bd3-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="79bd3-192">(1)</span><span class="sxs-lookup"><span data-stu-id="79bd3-192">(1)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-193">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="79bd3-193">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="79bd3-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="79bd3-195">(2)</span><span class="sxs-lookup"><span data-stu-id="79bd3-195">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="79bd3-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="79bd3-197">(3)</span><span class="sxs-lookup"><span data-stu-id="79bd3-197">(3)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-198">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="79bd3-198">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="79bd3-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="79bd3-200">(4)</span><span class="sxs-lookup"><span data-stu-id="79bd3-200">(4)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-201">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="79bd3-201">Device is not working properly.</span></span> <span data-ttu-id="79bd3-202">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="79bd3-202">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="79bd3-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="79bd3-204">(5)</span><span class="sxs-lookup"><span data-stu-id="79bd3-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-205">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="79bd3-205">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="79bd3-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="79bd3-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="79bd3-207">(6)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-208">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="79bd3-208">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="79bd3-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="79bd3-210">(7)</span><span class="sxs-lookup"><span data-stu-id="79bd3-210">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="79bd3-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="79bd3-212">(8)</span><span class="sxs-lookup"><span data-stu-id="79bd3-212">(8)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-213">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="79bd3-213">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="79bd3-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="79bd3-215">(9)</span><span class="sxs-lookup"><span data-stu-id="79bd3-215">(9)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-216">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="79bd3-216">Device is not working properly.</span></span> <span data-ttu-id="79bd3-217">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-217">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="79bd3-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="79bd3-219">(10)</span><span class="sxs-lookup"><span data-stu-id="79bd3-219">(10)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-220">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-220">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="79bd3-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="79bd3-222">(11)</span><span class="sxs-lookup"><span data-stu-id="79bd3-222">(11)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-223">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-223">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="79bd3-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="79bd3-225">12</span><span class="sxs-lookup"><span data-stu-id="79bd3-225">(12)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-226">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="79bd3-226">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="79bd3-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="79bd3-228">(13)</span><span class="sxs-lookup"><span data-stu-id="79bd3-228">(13)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-229">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-229">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="79bd3-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="79bd3-231">(14)</span><span class="sxs-lookup"><span data-stu-id="79bd3-231">(14)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-232">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-232">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="79bd3-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="79bd3-234">(15)</span><span class="sxs-lookup"><span data-stu-id="79bd3-234">(15)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-235">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="79bd3-235">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="79bd3-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="79bd3-237">(16)</span><span class="sxs-lookup"><span data-stu-id="79bd3-237">(16)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-238">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="79bd3-238">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="79bd3-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="79bd3-240">(17)</span><span class="sxs-lookup"><span data-stu-id="79bd3-240">(17)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-241">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="79bd3-241">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="79bd3-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="79bd3-243">(18)</span><span class="sxs-lookup"><span data-stu-id="79bd3-243">(18)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-244">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="79bd3-244">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="79bd3-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="79bd3-246">(19)</span><span class="sxs-lookup"><span data-stu-id="79bd3-246">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="79bd3-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="79bd3-248">(20)</span><span class="sxs-lookup"><span data-stu-id="79bd3-248">(20)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-249">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="79bd3-249">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="79bd3-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="79bd3-251">(21)</span><span class="sxs-lookup"><span data-stu-id="79bd3-251">(21)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-252">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="79bd3-252">System failure.</span></span> <span data-ttu-id="79bd3-253">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="79bd3-253">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="79bd3-254">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-254">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="79bd3-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="79bd3-256">(22)</span><span class="sxs-lookup"><span data-stu-id="79bd3-256">(22)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-257">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-257">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="79bd3-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="79bd3-259">(23)</span><span class="sxs-lookup"><span data-stu-id="79bd3-259">(23)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-260">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="79bd3-260">System failure.</span></span> <span data-ttu-id="79bd3-261">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="79bd3-261">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="79bd3-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="79bd3-263">(24)</span><span class="sxs-lookup"><span data-stu-id="79bd3-263">(24)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-264">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="79bd3-264">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="79bd3-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="79bd3-266">(25)</span><span class="sxs-lookup"><span data-stu-id="79bd3-266">(25)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-267">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="79bd3-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="79bd3-269">(26)</span><span class="sxs-lookup"><span data-stu-id="79bd3-269">(26)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-270">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-270">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="79bd3-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="79bd3-272">(27)</span><span class="sxs-lookup"><span data-stu-id="79bd3-272">(27)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-273">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="79bd3-273">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="79bd3-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="79bd3-275">(28)</span><span class="sxs-lookup"><span data-stu-id="79bd3-275">(28)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-276">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="79bd3-276">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="79bd3-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="79bd3-278">(29)</span><span class="sxs-lookup"><span data-stu-id="79bd3-278">(29)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-279">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-279">Device is disabled.</span></span> <span data-ttu-id="79bd3-280">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="79bd3-280">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="79bd3-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="79bd3-282">(30)</span><span class="sxs-lookup"><span data-stu-id="79bd3-282">(30)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-283">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="79bd3-283">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="79bd3-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79bd3-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="79bd3-285">(31)</span><span class="sxs-lookup"><span data-stu-id="79bd3-285">(31)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-286">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="79bd3-286">Device is not working properly.</span></span> <span data-ttu-id="79bd3-287">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="79bd3-287">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="79bd3-288">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="79bd3-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-289">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79bd3-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-291">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="79bd3-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-292">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="79bd3-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="79bd3-293">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-294">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="79bd3-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-297">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="79bd3-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-298">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="79bd3-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="79bd3-299">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="79bd3-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="79bd3-300">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-301">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="79bd3-301">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-302">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-304">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-304">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-305">Número de bits usados para exibir cada pixel.</span><span class="sxs-lookup"><span data-stu-id="79bd3-305">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-306">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="79bd3-306">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-307">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-309">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-309">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-310">Número atual de pixels horizontais.</span><span class="sxs-lookup"><span data-stu-id="79bd3-310">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-311">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="79bd3-311">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-312">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79bd3-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-314">Número de cores com suporte na resolução atual.</span><span class="sxs-lookup"><span data-stu-id="79bd3-314">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="79bd3-315">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="79bd3-315">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-316">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="79bd3-316">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-317">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-319">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,14 ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-320">Se estiver no modo de caractere, número de colunas para o controlador de vídeo; caso contrário, insira 0.</span><span class="sxs-lookup"><span data-stu-id="79bd3-320">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-321">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="79bd3-321">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-322">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-324">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,13 ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-325">Se estiver no modo de caractere, número de linhas para o controlador de vídeo; caso contrário, insira 0.</span><span class="sxs-lookup"><span data-stu-id="79bd3-325">If in character mode, number of rows for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-326">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="79bd3-326">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-327">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-329">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-330">Taxa de atualização atual, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="79bd3-330">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-331">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="79bd3-331">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-332">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79bd3-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-334">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,8 ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-335">Modo de verificação atual.</span><span class="sxs-lookup"><span data-stu-id="79bd3-335">Current scan mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79bd3-336">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="79bd3-336">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79bd3-337">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="79bd3-337">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="79bd3-338">**Entrelaçado** (3)</span><span class="sxs-lookup"><span data-stu-id="79bd3-338">**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="79bd3-339">**Não entrelaçado** (4)</span><span class="sxs-lookup"><span data-stu-id="79bd3-339">**Non Interlaced** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79bd3-340">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="79bd3-340">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-341">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-343">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-344">Número atual de pixels verticais.</span><span class="sxs-lookup"><span data-stu-id="79bd3-344">Current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-345">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="79bd3-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-348">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="79bd3-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-349">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="79bd3-349">Textual description of the object.</span></span>

<span data-ttu-id="79bd3-350">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="79bd3-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-354">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="79bd3-354">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-355">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79bd3-355">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="79bd3-356">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-357">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="79bd3-357">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-358">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79bd3-358">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-360">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="79bd3-360">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="79bd3-361">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-362">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="79bd3-362">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-363">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-365">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="79bd3-365">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="79bd3-366">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-367">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="79bd3-367">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-368">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="79bd3-368">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-370">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-371">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-371">Date and time the object was installed.</span></span> <span data-ttu-id="79bd3-372">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-372">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="79bd3-373">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-374">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="79bd3-374">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-375">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-377">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79bd3-377">Last error code reported by the logical device.</span></span>

<span data-ttu-id="79bd3-378">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-379">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="79bd3-379">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-380">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-382">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="79bd3-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-383">Quantidade máxima de memória com suporte, em bytes.</span><span class="sxs-lookup"><span data-stu-id="79bd3-383">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-384">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="79bd3-384">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-385">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-386">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-387">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-388">Número máximo de entidades diretamente endereçáveis com suporte pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="79bd3-388">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="79bd3-389">Um valor de 0 deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-389">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="79bd3-390">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-390">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-391">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="79bd3-391">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-392">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-394">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-395">Taxa máxima de atualização do controlador de vídeo, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="79bd3-395">Maximum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-396">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="79bd3-396">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-397">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-397">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-398">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-399">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-400">Taxa mínima de atualização do controlador de vídeo, em Hertz.</span><span class="sxs-lookup"><span data-stu-id="79bd3-400">Minimum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-401">**Nome**</span><span class="sxs-lookup"><span data-stu-id="79bd3-401">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-402">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-404">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="79bd3-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-405">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="79bd3-405">Label by which the object is known.</span></span> <span data-ttu-id="79bd3-406">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="79bd3-406">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="79bd3-407">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-408">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="79bd3-408">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-409">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79bd3-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-411">Número de páginas de vídeo com suporte dadas as resoluções atuais e a memória disponível.</span><span class="sxs-lookup"><span data-stu-id="79bd3-411">Number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-412">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="79bd3-412">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-413">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-415">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="79bd3-415">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-416">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79bd3-416">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="79bd3-417">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="79bd3-418">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="79bd3-418">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-419">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="79bd3-419">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-420">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79bd3-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-422">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79bd3-422">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="79bd3-423">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="79bd3-423">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79bd3-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="79bd3-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="79bd3-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="79bd3-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79bd3-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="79bd3-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79bd3-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="79bd3-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-428">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="79bd3-428">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="79bd3-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="79bd3-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-430">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="79bd3-430">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="79bd3-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="79bd3-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-432">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="79bd3-432">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="79bd3-433">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-433">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="79bd3-434">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="79bd3-434">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="79bd3-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="79bd3-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-436">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="79bd3-436">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="79bd3-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="79bd3-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="79bd3-438">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="79bd3-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="79bd3-439">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="79bd3-439">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-440">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="79bd3-440">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-442">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="79bd3-442">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="79bd3-443">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="79bd3-443">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="79bd3-444">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="79bd3-444">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="79bd3-445">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="79bd3-445">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="79bd3-446">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-447">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="79bd3-447">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-448">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79bd3-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-449">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-450">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-451">Protocolo usado pelo controlador para acessar os dispositivos ' controlados '.</span><span class="sxs-lookup"><span data-stu-id="79bd3-451">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="79bd3-452">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-452">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="79bd3-453">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="79bd3-453">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79bd3-454">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="79bd3-454">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79bd3-455">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="79bd3-455">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="79bd3-456">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="79bd3-456">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="79bd3-457">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="79bd3-457">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="79bd3-458">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="79bd3-458">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="79bd3-459">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="79bd3-459">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="79bd3-460">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="79bd3-460">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="79bd3-461">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="79bd3-461">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="79bd3-462">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="79bd3-462">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="79bd3-463">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="79bd3-463">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="79bd3-464">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="79bd3-464">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="79bd3-465">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="79bd3-465">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="79bd3-466">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="79bd3-466">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="79bd3-467">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="79bd3-467">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="79bd3-468">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="79bd3-468">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="79bd3-469">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="79bd3-469">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="79bd3-470">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="79bd3-470">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="79bd3-471">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="79bd3-471">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="79bd3-472">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="79bd3-472">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="79bd3-473">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="79bd3-473">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="79bd3-474">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="79bd3-474">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="79bd3-475">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="79bd3-475">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="79bd3-476">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="79bd3-476">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="79bd3-477">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="79bd3-477">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="79bd3-478">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="79bd3-478">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="79bd3-479">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="79bd3-479">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="79bd3-480">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="79bd3-480">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="79bd3-481">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="79bd3-481">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="79bd3-482">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="79bd3-482">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="79bd3-483">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="79bd3-483">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="79bd3-484">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="79bd3-484">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="79bd3-485">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="79bd3-485">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="79bd3-486">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="79bd3-486">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="79bd3-487">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="79bd3-487">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="79bd3-488">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="79bd3-488">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="79bd3-489">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="79bd3-489">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="79bd3-490">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="79bd3-490">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="79bd3-491">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="79bd3-491">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="79bd3-492">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="79bd3-492">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="79bd3-493">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="79bd3-493">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="79bd3-494">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="79bd3-494">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="79bd3-495">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="79bd3-495">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="79bd3-496">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="79bd3-496">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="79bd3-497">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="79bd3-497">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="79bd3-498">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="79bd3-498">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="79bd3-499">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="79bd3-499">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="79bd3-500">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="79bd3-500">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79bd3-501">**Status**</span><span class="sxs-lookup"><span data-stu-id="79bd3-501">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-502">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-503">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-504">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="79bd3-504">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-505">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="79bd3-505">Current status of the object.</span></span> <span data-ttu-id="79bd3-506">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-506">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="79bd3-507">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="79bd3-507">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="79bd3-508">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="79bd3-508">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="79bd3-509">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="79bd3-509">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="79bd3-510">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="79bd3-510">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79bd3-511">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="79bd3-511">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="79bd3-512">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="79bd3-512">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="79bd3-513">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="79bd3-513">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="79bd3-514">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="79bd3-514">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="79bd3-515">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="79bd3-515">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="79bd3-516">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="79bd3-516">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="79bd3-517">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="79bd3-517">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="79bd3-518">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="79bd3-518">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="79bd3-519">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="79bd3-519">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79bd3-520">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="79bd3-520">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-521">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79bd3-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-522">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-523">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-524">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79bd3-524">State of the logical device.</span></span> <span data-ttu-id="79bd3-525">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-525">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="79bd3-526">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-526">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79bd3-527">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="79bd3-527">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79bd3-528">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="79bd3-528">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79bd3-529">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="79bd3-529">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79bd3-530">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="79bd3-530">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="79bd3-531">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="79bd3-531">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79bd3-532">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="79bd3-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-533">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-534">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-535">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="79bd3-535">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-536">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-536">Scoping system's creation class name.</span></span>

<span data-ttu-id="79bd3-537">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-537">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-538">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="79bd3-538">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-539">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-540">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-541">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="79bd3-541">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-542">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-542">Scoping system's name.</span></span>

<span data-ttu-id="79bd3-543">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-543">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-544">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="79bd3-544">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-545">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="79bd3-545">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-546">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-546">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-547">Data e hora da última redefinição do controlador, o que significa que o controlador foi desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="79bd3-547">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="79bd3-548">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-548">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="79bd3-549">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="79bd3-549">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-550">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79bd3-550">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-551">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-552">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 3,6 ")</span><span class="sxs-lookup"><span data-stu-id="79bd3-552">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-553">Tipo de memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-553">Type of video memory.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79bd3-554">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="79bd3-554">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79bd3-555">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="79bd3-555">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="79bd3-556">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="79bd3-556">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="79bd3-557">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="79bd3-557">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="79bd3-558">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="79bd3-558">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="79bd3-559">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="79bd3-559">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="79bd3-560">**Edo RAM** (7)</span><span class="sxs-lookup"><span data-stu-id="79bd3-560">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="79bd3-561">**DRAM síncrona intermitente** (8)</span><span class="sxs-lookup"><span data-stu-id="79bd3-561">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="79bd3-562">**SRAM de intermitência em pipeline** (9)</span><span class="sxs-lookup"><span data-stu-id="79bd3-562">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="79bd3-563">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="79bd3-563">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="79bd3-564">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="79bd3-564">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="79bd3-565">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="79bd3-565">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="79bd3-566">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="79bd3-566">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79bd3-567">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="79bd3-567">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79bd3-568">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79bd3-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79bd3-569">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="79bd3-569">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79bd3-570">Cadeia de caracteres de forma livre que descreve o controlador ou processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79bd3-570">Free-form string that describes the video processor or controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79bd3-571">Comentários</span><span class="sxs-lookup"><span data-stu-id="79bd3-571">Remarks</span></span>

<span data-ttu-id="79bd3-572">A classe **CIM \_ VideoController** é derivada do [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-572">The **CIM\_VideoController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="79bd3-573">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="79bd3-573">WMI does not implement this class.</span></span> <span data-ttu-id="79bd3-574">Para classes WMI derivadas do **CIM \_ VideoController**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="79bd3-574">For WMI classes derived from **CIM\_VideoController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="79bd3-575">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="79bd3-575">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="79bd3-576">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="79bd3-576">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="79bd3-577">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79bd3-577">Requirements</span></span>



| <span data-ttu-id="79bd3-578">Requisito</span><span class="sxs-lookup"><span data-stu-id="79bd3-578">Requirement</span></span> | <span data-ttu-id="79bd3-579">Valor</span><span class="sxs-lookup"><span data-stu-id="79bd3-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79bd3-580">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79bd3-580">Minimum supported client</span></span><br/> | <span data-ttu-id="79bd3-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79bd3-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79bd3-582">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79bd3-582">Minimum supported server</span></span><br/> | <span data-ttu-id="79bd3-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79bd3-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79bd3-584">Namespace</span><span class="sxs-lookup"><span data-stu-id="79bd3-584">Namespace</span></span><br/>                | <span data-ttu-id="79bd3-585">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="79bd3-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="79bd3-586">MOF</span><span class="sxs-lookup"><span data-stu-id="79bd3-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79bd3-587"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79bd3-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="79bd3-588">DLL</span><span class="sxs-lookup"><span data-stu-id="79bd3-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79bd3-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79bd3-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79bd3-590">Confira também</span><span class="sxs-lookup"><span data-stu-id="79bd3-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79bd3-591">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="79bd3-591">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

