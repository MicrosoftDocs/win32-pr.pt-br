---
description: A \_ classe de impressora CIM representa os recursos e o gerenciamento do dispositivo lógico da impressora.
ms.assetid: e41ff580-0202-4d3f-8d78-4705d5fb41b3
ms.tgt_platform: multiple
title: Classe CIM_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer
- CIM_Printer.Availability
- CIM_Printer.AvailableJobSheets
- CIM_Printer.Capabilities
- CIM_Printer.CapabilityDescriptions
- CIM_Printer.Caption
- CIM_Printer.CharSetsSupported
- CIM_Printer.ConfigManagerErrorCode
- CIM_Printer.ConfigManagerUserConfig
- CIM_Printer.CreationClassName
- CIM_Printer.CurrentCapabilities
- CIM_Printer.CurrentCharSet
- CIM_Printer.CurrentLanguage
- CIM_Printer.CurrentMimeType
- CIM_Printer.CurrentNaturalLanguage
- CIM_Printer.CurrentPaperType
- CIM_Printer.DefaultCapabilities
- CIM_Printer.DefaultCopies
- CIM_Printer.DefaultLanguage
- CIM_Printer.DefaultMimeType
- CIM_Printer.DefaultNumberUp
- CIM_Printer.DefaultPaperType
- CIM_Printer.Description
- CIM_Printer.DetectedErrorState
- CIM_Printer.DeviceID
- CIM_Printer.ErrorCleared
- CIM_Printer.ErrorDescription
- CIM_Printer.ErrorInformation
- CIM_Printer.HorizontalResolution
- CIM_Printer.InstallDate
- CIM_Printer.JobCountSinceLastReset
- CIM_Printer.LanguagesSupported
- CIM_Printer.LastErrorCode
- CIM_Printer.MarkingTechnology
- CIM_Printer.MaxCopies
- CIM_Printer.MaxNumberUp
- CIM_Printer.MaxSizeSupported
- CIM_Printer.MimeTypesSupported
- CIM_Printer.Name
- CIM_Printer.NaturalLanguagesSupported
- CIM_Printer.PaperSizesSupported
- CIM_Printer.PaperTypesAvailable
- CIM_Printer.PNPDeviceID
- CIM_Printer.PowerManagementCapabilities
- CIM_Printer.PowerManagementSupported
- CIM_Printer.PrinterStatus
- CIM_Printer.Status
- CIM_Printer.StatusInfo
- CIM_Printer.SystemCreationClassName
- CIM_Printer.SystemName
- CIM_Printer.TimeOfLastReset
- CIM_Printer.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c673d6c58e6235e782a718b3b258a15790046eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089625"
---
# <a name="cim_printer-class"></a><span data-ttu-id="1d411-103">\_Classe de impressora CIM</span><span class="sxs-lookup"><span data-stu-id="1d411-103">CIM\_Printer class</span></span>

<span data-ttu-id="1d411-104">A classe de **\_ impressora CIM** representa os recursos e o gerenciamento do dispositivo lógico da impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-104">The **CIM\_Printer** class represents the capabilities and management of the printer logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d411-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="1d411-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1d411-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1d411-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1d411-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1d411-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1d411-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1d411-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d411-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d411-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Printer : CIM_LogicalDevice
{
  uint16   Availability;
  string   AvailableJobSheets[];
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PrinterStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="1d411-110">Membros</span><span class="sxs-lookup"><span data-stu-id="1d411-110">Members</span></span>

<span data-ttu-id="1d411-111">A classe de **\_ impressora CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1d411-111">The **CIM\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="1d411-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1d411-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1d411-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1d411-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1d411-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="1d411-114">Methods</span></span>

<span data-ttu-id="1d411-115">A classe de **\_ impressora CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1d411-115">The **CIM\_Printer** class has these methods.</span></span>



| <span data-ttu-id="1d411-116">Método</span><span class="sxs-lookup"><span data-stu-id="1d411-116">Method</span></span>                                                             | <span data-ttu-id="1d411-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d411-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d411-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="1d411-118">**Reset**</span></span>](reset-method-in-class-cim-printer.md)                 | <span data-ttu-id="1d411-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d411-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="1d411-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="1d411-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="1d411-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1d411-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-printer.md) | <span data-ttu-id="1d411-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="1d411-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="1d411-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="1d411-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1d411-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1d411-124">Properties</span></span>

<span data-ttu-id="1d411-125">A classe de **\_ impressora CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1d411-125">The **CIM\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d411-126">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="1d411-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="1d411-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-130">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d411-130">Availability and status of the device.</span></span>

<span data-ttu-id="1d411-131">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1d411-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-135">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="1d411-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1d411-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1d411-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1d411-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1d411-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="1d411-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1d411-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="1d411-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1d411-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="1d411-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1d411-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="1d411-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1d411-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="1d411-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1d411-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="1d411-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1d411-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="1d411-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-146">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="1d411-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1d411-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="1d411-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-148">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="1d411-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1d411-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="1d411-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-150">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="1d411-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1d411-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="1d411-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1d411-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="1d411-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-153">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="1d411-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1d411-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="1d411-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-155">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="1d411-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1d411-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="1d411-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-157">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="1d411-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1d411-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="1d411-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-159">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="1d411-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1d411-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="1d411-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-161">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="1d411-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-162">**AvailableJobSheets**</span><span class="sxs-lookup"><span data-stu-id="1d411-162">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-163">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-165">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. RequiredJobSheets")</span><span class="sxs-lookup"><span data-stu-id="1d411-165">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-166">Descreve todas as folhas de trabalho que estão disponíveis na impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-166">Describes all of the job sheets that are available on the printer.</span></span> <span data-ttu-id="1d411-167">Isso também pode ser usado para descrever a faixa que uma impressora pode fornecer no início de cada trabalho ou pode descrever outras opções especificadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1d411-167">This can also be used to describe the banner that a printer might provide at the beginning of each job, or can describe other user specified options.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-168">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="1d411-168">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-169">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-171">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ impressora CIM**. CapabilityDescriptions "," CIM \_ PrintJob. concluindo "," CIM \_ PrintCapabilities. Capabilities ")</span><span class="sxs-lookup"><span data-stu-id="1d411-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-172">Recursos da impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-172">Printer capabilities.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d411-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="1d411-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impressão de cores** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="1d411-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impressão duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="1d411-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Cópias** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="1d411-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Agrupamento** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="1d411-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grampeamento** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="1d411-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impressão de transparência** (7)</span><span class="sxs-lookup"><span data-stu-id="1d411-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="1d411-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perfuração** (8)</span><span class="sxs-lookup"><span data-stu-id="1d411-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="1d411-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Capa** (9)</span><span class="sxs-lookup"><span data-stu-id="1d411-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="1d411-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Associar** (10)</span><span class="sxs-lookup"><span data-stu-id="1d411-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="1d411-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impressão em preto e branco** (11)</span><span class="sxs-lookup"><span data-stu-id="1d411-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="1d411-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Um lado** (12)</span><span class="sxs-lookup"><span data-stu-id="1d411-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-186">Um lado</span><span class="sxs-lookup"><span data-stu-id="1d411-186">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="1d411-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borda longa de dois lados** (13)</span><span class="sxs-lookup"><span data-stu-id="1d411-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-188">Borda longa de dois lados</span><span class="sxs-lookup"><span data-stu-id="1d411-188">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="1d411-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borda curta de dois lados** (14)</span><span class="sxs-lookup"><span data-stu-id="1d411-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-190">Borda curta de dois lados</span><span class="sxs-lookup"><span data-stu-id="1d411-190">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="1d411-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Retrato** (15)</span><span class="sxs-lookup"><span data-stu-id="1d411-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="1d411-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paisagem** (16)</span><span class="sxs-lookup"><span data-stu-id="1d411-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="1d411-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverter retrato** (17)</span><span class="sxs-lookup"><span data-stu-id="1d411-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="1d411-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paisagem reversa** (18)</span><span class="sxs-lookup"><span data-stu-id="1d411-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="1d411-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Alta qualidade** (19)</span><span class="sxs-lookup"><span data-stu-id="1d411-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-196">Alta qualidade</span><span class="sxs-lookup"><span data-stu-id="1d411-196">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="1d411-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualidade normal** (20)</span><span class="sxs-lookup"><span data-stu-id="1d411-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-198">Qualidade normal</span><span class="sxs-lookup"><span data-stu-id="1d411-198">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="1d411-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualidade baixa** (21)</span><span class="sxs-lookup"><span data-stu-id="1d411-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-200">Qualidade baixa</span><span class="sxs-lookup"><span data-stu-id="1d411-200">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-201">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1d411-201">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-202">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-202">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-204">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ impressora CIM**.**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="1d411-204">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-205">Cadeias de caracteres de forma livre que fornecem explicações detalhadas para qualquer um dos recursos da impressora indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="1d411-205">Free-form strings that provide detailed explanations for any of the printer features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="1d411-206">Cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="1d411-206">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="1d411-207">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1d411-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-210">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1d411-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-211">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1d411-211">Short textual description of the object.</span></span>

<span data-ttu-id="1d411-212">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-213">**CharSetsSupported**</span><span class="sxs-lookup"><span data-stu-id="1d411-213">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-214">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-216">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. CharSet"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtLocalizationCharacterSet ")</span><span class="sxs-lookup"><span data-stu-id="1d411-216">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-217">Conjuntos de caracteres disponíveis para a saída de texto relacionada ao gerenciamento da impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-217">Available character sets for the output of text related to managing the printer.</span></span> <span data-ttu-id="1d411-218">As cadeias de caracteres fornecidas nesta propriedade devem estar em conformidade com a semântica e a sintaxe especificadas pela seção 4.1.2 ("parâmetro charset") no RFC 2046 (MIME Part 2) e contidas no registro de conjunto de caracteres IANA.</span><span class="sxs-lookup"><span data-stu-id="1d411-218">Strings provided in this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="1d411-219">Os exemplos incluem "UTF-8", "US-ASCII" e "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="1d411-219">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="1d411-220">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1d411-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-221">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d411-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-223">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d411-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-224">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="1d411-224">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="1d411-225">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1d411-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="1d411-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="1d411-227"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="1d411-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-228">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1d411-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1d411-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="1d411-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="1d411-230">(1)</span><span class="sxs-lookup"><span data-stu-id="1d411-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-231">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="1d411-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d411-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d411-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1d411-233">(2)</span><span class="sxs-lookup"><span data-stu-id="1d411-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1d411-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="1d411-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1d411-235">(3)</span><span class="sxs-lookup"><span data-stu-id="1d411-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-236">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="1d411-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1d411-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="1d411-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1d411-238">(4)</span><span class="sxs-lookup"><span data-stu-id="1d411-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-239">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1d411-239">Device is not working properly.</span></span> <span data-ttu-id="1d411-240">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="1d411-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1d411-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="1d411-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1d411-242">(5)</span><span class="sxs-lookup"><span data-stu-id="1d411-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-243">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="1d411-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1d411-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="1d411-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1d411-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-246">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1d411-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1d411-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="1d411-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="1d411-248">(7)</span><span class="sxs-lookup"><span data-stu-id="1d411-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1d411-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="1d411-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1d411-250">(8)</span><span class="sxs-lookup"><span data-stu-id="1d411-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-251">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="1d411-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1d411-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="1d411-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1d411-253">(9)</span><span class="sxs-lookup"><span data-stu-id="1d411-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-254">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1d411-254">Device is not working properly.</span></span> <span data-ttu-id="1d411-255">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d411-255">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1d411-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="1d411-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="1d411-257">(10)</span><span class="sxs-lookup"><span data-stu-id="1d411-257">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-258">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d411-258">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1d411-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="1d411-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="1d411-260">(11)</span><span class="sxs-lookup"><span data-stu-id="1d411-260">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-261">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d411-261">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1d411-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="1d411-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1d411-263">12</span><span class="sxs-lookup"><span data-stu-id="1d411-263">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-264">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="1d411-264">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1d411-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d411-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1d411-266">(13)</span><span class="sxs-lookup"><span data-stu-id="1d411-266">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-267">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d411-267">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1d411-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="1d411-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1d411-269">(14)</span><span class="sxs-lookup"><span data-stu-id="1d411-269">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-270">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="1d411-270">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1d411-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="1d411-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1d411-272">(15)</span><span class="sxs-lookup"><span data-stu-id="1d411-272">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-273">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="1d411-273">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1d411-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="1d411-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1d411-275">(16)</span><span class="sxs-lookup"><span data-stu-id="1d411-275">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-276">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="1d411-276">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1d411-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="1d411-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1d411-278">(17)</span><span class="sxs-lookup"><span data-stu-id="1d411-278">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-279">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="1d411-279">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d411-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d411-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1d411-281">(18)</span><span class="sxs-lookup"><span data-stu-id="1d411-281">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-282">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="1d411-282">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1d411-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="1d411-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="1d411-284">(19)</span><span class="sxs-lookup"><span data-stu-id="1d411-284">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1d411-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="1d411-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="1d411-286">(20)</span><span class="sxs-lookup"><span data-stu-id="1d411-286">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-287">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="1d411-287">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1d411-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d411-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1d411-289">(21)</span><span class="sxs-lookup"><span data-stu-id="1d411-289">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-290">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="1d411-290">System failure.</span></span> <span data-ttu-id="1d411-291">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="1d411-291">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="1d411-292">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d411-292">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1d411-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="1d411-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="1d411-294">(22)</span><span class="sxs-lookup"><span data-stu-id="1d411-294">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-295">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1d411-295">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1d411-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="1d411-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1d411-297">(23)</span><span class="sxs-lookup"><span data-stu-id="1d411-297">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-298">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="1d411-298">System failure.</span></span> <span data-ttu-id="1d411-299">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="1d411-299">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1d411-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="1d411-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1d411-301">(24)</span><span class="sxs-lookup"><span data-stu-id="1d411-301">(24)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-302">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="1d411-302">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1d411-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d411-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1d411-304">(25)</span><span class="sxs-lookup"><span data-stu-id="1d411-304">(25)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-305">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d411-305">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1d411-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d411-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1d411-307">(26)</span><span class="sxs-lookup"><span data-stu-id="1d411-307">(26)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-308">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d411-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1d411-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="1d411-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1d411-310">(27)</span><span class="sxs-lookup"><span data-stu-id="1d411-310">(27)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-311">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="1d411-311">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1d411-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="1d411-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1d411-313">(28)</span><span class="sxs-lookup"><span data-stu-id="1d411-313">(28)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-314">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="1d411-314">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1d411-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="1d411-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1d411-316">(29)</span><span class="sxs-lookup"><span data-stu-id="1d411-316">(29)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-317">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1d411-317">Device is disabled.</span></span> <span data-ttu-id="1d411-318">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="1d411-318">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1d411-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="1d411-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1d411-320">(30)</span><span class="sxs-lookup"><span data-stu-id="1d411-320">(30)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-321">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="1d411-321">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d411-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d411-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1d411-323">(31)</span><span class="sxs-lookup"><span data-stu-id="1d411-323">(31)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-324">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1d411-324">Device is not working properly.</span></span> <span data-ttu-id="1d411-325">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="1d411-325">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-326">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="1d411-326">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-327">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1d411-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-329">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d411-329">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-330">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1d411-330">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1d411-331">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d411-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-335">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d411-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d411-336">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="1d411-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1d411-337">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="1d411-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1d411-338">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-339">**CurrentCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1d411-339">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-340">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-342">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="1d411-342">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-343">As finalidades e outros recursos da impressora que estão em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="1d411-343">Finishings and other capabilities of the printer that are currently in use.</span></span> <span data-ttu-id="1d411-344">Cada entrada nessa propriedade também deve ser listada na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="1d411-344">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d411-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="1d411-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impressão de cores** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="1d411-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impressão duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="1d411-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Cópias** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="1d411-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Agrupamento** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="1d411-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grampeamento** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="1d411-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impressão de transparência** (7)</span><span class="sxs-lookup"><span data-stu-id="1d411-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="1d411-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perfuração** (8)</span><span class="sxs-lookup"><span data-stu-id="1d411-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="1d411-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Capa** (9)</span><span class="sxs-lookup"><span data-stu-id="1d411-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="1d411-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Associar** (10)</span><span class="sxs-lookup"><span data-stu-id="1d411-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="1d411-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impressão em preto e branco** (11)</span><span class="sxs-lookup"><span data-stu-id="1d411-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="1d411-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Um lado** (12)</span><span class="sxs-lookup"><span data-stu-id="1d411-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-358">Um lado</span><span class="sxs-lookup"><span data-stu-id="1d411-358">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="1d411-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borda longa de dois lados** (13)</span><span class="sxs-lookup"><span data-stu-id="1d411-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-360">Borda longa de dois lados</span><span class="sxs-lookup"><span data-stu-id="1d411-360">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="1d411-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borda curta de dois lados** (14)</span><span class="sxs-lookup"><span data-stu-id="1d411-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-362">Borda curta de dois lados</span><span class="sxs-lookup"><span data-stu-id="1d411-362">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="1d411-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Retrato** (15)</span><span class="sxs-lookup"><span data-stu-id="1d411-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="1d411-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paisagem** (16)</span><span class="sxs-lookup"><span data-stu-id="1d411-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="1d411-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverter retrato** (17)</span><span class="sxs-lookup"><span data-stu-id="1d411-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="1d411-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paisagem reversa** (18)</span><span class="sxs-lookup"><span data-stu-id="1d411-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="1d411-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Alta qualidade** (19)</span><span class="sxs-lookup"><span data-stu-id="1d411-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-368">Alta qualidade</span><span class="sxs-lookup"><span data-stu-id="1d411-368">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="1d411-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualidade normal** (20)</span><span class="sxs-lookup"><span data-stu-id="1d411-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-370">Qualidade normal</span><span class="sxs-lookup"><span data-stu-id="1d411-370">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="1d411-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualidade baixa** (21)</span><span class="sxs-lookup"><span data-stu-id="1d411-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-372">Qualidade baixa</span><span class="sxs-lookup"><span data-stu-id="1d411-372">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-373">**CurrentCharSet**</span><span class="sxs-lookup"><span data-stu-id="1d411-373">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-374">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-376">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**CharSetsSupported**")</span><span class="sxs-lookup"><span data-stu-id="1d411-376">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-377">Conjunto de caracteres atual usado para a saída de texto relacionada ao gerenciamento da impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-377">Current character set used for the output of text relating to management of the printer.</span></span> <span data-ttu-id="1d411-378">O conjunto de caracteres descrito por essa propriedade também deve ser listado na propriedade **CharsetsSupported** .</span><span class="sxs-lookup"><span data-stu-id="1d411-378">The character set described by this property should also be listed in the **CharsetsSupported** property.</span></span> <span data-ttu-id="1d411-379">A cadeia de caracteres especificada por essa propriedade deve estar de acordo com a semântica e a sintaxe especificadas pela seção 4.1.2 ("parâmetro charset") no RFC 2046 (MIME Part 2) e contidas no registro de conjunto de caracteres IANA.</span><span class="sxs-lookup"><span data-stu-id="1d411-379">The string specified by this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="1d411-380">Os exemplos incluem "UTF-8", "US-ASCII" e "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="1d411-380">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="1d411-381">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="1d411-381">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-382">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-384">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**. LanguagesSupported "," CIM \_ Printer. CurrentMimeType ")</span><span class="sxs-lookup"><span data-stu-id="1d411-384">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.CurrentMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-385">Idioma da impressora atual que está sendo usado; o idioma também deve ser listado na propriedade **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="1d411-385">Current printer language being used; the language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-386">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-386">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-387">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-387">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="1d411-388">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-388">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="1d411-389">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-389">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="1d411-390">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-390">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="1d411-391">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-391">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="1d411-392">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="1d411-392">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="1d411-393">**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="1d411-393">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="1d411-394">**PPDs** (9)</span><span class="sxs-lookup"><span data-stu-id="1d411-394">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="1d411-395">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="1d411-395">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="1d411-396">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="1d411-396">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="1d411-397">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="1d411-397">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="1d411-398">**Interoperação** (13)</span><span class="sxs-lookup"><span data-stu-id="1d411-398">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="1d411-399">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="1d411-399">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="1d411-400">**Dados da linha** (15)</span><span class="sxs-lookup"><span data-stu-id="1d411-400">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="1d411-401">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="1d411-401">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="1d411-402">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="1d411-402">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="1d411-403">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="1d411-403">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="1d411-404">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="1d411-404">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="1d411-405">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="1d411-405">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="1d411-406">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="1d411-406">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="1d411-407">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="1d411-407">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="1d411-408">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="1d411-408">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="1d411-409">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="1d411-409">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="1d411-410">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="1d411-410">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="1d411-411">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="1d411-411">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="1d411-412">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="1d411-412">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="1d411-413">**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="1d411-413">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="1d411-414">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="1d411-414">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="1d411-415">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="1d411-415">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="1d411-416">**Texto simples** (31)</span><span class="sxs-lookup"><span data-stu-id="1d411-416">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="1d411-417">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="1d411-417">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="1d411-418">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="1d411-418">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="1d411-419">**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="1d411-419">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="1d411-420">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="1d411-420">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="1d411-421">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="1d411-421">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="1d411-422">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="1d411-422">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="1d411-423">**Automático** (38)</span><span class="sxs-lookup"><span data-stu-id="1d411-423">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="1d411-424">**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="1d411-424">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="1d411-425">**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="1d411-425">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="1d411-426">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="1d411-426">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="1d411-427">**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="1d411-427">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="1d411-428">**CaPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="1d411-428">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="1d411-429">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="1d411-429">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="1d411-430">**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="1d411-430">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="1d411-431">**CES** (46)</span><span class="sxs-lookup"><span data-stu-id="1d411-431">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="1d411-432">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="1d411-432">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-433">**CurrentMimeType**</span><span class="sxs-lookup"><span data-stu-id="1d411-433">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-436">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**CurrentLanguage**")</span><span class="sxs-lookup"><span data-stu-id="1d411-436">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-437">Tipo MIME atualmente em uso pela impressora quando a propriedade **CurrentLanguage** está definida para indicar que um tipo MIME está em uso.</span><span class="sxs-lookup"><span data-stu-id="1d411-437">Mime type currently in use by the printer when the **CurrentLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-438">**CurrentNaturalLanguage**</span><span class="sxs-lookup"><span data-stu-id="1d411-438">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-439">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-441">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**NaturalLanguagesSupported**")</span><span class="sxs-lookup"><span data-stu-id="1d411-441">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-442">Idioma atual em uso pela impressora para gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="1d411-442">Current language in use by the printer for management.</span></span> <span data-ttu-id="1d411-443">A linguagem listada aqui também deve ser listada em **NaturalLanguagesSupported**.</span><span class="sxs-lookup"><span data-stu-id="1d411-443">The language listed here should also be listed in **NaturalLanguagesSupported**.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-444">**CurrentPaperType**</span><span class="sxs-lookup"><span data-stu-id="1d411-444">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-445">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-447">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="1d411-447">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-448">Tipo de papel atualmente em uso pela impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-448">Paper type currently in use by the printer.</span></span> <span data-ttu-id="1d411-449">A cadeia de caracteres deve ser expressa no formulário especificado pelo DPA (aplicativo de impressão de documentos) ISO/IEC 10175, que também é resumido no Apêndice C do RFC 1759 (MIB de impressora).</span><span class="sxs-lookup"><span data-stu-id="1d411-449">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-450">**Funções de recursos**</span><span class="sxs-lookup"><span data-stu-id="1d411-450">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-451">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-451">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-452">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-453">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="1d411-453">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-454">As finalidades padrão e outros recursos da impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-454">Default finishings and other capabilities of the printer.</span></span> <span data-ttu-id="1d411-455">Cada entrada nessa propriedade também deve ser listada na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="1d411-455">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d411-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="1d411-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impressão de cores** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="1d411-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impressão duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="1d411-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Cópias** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="1d411-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Agrupamento** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="1d411-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grampeamento** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="1d411-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impressão de transparência** (7)</span><span class="sxs-lookup"><span data-stu-id="1d411-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="1d411-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perfuração** (8)</span><span class="sxs-lookup"><span data-stu-id="1d411-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="1d411-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Capa** (9)</span><span class="sxs-lookup"><span data-stu-id="1d411-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="1d411-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Associar** (10)</span><span class="sxs-lookup"><span data-stu-id="1d411-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="1d411-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impressão em preto e branco** (11)</span><span class="sxs-lookup"><span data-stu-id="1d411-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="1d411-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Um lado** (12)</span><span class="sxs-lookup"><span data-stu-id="1d411-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-469">Um lado</span><span class="sxs-lookup"><span data-stu-id="1d411-469">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="1d411-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borda longa de dois lados** (13)</span><span class="sxs-lookup"><span data-stu-id="1d411-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-471">Borda longa de dois lados</span><span class="sxs-lookup"><span data-stu-id="1d411-471">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="1d411-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borda curta de dois lados** (14)</span><span class="sxs-lookup"><span data-stu-id="1d411-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-473">Borda curta de dois lados</span><span class="sxs-lookup"><span data-stu-id="1d411-473">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="1d411-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Retrato** (15)</span><span class="sxs-lookup"><span data-stu-id="1d411-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="1d411-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paisagem** (16)</span><span class="sxs-lookup"><span data-stu-id="1d411-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="1d411-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverter retrato** (17)</span><span class="sxs-lookup"><span data-stu-id="1d411-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="1d411-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paisagem reversa** (18)</span><span class="sxs-lookup"><span data-stu-id="1d411-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="1d411-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Alta qualidade** (19)</span><span class="sxs-lookup"><span data-stu-id="1d411-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-479">Alta qualidade</span><span class="sxs-lookup"><span data-stu-id="1d411-479">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="1d411-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualidade normal** (20)</span><span class="sxs-lookup"><span data-stu-id="1d411-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-481">Qualidade normal</span><span class="sxs-lookup"><span data-stu-id="1d411-481">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="1d411-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualidade baixa** (21)</span><span class="sxs-lookup"><span data-stu-id="1d411-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-483">Qualidade baixa</span><span class="sxs-lookup"><span data-stu-id="1d411-483">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-484">**Defaultcopies**</span><span class="sxs-lookup"><span data-stu-id="1d411-484">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-485">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d411-485">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-486">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d411-487">Número de cópias que um único trabalho produzirá, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="1d411-487">Number of copies that a single job will produce, unless otherwise specified.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-488">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="1d411-488">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-489">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-489">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-490">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-491">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**. LanguagesSupported "," CIM \_ Printer. Defaultmimetype ")</span><span class="sxs-lookup"><span data-stu-id="1d411-491">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.DefaultMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-492">Idioma padrão da impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-492">Default printer language.</span></span> <span data-ttu-id="1d411-493">O idioma também deve ser listado na propriedade **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="1d411-493">The language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-494">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-495">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="1d411-496">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-496">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="1d411-497">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-497">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="1d411-498">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-498">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="1d411-499">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-499">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="1d411-500">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="1d411-500">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="1d411-501">**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="1d411-501">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="1d411-502">**PPDs** (9)</span><span class="sxs-lookup"><span data-stu-id="1d411-502">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="1d411-503">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="1d411-503">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="1d411-504">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="1d411-504">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="1d411-505">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="1d411-505">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="1d411-506">**Interoperação** (13)</span><span class="sxs-lookup"><span data-stu-id="1d411-506">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="1d411-507">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="1d411-507">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="1d411-508">**Dados da linha** (15)</span><span class="sxs-lookup"><span data-stu-id="1d411-508">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="1d411-509">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="1d411-509">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="1d411-510">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="1d411-510">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="1d411-511">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="1d411-511">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="1d411-512">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="1d411-512">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="1d411-513">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="1d411-513">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="1d411-514">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="1d411-514">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="1d411-515">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="1d411-515">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="1d411-516">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="1d411-516">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="1d411-517">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="1d411-517">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="1d411-518">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="1d411-518">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="1d411-519">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="1d411-519">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="1d411-520">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="1d411-520">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="1d411-521">**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="1d411-521">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="1d411-522">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="1d411-522">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="1d411-523">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="1d411-523">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="1d411-524">**Texto simples** (31)</span><span class="sxs-lookup"><span data-stu-id="1d411-524">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="1d411-525">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="1d411-525">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="1d411-526">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="1d411-526">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="1d411-527">**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="1d411-527">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="1d411-528">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="1d411-528">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="1d411-529">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="1d411-529">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="1d411-530">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="1d411-530">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="1d411-531">**Automático** (38)</span><span class="sxs-lookup"><span data-stu-id="1d411-531">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="1d411-532">**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="1d411-532">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="1d411-533">**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="1d411-533">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="1d411-534">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="1d411-534">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="1d411-535">**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="1d411-535">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="1d411-536">**CaPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="1d411-536">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="1d411-537">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="1d411-537">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="1d411-538">**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="1d411-538">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="1d411-539">**CES** (46)</span><span class="sxs-lookup"><span data-stu-id="1d411-539">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="1d411-540">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="1d411-540">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-541">**Defaultmimetype**</span><span class="sxs-lookup"><span data-stu-id="1d411-541">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-542">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-543">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-544">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="1d411-544">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-545">Tipo MIME padrão usado pela impressora quando a propriedade **DefaultLanguage** está definida para indicar que um tipo MIME está em uso.</span><span class="sxs-lookup"><span data-stu-id="1d411-545">Default mime type used by the printer when the **DefaultLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-546">**DefaultNumberUp**</span><span class="sxs-lookup"><span data-stu-id="1d411-546">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-547">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d411-547">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-548">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d411-549">Número de páginas de fluxo de impressão que a impressora processará em uma única folha de mídia, a menos que um trabalho especifique o contrário.</span><span class="sxs-lookup"><span data-stu-id="1d411-549">Number of print-stream pages that the printer will render onto a single media sheet, unless a job specifies otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-550">**Defaultpapertype**</span><span class="sxs-lookup"><span data-stu-id="1d411-550">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-551">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-552">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-553">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="1d411-553">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-554">Tipo de papel que a impressora usará se PrintJob não especificar um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="1d411-554">Paper type that the printer will use if PrintJob does not specify a particular type.</span></span> <span data-ttu-id="1d411-555">A cadeia de caracteres deve ser expressa no formulário especificado pelo DPA (aplicativo de impressão de documentos) ISO/IEC 10175, que também é resumido no Apêndice C do RFC 1759 (MIB de impressora).</span><span class="sxs-lookup"><span data-stu-id="1d411-555">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-556">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1d411-556">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-557">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-558">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-559">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="1d411-559">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-560">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1d411-560">Textual description of the object.</span></span>

<span data-ttu-id="1d411-561">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-561">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-562">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="1d411-562">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-563">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-563">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-564">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-565">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIB. IETF \| Printer-MIB. hrPrinterDetectedErrorState ")</span><span class="sxs-lookup"><span data-stu-id="1d411-565">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-566">Informações de erro da impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-566">Printer error information.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-567">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d411-567">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-568">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="1d411-569">**Sem erro** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-569">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="1d411-570">**Papel baixo** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-570">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="1d411-571">**Sem papel** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-571">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="1d411-572">**Toner baixo** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-572">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="1d411-573">**Sem toner** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-573">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="1d411-574">**Porta aberta** (7)</span><span class="sxs-lookup"><span data-stu-id="1d411-574">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="1d411-575">**Emperrado** (8)</span><span class="sxs-lookup"><span data-stu-id="1d411-575">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="1d411-576">**Offline** (9)</span><span class="sxs-lookup"><span data-stu-id="1d411-576">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="1d411-577">**Serviço solicitado** (10)</span><span class="sxs-lookup"><span data-stu-id="1d411-577">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="1d411-578">**Escaninho de saída cheio** (11)</span><span class="sxs-lookup"><span data-stu-id="1d411-578">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-579">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1d411-579">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-580">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-581">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-582">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d411-582">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d411-583">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d411-583">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="1d411-584">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-584">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-585">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1d411-585">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-586">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1d411-586">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-587">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-587">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d411-588">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="1d411-588">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="1d411-589">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-589">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-590">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1d411-590">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-591">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-592">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-592">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d411-593">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="1d411-593">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="1d411-594">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-595">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="1d411-595">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-596">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-596">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-597">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1d411-597">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d411-598">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**DetectedErrorState**")</span><span class="sxs-lookup"><span data-stu-id="1d411-598">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-599">Matriz que fornece informações complementares para o estado de erro atual, indicado na propriedade **DetectedErrorState** .</span><span class="sxs-lookup"><span data-stu-id="1d411-599">Array that provides supplemental information for the current error state, indicated in the **DetectedErrorState** property.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-600">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="1d411-600">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-601">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d411-601">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-602">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-603">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. HorizontalResolution"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels por polegada")</span><span class="sxs-lookup"><span data-stu-id="1d411-603">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-604">Resolução horizontal em pixels por polegada.</span><span class="sxs-lookup"><span data-stu-id="1d411-604">Horizontal resolution in pixels-per-inch.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-605">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1d411-605">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-606">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d411-606">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-607">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-608">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="1d411-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-609">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="1d411-609">Date and time the object was installed.</span></span> <span data-ttu-id="1d411-610">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d411-610">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1d411-611">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-611">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-612">**JobCountSinceLastReset**</span><span class="sxs-lookup"><span data-stu-id="1d411-612">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-613">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d411-613">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-614">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-615">Qualificadores: **contador**</span><span class="sxs-lookup"><span data-stu-id="1d411-615">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="1d411-616">Trabalhos de impressora processados desde a última redefinição.</span><span class="sxs-lookup"><span data-stu-id="1d411-616">Printer jobs processed since the last reset.</span></span> <span data-ttu-id="1d411-617">Esses trabalhos podem ser processados de uma ou mais filas de impressão.</span><span class="sxs-lookup"><span data-stu-id="1d411-617">These jobs can be processed from one or more print queues.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-618">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="1d411-618">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-619">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-619">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-620">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-621">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtInterpreterLangFamily "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**. MimeTypesSupported "," CIM \_ PrintJob. Language "," CIM \_ reservice. LanguagesSupported ")</span><span class="sxs-lookup"><span data-stu-id="1d411-621">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-622">Idiomas de impressão com suporte nativo.</span><span class="sxs-lookup"><span data-stu-id="1d411-622">Print languages that are natively supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-623">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-623">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-624">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-624">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="1d411-625">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-625">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="1d411-626">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-626">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="1d411-627">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-627">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="1d411-628">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-628">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="1d411-629">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="1d411-629">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="1d411-630">**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="1d411-630">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="1d411-631">**PPDs** (9)</span><span class="sxs-lookup"><span data-stu-id="1d411-631">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="1d411-632">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="1d411-632">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="1d411-633">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="1d411-633">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="1d411-634">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="1d411-634">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="1d411-635">**Interoperação** (13)</span><span class="sxs-lookup"><span data-stu-id="1d411-635">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="1d411-636">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="1d411-636">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="1d411-637">**Dados da linha** (15)</span><span class="sxs-lookup"><span data-stu-id="1d411-637">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="1d411-638">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="1d411-638">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="1d411-639">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="1d411-639">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="1d411-640">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="1d411-640">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="1d411-641">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="1d411-641">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="1d411-642">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="1d411-642">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="1d411-643">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="1d411-643">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="1d411-644">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="1d411-644">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="1d411-645">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="1d411-645">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="1d411-646">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="1d411-646">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="1d411-647">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="1d411-647">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="1d411-648">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="1d411-648">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="1d411-649">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="1d411-649">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="1d411-650">**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="1d411-650">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="1d411-651">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="1d411-651">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="1d411-652">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="1d411-652">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="1d411-653">**Texto simples** (31)</span><span class="sxs-lookup"><span data-stu-id="1d411-653">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="1d411-654">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="1d411-654">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="1d411-655">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="1d411-655">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="1d411-656">**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="1d411-656">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="1d411-657">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="1d411-657">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="1d411-658">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="1d411-658">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="1d411-659">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="1d411-659">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="1d411-660">**Automático** (38)</span><span class="sxs-lookup"><span data-stu-id="1d411-660">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="1d411-661">**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="1d411-661">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="1d411-662">**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="1d411-662">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="1d411-663">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="1d411-663">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="1d411-664">**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="1d411-664">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="1d411-665">**CaPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="1d411-665">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="1d411-666">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="1d411-666">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="1d411-667">**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="1d411-667">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="1d411-668">**CES** (46)</span><span class="sxs-lookup"><span data-stu-id="1d411-668">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="1d411-669">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="1d411-669">**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="1d411-670">**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="1d411-670">**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="1d411-671">**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="1d411-671">**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="1d411-672">**PCLXL** (50)</span><span class="sxs-lookup"><span data-stu-id="1d411-672">**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-673">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1d411-673">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-674">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d411-674">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-675">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-675">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d411-676">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d411-676">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1d411-677">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-677">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-678">**MarkingTechnology**</span><span class="sxs-lookup"><span data-stu-id="1d411-678">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-679">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-679">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-680">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-681">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtMarkerMarkTech ")</span><span class="sxs-lookup"><span data-stu-id="1d411-681">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-682">Marcando a tecnologia usada pela impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-682">Marking technology used by the printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-683">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-683">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-684">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-684">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="1d411-685">**LED de Electrophotographic** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-685">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="1d411-686">**Electrophotographic laser** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-686">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="1d411-687">**Electrophotographic outro** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-687">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="1d411-688">**Impacto ao mover matriz de ponto de cabeçalho 9pin** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-688">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="1d411-689">**Impacto ao mover matriz de ponto de cabeçalho 24pin** (7)</span><span class="sxs-lookup"><span data-stu-id="1d411-689">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="1d411-690">**Impacto ao mover matriz de ponto de cabeçalho outro** (8)</span><span class="sxs-lookup"><span data-stu-id="1d411-690">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="1d411-691">**Cabeçalho de movimentação de impacto totalmente formado** (9)</span><span class="sxs-lookup"><span data-stu-id="1d411-691">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="1d411-692">**Faixa de impacto** (10)</span><span class="sxs-lookup"><span data-stu-id="1d411-692">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="1d411-693">**Outro impacto** (11)</span><span class="sxs-lookup"><span data-stu-id="1d411-693">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="1d411-694">**Jato de aqueous** (12)</span><span class="sxs-lookup"><span data-stu-id="1d411-694">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="1d411-695">**Jato de radiosolid** (13)</span><span class="sxs-lookup"><span data-stu-id="1d411-695">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="1d411-696">**Outro jato** de Radio(14)</span><span class="sxs-lookup"><span data-stu-id="1d411-696">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="1d411-697">**Caneta** (15)</span><span class="sxs-lookup"><span data-stu-id="1d411-697">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="1d411-698">**Transferência térmica** (16)</span><span class="sxs-lookup"><span data-stu-id="1d411-698">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="1d411-699">**Sensível à térmica** (17)</span><span class="sxs-lookup"><span data-stu-id="1d411-699">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="1d411-700">**Difusão térmica** (18)</span><span class="sxs-lookup"><span data-stu-id="1d411-700">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="1d411-701">**Outros térmicas** (19)</span><span class="sxs-lookup"><span data-stu-id="1d411-701">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="1d411-702">**Electroerosion** (20)</span><span class="sxs-lookup"><span data-stu-id="1d411-702">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="1d411-703">**Eletrostática** (21)</span><span class="sxs-lookup"><span data-stu-id="1d411-703">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="1d411-704">**Microfilme fotográfico** (22)</span><span class="sxs-lookup"><span data-stu-id="1d411-704">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="1d411-705">**Fotocompositora fotográfica** (23)</span><span class="sxs-lookup"><span data-stu-id="1d411-705">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="1d411-706">**Outro fotográfico** (24)</span><span class="sxs-lookup"><span data-stu-id="1d411-706">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="1d411-707">**Desposição de íon** (25)</span><span class="sxs-lookup"><span data-stu-id="1d411-707">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="1d411-708">**eBeam** (26)</span><span class="sxs-lookup"><span data-stu-id="1d411-708">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="1d411-709">**Typesetter** (27)</span><span class="sxs-lookup"><span data-stu-id="1d411-709">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-710">**MaxCopies**</span><span class="sxs-lookup"><span data-stu-id="1d411-710">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-711">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d411-711">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-712">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-713">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. Copies")</span><span class="sxs-lookup"><span data-stu-id="1d411-713">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-714">Número máximo de cópias que podem ser produzidas pela impressora a partir de um único trabalho.</span><span class="sxs-lookup"><span data-stu-id="1d411-714">Maximum number of copies that can be produced by the printer from a single job.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-715">**MaxNumberUp**</span><span class="sxs-lookup"><span data-stu-id="1d411-715">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-716">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d411-716">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-717">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-717">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-718">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. NumberUp")</span><span class="sxs-lookup"><span data-stu-id="1d411-718">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-719">Número máximo de páginas de fluxo de impressão que a impressora pode processar em uma única folha de mídia.</span><span class="sxs-lookup"><span data-stu-id="1d411-719">Maximum number of print-stream pages that the printer can render onto a single media sheet.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-720">**MaxSizeSupported**</span><span class="sxs-lookup"><span data-stu-id="1d411-720">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-721">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d411-721">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-722">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-722">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-723">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. Jobs"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="1d411-723">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.JobSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-724">O maior trabalho (como um fluxo de bytes) que a impressora aceitará em unidades de kilobytes.</span><span class="sxs-lookup"><span data-stu-id="1d411-724">Largest job (as a byte stream) that the printer will accept in units of kilobytes.</span></span> <span data-ttu-id="1d411-725">Um valor de 0 (zero) indica que nenhum limite foi definido.</span><span class="sxs-lookup"><span data-stu-id="1d411-725">A value of 0 (zero) indicates that no limit has been set.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-726">**MimeTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="1d411-726">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-727">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-727">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-728">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-728">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-729">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**. LanguagesSupported "," CIM \_ PrintJob. mimeTypes "," CIM \_ Autoservice. MimeTypesSupported ")</span><span class="sxs-lookup"><span data-stu-id="1d411-729">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-730">Cadeias de caracteres de forma livre que fornecem explicações detalhadas de tipos MIME com suporte pela impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-730">Free-form strings that provide detailed explanations of mime types that are supported by the printer.</span></span> <span data-ttu-id="1d411-731">Se os dados forem fornecidos para essa propriedade, o valor 47 ("MIME") deverá ser incluído na propriedade **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="1d411-731">If data is provided for this property, then the value 47 ("Mime"), should be included in the **LanguagesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-732">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1d411-732">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-733">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-733">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-734">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-734">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-735">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1d411-735">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-736">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="1d411-736">Label by which the object is known.</span></span> <span data-ttu-id="1d411-737">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="1d411-737">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="1d411-738">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-738">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-739">**NaturalLanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="1d411-739">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-740">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-740">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-741">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-741">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-742">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtLocalizationLanguage "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ PrintJob. NaturalLanguage ")</span><span class="sxs-lookup"><span data-stu-id="1d411-742">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-743">Idiomas disponíveis para cadeias de caracteres usadas pela impressora para saída de informações de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="1d411-743">Available languages for strings used by the printer for management information output.</span></span> <span data-ttu-id="1d411-744">As cadeias de caracteres devem estar em conformidade com a RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="1d411-744">The strings should conform to RFC 1766.</span></span> <span data-ttu-id="1d411-745">Por exemplo, "en" é usado para inglês.</span><span class="sxs-lookup"><span data-stu-id="1d411-745">For example, "en" is used for English.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-746">**PaperSizesSupported**</span><span class="sxs-lookup"><span data-stu-id="1d411-746">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-747">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-747">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-748">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-748">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d411-749">Tipos de papel com suporte.</span><span class="sxs-lookup"><span data-stu-id="1d411-749">Types of paper supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-750">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d411-750">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-751">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-751">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="1d411-752">**A** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-752">**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="1d411-753">**B** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-753">**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="1d411-754">**C** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-754">**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="1d411-755">**D** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-755">**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="1d411-756">**E** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-756">**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="1d411-757">**Letra** (7)</span><span class="sxs-lookup"><span data-stu-id="1d411-757">**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="1d411-758">**Ofício** (8)</span><span class="sxs-lookup"><span data-stu-id="1d411-758">**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="1d411-759">**Na-10x13-envelope** (9)</span><span class="sxs-lookup"><span data-stu-id="1d411-759">**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="1d411-760">**Na-9x12-envelope** (10)</span><span class="sxs-lookup"><span data-stu-id="1d411-760">**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="1d411-761">**Na-número-10-envelope** (11)</span><span class="sxs-lookup"><span data-stu-id="1d411-761">**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="1d411-762">**Na-7x9-envelope** (12)</span><span class="sxs-lookup"><span data-stu-id="1d411-762">**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="1d411-763">**Na-9x11-envelope** (13)</span><span class="sxs-lookup"><span data-stu-id="1d411-763">**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="1d411-764">**Na-10x14-envelope** (14)</span><span class="sxs-lookup"><span data-stu-id="1d411-764">**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="1d411-765">**Na-número-9-envelope** (15)</span><span class="sxs-lookup"><span data-stu-id="1d411-765">**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="1d411-766">**Na-6x9-envelope** (16)</span><span class="sxs-lookup"><span data-stu-id="1d411-766">**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="1d411-767">**Na-10x15-envelope** (17)</span><span class="sxs-lookup"><span data-stu-id="1d411-767">**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="1d411-768">**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="1d411-768">**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="1d411-769">**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="1d411-769">**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="1d411-770">**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="1d411-770">**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="1d411-771">**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="1d411-771">**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="1d411-772">**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="1d411-772">**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="1d411-773">**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="1d411-773">**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="1d411-774">**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="1d411-774">**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="1d411-775">**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="1d411-775">**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="1d411-776">**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="1d411-776">**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="1d411-777">**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="1d411-777">**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="1d411-778">**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="1d411-778">**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="1d411-779">**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="1d411-779">**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="1d411-780">**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="1d411-780">**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="1d411-781">**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="1d411-781">**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="1d411-782">**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="1d411-782">**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="1d411-783">**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="1d411-783">**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="1d411-784">**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="1d411-784">**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="1d411-785">**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="1d411-785">**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="1d411-786">**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="1d411-786">**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="1d411-787">**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="1d411-787">**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="1d411-788">**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="1d411-788">**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="1d411-789">**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="1d411-789">**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="1d411-790">**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="1d411-790">**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="1d411-791">**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="1d411-791">**C2C3** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="1d411-792">**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="1d411-792">**C4** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="1d411-793">**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="1d411-793">**C5** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="1d411-794">**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="1d411-794">**C6** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="1d411-795">**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="1d411-795">**C7** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="1d411-796">**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="1d411-796">**C8** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="1d411-797">**Designado por ISO** (47)</span><span class="sxs-lookup"><span data-stu-id="1d411-797">**ISO-Designated** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="1d411-798">**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="1d411-798">**JIS B0** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="1d411-799">**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="1d411-799">**JIS B1** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="1d411-800">**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="1d411-800">**JIS B2** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="1d411-801">**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="1d411-801">**JIS B3** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="1d411-802">**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="1d411-802">**JIS B4** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="1d411-803">**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="1d411-803">**JIS B5** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="1d411-804">**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="1d411-804">**JIS B6** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="1d411-805">**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="1d411-805">**JIS B7** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="1d411-806">**JIS B8** (56)</span><span class="sxs-lookup"><span data-stu-id="1d411-806">**JIS B8** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="1d411-807">**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="1d411-807">**JIS B9** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="1d411-808">**JIS B10** (58)</span><span class="sxs-lookup"><span data-stu-id="1d411-808">**JIS B10** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="1d411-809">**Na-letra** (59)</span><span class="sxs-lookup"><span data-stu-id="1d411-809">**NA-Letter** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="1d411-810">**Na-ofício** (60)</span><span class="sxs-lookup"><span data-stu-id="1d411-810">**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="1d411-811">**B4-envelope** (61)</span><span class="sxs-lookup"><span data-stu-id="1d411-811">**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="1d411-812">**B5-envelope** (62)</span><span class="sxs-lookup"><span data-stu-id="1d411-812">**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="1d411-813">**C3-envelope** (63)</span><span class="sxs-lookup"><span data-stu-id="1d411-813">**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="1d411-814">**C4-envelope** (64)</span><span class="sxs-lookup"><span data-stu-id="1d411-814">**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="1d411-815">**C5-envelope** (65)</span><span class="sxs-lookup"><span data-stu-id="1d411-815">**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="1d411-816">**C6-envelope** (66)</span><span class="sxs-lookup"><span data-stu-id="1d411-816">**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="1d411-817">**Designado – envelope longo** (67)</span><span class="sxs-lookup"><span data-stu-id="1d411-817">**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="1d411-818">**Monarch-envelope** (68)</span><span class="sxs-lookup"><span data-stu-id="1d411-818">**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="1d411-819">**Executivo** (69)</span><span class="sxs-lookup"><span data-stu-id="1d411-819">**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="1d411-820">**Fólio** (70)</span><span class="sxs-lookup"><span data-stu-id="1d411-820">**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="1d411-821">**Fatura** (71)</span><span class="sxs-lookup"><span data-stu-id="1d411-821">**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="1d411-822">**Razão** (72)</span><span class="sxs-lookup"><span data-stu-id="1d411-822">**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="1d411-823">**Quarto** (73)</span><span class="sxs-lookup"><span data-stu-id="1d411-823">**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-824">**PaperTypesAvailable**</span><span class="sxs-lookup"><span data-stu-id="1d411-824">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-825">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-825">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-826">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-826">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-827">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. RequiredPaperType", "CIM \_ reservice. PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtInputMediaName ")</span><span class="sxs-lookup"><span data-stu-id="1d411-827">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-828">Cadeias de caracteres de forma livre que especificam os tipos de papel disponíveis atualmente para a impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-828">Free-form strings that specify the types of paper that are currently available for the printer.</span></span> <span data-ttu-id="1d411-829">Cada cadeia de caracteres deve ser expressa no formulário especificado pelo DPA (aplicativo de impressão de documentos) ISO/IEC 10175, que também é resumido no Apêndice C do RFC 1759 (MIB de impressora).</span><span class="sxs-lookup"><span data-stu-id="1d411-829">Each string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span> <span data-ttu-id="1d411-830">Exemplos de cadeias de caracteres válidas são "ISO-A4-coloridas" e "na-10x14-envelope".</span><span class="sxs-lookup"><span data-stu-id="1d411-830">Examples of valid strings are "iso-a4-colored" and "na-10x14-envelope".</span></span> <span data-ttu-id="1d411-831">Por definição, um tamanho de papel que está disponível e listado na propriedade **PaperTypesAvailable** também deve aparecer na propriedade **PaperSizesSupported** .</span><span class="sxs-lookup"><span data-stu-id="1d411-831">By definition, a paper size that is available and listed in the **PaperTypesAvailable** property should also appear in the **PaperSizesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-832">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1d411-832">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-833">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-834">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-834">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-835">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d411-835">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-836">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d411-836">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="1d411-837">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-837">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1d411-838">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1d411-838">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="1d411-839">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1d411-839">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-840">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-840">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d411-841">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-841">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d411-842">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d411-842">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="1d411-843">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="1d411-843">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d411-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1d411-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1d411-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1d411-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-848">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1d411-848">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1d411-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-850">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="1d411-850">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1d411-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-852">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="1d411-852">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="1d411-853">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="1d411-853">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="1d411-854">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="1d411-854">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1d411-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-856">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="1d411-856">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1d411-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="1d411-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1d411-858">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="1d411-858">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-859">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1d411-859">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-860">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1d411-860">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-861">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-861">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d411-862">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="1d411-862">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="1d411-863">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="1d411-863">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="1d411-864">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="1d411-864">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="1d411-865">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="1d411-865">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="1d411-866">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-866">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-867">**PrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="1d411-867">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-868">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-868">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-869">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-869">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-870">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. hrPrinterStatus ")</span><span class="sxs-lookup"><span data-stu-id="1d411-870">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-871">Informações de status, além daquelas especificadas na propriedade de **disponibilidade** , para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-871">Status information, beyond that specified in the **Availability** property, for a printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-872">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-872">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-873">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-873">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="1d411-874">**Ocioso** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-874">**Idle** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="1d411-875">**Impressão** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-875">**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="1d411-876">**Aquecimento** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-876">**Warmup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="1d411-877">**Impressão interrompida** (6)</span><span class="sxs-lookup"><span data-stu-id="1d411-877">**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="1d411-878">**Offline** (7)</span><span class="sxs-lookup"><span data-stu-id="1d411-878">**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-879">**Status**</span><span class="sxs-lookup"><span data-stu-id="1d411-879">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-880">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-880">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-881">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-881">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-882">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="1d411-882">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-883">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1d411-883">Current status of the object.</span></span> <span data-ttu-id="1d411-884">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-884">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1d411-885">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1d411-885">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1d411-886">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1d411-886">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1d411-887">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="1d411-887">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1d411-888">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="1d411-888">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-889">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="1d411-889">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1d411-890">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1d411-890">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1d411-891">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="1d411-891">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1d411-892">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="1d411-892">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1d411-893">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="1d411-893">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1d411-894">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="1d411-894">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1d411-895">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="1d411-895">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1d411-896">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="1d411-896">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1d411-897">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="1d411-897">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-898">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1d411-898">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-899">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d411-899">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-900">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-900">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-901">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="1d411-901">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-902">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d411-902">State of the logical device.</span></span> <span data-ttu-id="1d411-903">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="1d411-903">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="1d411-904">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-904">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d411-905">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d411-905">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d411-906">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d411-906">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1d411-907">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="1d411-907">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1d411-908">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="1d411-908">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1d411-909">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="1d411-909">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d411-910">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d411-910">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-911">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-911">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-912">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-913">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d411-913">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d411-914">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="1d411-914">Scoping system's creation class name.</span></span>

<span data-ttu-id="1d411-915">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-915">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-916">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1d411-916">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-917">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d411-917">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-918">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-918">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-919">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d411-919">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d411-920">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="1d411-920">Scoping system's name.</span></span>

<span data-ttu-id="1d411-921">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-921">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d411-922">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="1d411-922">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-923">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d411-923">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-924">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-924">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d411-925">Hora da última redefinição de impressora.</span><span class="sxs-lookup"><span data-stu-id="1d411-925">Time of last printer reset.</span></span>

</dd> <dt>

<span data-ttu-id="1d411-926">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="1d411-926">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d411-927">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d411-927">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d411-928">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d411-928">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d411-929">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. HorizontalResolution"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels por polegada")</span><span class="sxs-lookup"><span data-stu-id="1d411-929">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="1d411-930">Resolução vertical em pixels por polegada.</span><span class="sxs-lookup"><span data-stu-id="1d411-930">Vertical resolution in pixels-per-inch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d411-931">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d411-931">Remarks</span></span>

<span data-ttu-id="1d411-932">A classe de **\_ impressora CIM** é derivada de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-932">The **CIM\_Printer** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1d411-933">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="1d411-933">WMI does not implement this class.</span></span> <span data-ttu-id="1d411-934">Para a classe WMI derivada da **\_ impressora CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1d411-934">For WMI classed derived from **CIM\_Printer**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1d411-935">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="1d411-935">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1d411-936">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="1d411-936">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d411-937">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d411-937">Requirements</span></span>



| <span data-ttu-id="1d411-938">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d411-938">Requirement</span></span> | <span data-ttu-id="1d411-939">Valor</span><span class="sxs-lookup"><span data-stu-id="1d411-939">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d411-940">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d411-940">Minimum supported client</span></span><br/> | <span data-ttu-id="1d411-941">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d411-941">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d411-942">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d411-942">Minimum supported server</span></span><br/> | <span data-ttu-id="1d411-943">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d411-943">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d411-944">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d411-944">Namespace</span></span><br/>                | <span data-ttu-id="1d411-945">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1d411-945">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d411-946">MOF</span><span class="sxs-lookup"><span data-stu-id="1d411-946">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d411-947"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d411-947"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d411-948">DLL</span><span class="sxs-lookup"><span data-stu-id="1d411-948">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d411-949"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d411-949"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d411-950">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d411-950">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d411-951">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1d411-951">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

