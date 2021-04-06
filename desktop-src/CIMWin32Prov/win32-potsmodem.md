---
description: A \_ classe WMI POTSModem do Win32 representa os serviços e as características de um modem de serviço de telefonia (POTS) simples em um sistema de computador executando o Windows.
ms.assetid: 24589942-e2c3-477e-8179-59ae4a4aa85a
ms.tgt_platform: multiple
title: Classe Win32_POTSModem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModem
- Win32_POTSModem.Reset
- Win32_POTSModem.SetPowerState
- Win32_POTSModem.AnswerMode
- Win32_POTSModem.AttachedTo
- Win32_POTSModem.Availability
- Win32_POTSModem.BlindOff
- Win32_POTSModem.BlindOn
- Win32_POTSModem.Caption
- Win32_POTSModem.CompatibilityFlags
- Win32_POTSModem.CompressionInfo
- Win32_POTSModem.CompressionOff
- Win32_POTSModem.CompressionOn
- Win32_POTSModem.ConfigManagerErrorCode
- Win32_POTSModem.ConfigManagerUserConfig
- Win32_POTSModem.ConfigurationDialog
- Win32_POTSModem.CountriesSupported
- Win32_POTSModem.CountrySelected
- Win32_POTSModem.CreationClassName
- Win32_POTSModem.CurrentPasswords
- Win32_POTSModem.DCB
- Win32_POTSModem.Default
- Win32_POTSModem.Description
- Win32_POTSModem.DeviceID
- Win32_POTSModem.DeviceLoader
- Win32_POTSModem.DeviceType
- Win32_POTSModem.DialType
- Win32_POTSModem.DriverDate
- Win32_POTSModem.ErrorCleared
- Win32_POTSModem.ErrorControlForced
- Win32_POTSModem.ErrorControlInfo
- Win32_POTSModem.ErrorControlOff
- Win32_POTSModem.ErrorControlOn
- Win32_POTSModem.ErrorDescription
- Win32_POTSModem.FlowControlHard
- Win32_POTSModem.FlowControlOff
- Win32_POTSModem.FlowControlSoft
- Win32_POTSModem.InactivityScale
- Win32_POTSModem.InactivityTimeout
- Win32_POTSModem.Index
- Win32_POTSModem.IndexEx
- Win32_POTSModem.InstallDate
- Win32_POTSModem.LastErrorCode
- Win32_POTSModem.MaxBaudRateToPhone
- Win32_POTSModem.MaxBaudRateToSerialPort
- Win32_POTSModem.MaxNumberOfPasswords
- Win32_POTSModem.Model
- Win32_POTSModem.ModemInfPath
- Win32_POTSModem.ModemInfSection
- Win32_POTSModem.ModulationBell
- Win32_POTSModem.ModulationCCITT
- Win32_POTSModem.ModulationScheme
- Win32_POTSModem.Name
- Win32_POTSModem.PNPDeviceID
- Win32_POTSModem.PortSubClass
- Win32_POTSModem.PowerManagementCapabilities
- Win32_POTSModem.PowerManagementSupported
- Win32_POTSModem.Prefix
- Win32_POTSModem.Properties
- Win32_POTSModem.ProviderName
- Win32_POTSModem.Pulse
- Win32_POTSModem.Reset
- Win32_POTSModem.ResponsesKeyName
- Win32_POTSModem.RingsBeforeAnswer
- Win32_POTSModem.SpeakerModeDial
- Win32_POTSModem.SpeakerModeOff
- Win32_POTSModem.SpeakerModeOn
- Win32_POTSModem.SpeakerModeSetup
- Win32_POTSModem.SpeakerVolumeHigh
- Win32_POTSModem.SpeakerVolumeInfo
- Win32_POTSModem.SpeakerVolumeLow
- Win32_POTSModem.SpeakerVolumeMed
- Win32_POTSModem.Status
- Win32_POTSModem.StatusInfo
- Win32_POTSModem.StringFormat
- Win32_POTSModem.SupportsCallback
- Win32_POTSModem.SupportsSynchronousConnect
- Win32_POTSModem.SystemCreationClassName
- Win32_POTSModem.SystemName
- Win32_POTSModem.Terminator
- Win32_POTSModem.TimeOfLastReset
- Win32_POTSModem.Tone
- Win32_POTSModem.VoiceSwitchFeature
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6ec9634c5ee86d6819bf8f7a45dd521276565903
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826421"
---
# <a name="win32_potsmodem-class"></a><span data-ttu-id="e228d-103">\_Classe Win32 POTSModem</span><span class="sxs-lookup"><span data-stu-id="e228d-103">Win32\_POTSModem class</span></span>

<span data-ttu-id="e228d-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ POTSModem do Win32** representa os serviços e as características de um modem de serviço de telefonia (POTS) simples em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="e228d-104">The **Win32\_POTSModem** [WMI class](../wmisdk/retrieving-a-class.md) represents the services and characteristics of a Plain Old Telephone Service (POTS) modem on a computer system running Windows.</span></span>

<span data-ttu-id="e228d-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e228d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e228d-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e228d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e228d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e228d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModem : CIM_PotsModem
{
  uint16   AnswerMode;
  string   AttachedTo;
  uint16   Availability;
  string   BlindOff;
  string   BlindOn;
  string   Caption;
  string   CompatibilityFlags;
  uint16   CompressionInfo;
  string   CompressionOff;
  string   CompressionOn;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   ConfigurationDialog;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  uint8    DCB[];
  uint8    Default[];
  string   Description;
  string   DeviceID;
  string   DeviceLoader;
  string   DeviceType;
  uint16   DialType;
  datetime DriverDate;
  boolean  ErrorCleared;
  string   ErrorControlForced;
  uint16   ErrorControlInfo;
  string   ErrorControlOff;
  string   ErrorControlOn;
  string   ErrorDescription;
  string   FlowControlHard;
  string   FlowControlOff;
  string   FlowControlSoft;
  string   InactivityScale;
  uint32   InactivityTimeout;
  uint32   Index;
  string   IndexEx;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  string   Model;
  string   ModemInfPath;
  string   ModemInfSection;
  string   ModulationBell;
  string   ModulationCCITT;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  string   PortSubClass;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Prefix;
  uint8    Properties[];
  string   ProviderName;
  string   Pulse;
  string   Reset;
  string   ResponsesKeyName;
  uint8    RingsBeforeAnswer;
  string   SpeakerModeDial;
  string   SpeakerModeOff;
  string   SpeakerModeOn;
  string   SpeakerModeSetup;
  string   SpeakerVolumeHigh;
  uint16   SpeakerVolumeInfo;
  string   SpeakerVolumeLow;
  string   SpeakerVolumeMed;
  string   Status;
  uint16   StatusInfo;
  string   StringFormat;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  string   Terminator;
  datetime TimeOfLastReset;
  string   Tone;
  string   VoiceSwitchFeature;
};
```

## <a name="members"></a><span data-ttu-id="e228d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e228d-108">Members</span></span>

<span data-ttu-id="e228d-109">A classe **Win32 \_ POTSModem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e228d-109">The **Win32\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="e228d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e228d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e228d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e228d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e228d-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e228d-112">Methods</span></span>

<span data-ttu-id="e228d-113">A classe **Win32 \_ POTSModem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e228d-113">The **Win32\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="e228d-114">Método</span><span class="sxs-lookup"><span data-stu-id="e228d-114">Method</span></span>            | <span data-ttu-id="e228d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e228d-115">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e228d-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="e228d-116">**Reset**</span></span>         | <span data-ttu-id="e228d-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="e228d-117">Not implemented.</span></span> <span data-ttu-id="e228d-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/>                 |
| <span data-ttu-id="e228d-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e228d-119">**SetPowerState**</span></span> | <span data-ttu-id="e228d-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="e228d-120">Not implemented.</span></span> <span data-ttu-id="e228d-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e228d-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e228d-122">Properties</span></span>

<span data-ttu-id="e228d-123">A classe **Win32 \_ POTSModem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e228d-123">The **Win32\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e228d-124">**Respondermode**</span><span class="sxs-lookup"><span data-stu-id="e228d-124">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e228d-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-127">Configuração de resposta automática ou de retorno de chamada atual para o modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-127">Current auto-answer or callback setting for the modem.</span></span>

<span data-ttu-id="e228d-128">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-128">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e228d-129">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e228d-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e228d-130">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e228d-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e228d-131">**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e228d-131">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="e228d-132">**Resposta manual** (3)</span><span class="sxs-lookup"><span data-stu-id="e228d-132">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="e228d-133">**Resposta automática** (4)</span><span class="sxs-lookup"><span data-stu-id="e228d-133">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="e228d-134">**Resposta automática com retorno de chamada** (5)</span><span class="sxs-lookup"><span data-stu-id="e228d-134">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-135">**AttachedTo**</span><span class="sxs-lookup"><span data-stu-id="e228d-135">**AttachedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-138">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \| anexada")</span><span class="sxs-lookup"><span data-stu-id="e228d-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|AttachedTo")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-139">Porta à qual o modem POTS está anexado.</span><span class="sxs-lookup"><span data-stu-id="e228d-139">Port to which the POTS modem is attached.</span></span>

<span data-ttu-id="e228d-140">Exemplo: "COM1"</span><span class="sxs-lookup"><span data-stu-id="e228d-140">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-141">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="e228d-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-142">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e228d-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-144">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="e228d-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-145">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e228d-145">Availability and status of the device.</span></span>

<span data-ttu-id="e228d-146">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e228d-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e228d-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e228d-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="e228d-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e228d-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="e228d-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-150">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="e228d-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e228d-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="e228d-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e228d-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="e228d-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e228d-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="e228d-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e228d-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="e228d-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e228d-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="e228d-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e228d-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="e228d-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e228d-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="e228d-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e228d-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="e228d-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e228d-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="e228d-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e228d-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="e228d-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-161">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e228d-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e228d-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="e228d-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-163">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="e228d-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e228d-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="e228d-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-165">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="e228d-165">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e228d-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="e228d-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e228d-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="e228d-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-168">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="e228d-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e228d-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="e228d-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-170">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="e228d-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e228d-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="e228d-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-172">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="e228d-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e228d-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="e228d-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-174">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="e228d-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e228d-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="e228d-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-176">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="e228d-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-177">**BlindOff**</span><span class="sxs-lookup"><span data-stu-id="e228d-177">**BlindOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-180">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| BlindOff")</span><span class="sxs-lookup"><span data-stu-id="e228d-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOff")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-181">Cadeia de caracteres de comando usada para detectar um tom de discagem antes de discar.</span><span class="sxs-lookup"><span data-stu-id="e228d-181">Command string used to detect a dial tone before dialing.</span></span>

<span data-ttu-id="e228d-182">Exemplo: "x4"</span><span class="sxs-lookup"><span data-stu-id="e228d-182">Example: "X4"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-183">**Cegueira**</span><span class="sxs-lookup"><span data-stu-id="e228d-183">**BlindOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-186">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| de \\ \\ classe de controle CurrentControlSet do sistema \\ \\ \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="e228d-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOn")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-187">Cadeia de caracteres de comando usada para discar se há ou não um tom de discagem.</span><span class="sxs-lookup"><span data-stu-id="e228d-187">Command string used to dial whether or not there is a dial tone.</span></span>

<span data-ttu-id="e228d-188">Exemplo: "x3"</span><span class="sxs-lookup"><span data-stu-id="e228d-188">Example: "X3"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-189">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e228d-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-192">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e228d-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-193">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e228d-193">Short description of the object.</span></span>

<span data-ttu-id="e228d-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-195">**CompatibilityFlags**</span><span class="sxs-lookup"><span data-stu-id="e228d-195">**CompatibilityFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-198">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| CompatibilityFlags")</span><span class="sxs-lookup"><span data-stu-id="e228d-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|CompatibilityFlags")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-199">Todos os protocolos de conexão de modem com os quais este dispositivo de modem é compatível.</span><span class="sxs-lookup"><span data-stu-id="e228d-199">All modem connection protocols with which this modem device is compatible.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-200">**CompressionInfo**</span><span class="sxs-lookup"><span data-stu-id="e228d-200">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-201">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e228d-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-203">Características de compactação de dados do modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-203">Data compression characteristics of the modem.</span></span>

<span data-ttu-id="e228d-204">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-204">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e228d-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e228d-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e228d-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e228d-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-207">Unknown</span><span class="sxs-lookup"><span data-stu-id="e228d-207">Unknown</span></span>

</dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="e228d-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**Sem compactação** (2)</span><span class="sxs-lookup"><span data-stu-id="e228d-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**No Compression** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-209">Outro</span><span class="sxs-lookup"><span data-stu-id="e228d-209">Other</span></span>

</dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="e228d-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="e228d-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-211">Sem compactação</span><span class="sxs-lookup"><span data-stu-id="e228d-211">No Compression</span></span>

</dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="e228d-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="e228d-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V.42bis** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-213">MNP5 5</span><span class="sxs-lookup"><span data-stu-id="e228d-213">MNP 5</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="e228d-214"><span id="5"></span>**05**</span><span class="sxs-lookup"><span data-stu-id="e228d-214"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="e228d-215">V. 42bis</span><span class="sxs-lookup"><span data-stu-id="e228d-215">V.42bis</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-216">**CompressionOff**</span><span class="sxs-lookup"><span data-stu-id="e228d-216">**CompressionOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-219">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ \\ \\ compactação de classe de controle \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="e228d-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-220">Cadeia de caracteres de comando usada para desabilitar a compactação de dados de hardware.</span><span class="sxs-lookup"><span data-stu-id="e228d-220">Command string used to disable hardware data compression.</span></span>

<span data-ttu-id="e228d-221">Exemplo: "S46 = 136"</span><span class="sxs-lookup"><span data-stu-id="e228d-221">Example: "S46=136"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-222">**Compactação**</span><span class="sxs-lookup"><span data-stu-id="e228d-222">**CompressionOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-223">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-225">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ \\ \\ \| compactação \_ de classe de controle")</span><span class="sxs-lookup"><span data-stu-id="e228d-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_On")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-226">Cadeia de caracteres de comando usada para habilitar a compactação de dados de hardware.</span><span class="sxs-lookup"><span data-stu-id="e228d-226">Command string used to enable hardware data compression.</span></span>

<span data-ttu-id="e228d-227">Exemplo: "S46 = 138"</span><span class="sxs-lookup"><span data-stu-id="e228d-227">Example: "S46=138"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-228">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e228d-228">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-229">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e228d-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-231">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e228d-231">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-232">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e228d-232">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="e228d-233">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-233">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e228d-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="e228d-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e228d-235"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="e228d-235">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-236">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="e228d-236">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e228d-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="e228d-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e228d-238">(1)</span><span class="sxs-lookup"><span data-stu-id="e228d-238">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-239">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="e228d-239">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e228d-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e228d-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e228d-241">(2)</span><span class="sxs-lookup"><span data-stu-id="e228d-241">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e228d-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="e228d-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e228d-243">(3)</span><span class="sxs-lookup"><span data-stu-id="e228d-243">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-244">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="e228d-244">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e228d-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="e228d-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e228d-246">(4)</span><span class="sxs-lookup"><span data-stu-id="e228d-246">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-247">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="e228d-247">Device is not working properly.</span></span> <span data-ttu-id="e228d-248">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="e228d-248">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e228d-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="e228d-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e228d-250">(5)</span><span class="sxs-lookup"><span data-stu-id="e228d-250">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-251">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="e228d-251">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e228d-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="e228d-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e228d-253"> (6)</span><span class="sxs-lookup"><span data-stu-id="e228d-253">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-254">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e228d-254">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e228d-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="e228d-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e228d-256">(7)</span><span class="sxs-lookup"><span data-stu-id="e228d-256">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e228d-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="e228d-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e228d-258">(8)</span><span class="sxs-lookup"><span data-stu-id="e228d-258">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-259">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="e228d-259">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e228d-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="e228d-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e228d-261">(9)</span><span class="sxs-lookup"><span data-stu-id="e228d-261">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-262">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="e228d-262">Device is not working properly.</span></span> <span data-ttu-id="e228d-263">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e228d-263">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e228d-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="e228d-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e228d-265">(10)</span><span class="sxs-lookup"><span data-stu-id="e228d-265">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-266">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e228d-266">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e228d-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="e228d-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e228d-268">(11)</span><span class="sxs-lookup"><span data-stu-id="e228d-268">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-269">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e228d-269">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e228d-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="e228d-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e228d-271">12</span><span class="sxs-lookup"><span data-stu-id="e228d-271">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-272">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="e228d-272">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e228d-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e228d-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e228d-274">(13)</span><span class="sxs-lookup"><span data-stu-id="e228d-274">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-275">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e228d-275">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e228d-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="e228d-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e228d-277">(14)</span><span class="sxs-lookup"><span data-stu-id="e228d-277">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-278">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="e228d-278">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e228d-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="e228d-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e228d-280">(15)</span><span class="sxs-lookup"><span data-stu-id="e228d-280">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-281">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="e228d-281">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e228d-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="e228d-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e228d-283">(16)</span><span class="sxs-lookup"><span data-stu-id="e228d-283">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-284">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="e228d-284">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e228d-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="e228d-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e228d-286">(17)</span><span class="sxs-lookup"><span data-stu-id="e228d-286">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-287">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e228d-287">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e228d-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e228d-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e228d-289">(18)</span><span class="sxs-lookup"><span data-stu-id="e228d-289">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-290">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="e228d-290">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e228d-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="e228d-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e228d-292">(19)</span><span class="sxs-lookup"><span data-stu-id="e228d-292">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e228d-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="e228d-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e228d-294">(20)</span><span class="sxs-lookup"><span data-stu-id="e228d-294">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-295">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="e228d-295">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e228d-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e228d-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e228d-297">(21)</span><span class="sxs-lookup"><span data-stu-id="e228d-297">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-298">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="e228d-298">System failure.</span></span> <span data-ttu-id="e228d-299">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="e228d-299">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e228d-300">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e228d-300">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e228d-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="e228d-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e228d-302">(22)</span><span class="sxs-lookup"><span data-stu-id="e228d-302">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-303">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e228d-303">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e228d-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="e228d-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e228d-305">(23)</span><span class="sxs-lookup"><span data-stu-id="e228d-305">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-306">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="e228d-306">System failure.</span></span> <span data-ttu-id="e228d-307">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="e228d-307">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e228d-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="e228d-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e228d-309">(24)</span><span class="sxs-lookup"><span data-stu-id="e228d-309">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-310">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="e228d-310">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e228d-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e228d-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e228d-312">(25)</span><span class="sxs-lookup"><span data-stu-id="e228d-312">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-313">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e228d-313">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e228d-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e228d-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e228d-315">(26)</span><span class="sxs-lookup"><span data-stu-id="e228d-315">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-316">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e228d-316">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e228d-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="e228d-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e228d-318">(27)</span><span class="sxs-lookup"><span data-stu-id="e228d-318">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-319">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="e228d-319">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e228d-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="e228d-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e228d-321">(28)</span><span class="sxs-lookup"><span data-stu-id="e228d-321">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-322">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="e228d-322">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e228d-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="e228d-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e228d-324">(29)</span><span class="sxs-lookup"><span data-stu-id="e228d-324">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-325">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e228d-325">Device is disabled.</span></span> <span data-ttu-id="e228d-326">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="e228d-326">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e228d-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="e228d-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e228d-328">(30)</span><span class="sxs-lookup"><span data-stu-id="e228d-328">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-329">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="e228d-329">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e228d-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e228d-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e228d-331">(31)</span><span class="sxs-lookup"><span data-stu-id="e228d-331">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-332">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="e228d-332">Device is not working properly.</span></span> <span data-ttu-id="e228d-333">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="e228d-333">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-334">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="e228d-334">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-335">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e228d-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-337">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e228d-337">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-338">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e228d-338">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e228d-339">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-340">**ConfigurationDialog**</span><span class="sxs-lookup"><span data-stu-id="e228d-340">**ConfigurationDialog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-341">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-343">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ConfigDialog")</span><span class="sxs-lookup"><span data-stu-id="e228d-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ConfigDialog")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-344">Cadeia de inicialização do modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-344">Modem initialization string.</span></span> <span data-ttu-id="e228d-345">Essa propriedade é composta por cadeias de caracteres de comando de outras propriedades dessa classe.</span><span class="sxs-lookup"><span data-stu-id="e228d-345">This property is made up of command strings from other properties of this class.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-346">**CountriesSupported**</span><span class="sxs-lookup"><span data-stu-id="e228d-346">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-347">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-347">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e228d-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-349">Matriz de países/regiões em que o modem pode operar.</span><span class="sxs-lookup"><span data-stu-id="e228d-349">Array of countries/regions in which the modem can operate.</span></span>

<span data-ttu-id="e228d-350">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-350">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-351">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="e228d-351">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-354">País/região para o qual o modem está programado no momento.</span><span class="sxs-lookup"><span data-stu-id="e228d-354">Country/region for which the modem is currently programmed.</span></span> <span data-ttu-id="e228d-355">Quando há suporte para vários países/regiões, essa propriedade define qual deles está selecionado atualmente para uso.</span><span class="sxs-lookup"><span data-stu-id="e228d-355">When multiple countries/regions are supported, this property defines which one is currently selected for use.</span></span>

<span data-ttu-id="e228d-356">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-356">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-357">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e228d-357">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-358">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-360">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e228d-360">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e228d-361">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="e228d-361">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="e228d-362">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="e228d-362">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e228d-363">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-364">**CurrentPasswords**</span><span class="sxs-lookup"><span data-stu-id="e228d-364">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-365">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-365">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e228d-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-367">Lista de senhas definidas no momento para o modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-367">List of currently defined passwords for the modem.</span></span> <span data-ttu-id="e228d-368">Essa matriz pode ser deixada em branco por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="e228d-368">This array may be left blank for security reasons.</span></span>

<span data-ttu-id="e228d-369">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-369">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-370">**DCB**</span><span class="sxs-lookup"><span data-stu-id="e228d-370">**DCB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-371">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="e228d-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e228d-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-373">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span><span class="sxs-lookup"><span data-stu-id="e228d-373">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-374">Configurações de controle para um dispositivo de comunicações serial, nesse caso, o dispositivo de modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-374">Control settings for a serial communications device, in this case, the modem device.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-375">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="e228d-375">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-376">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="e228d-376">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e228d-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-378">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ controle de \\ \\ classe \| padrão")</span><span class="sxs-lookup"><span data-stu-id="e228d-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Default")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-379">Se for **true**, esse modem POTS será o modem padrão no sistema de computador que executa o Windows.</span><span class="sxs-lookup"><span data-stu-id="e228d-379">If **TRUE**, this POTS modem is the default modem on the computer system running Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-380">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e228d-380">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-383">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="e228d-383">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-384">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e228d-384">Description of the object.</span></span>

<span data-ttu-id="e228d-385">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-386">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e228d-386">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-387">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-389">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="e228d-389">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-390">Identificador exclusivo deste modem POTS de outros dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="e228d-390">Unique identifier of this POTS modem from other devices on the system.</span></span>

<span data-ttu-id="e228d-391">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-392">**DeviceLoader**</span><span class="sxs-lookup"><span data-stu-id="e228d-392">**DeviceLoader**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-393">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-395">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ classe \| DevLoader")</span><span class="sxs-lookup"><span data-stu-id="e228d-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DevLoader")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-396">Nome do carregador de dispositivo para o modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-396">Name of the device loader for the modem.</span></span> <span data-ttu-id="e228d-397">Um carregador de dispositivo carrega e gerencia drivers de dispositivo e enumeradores para um determinado dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e228d-397">A device loader loads and manages device drivers and enumerators for a given device.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-398">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="e228d-398">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-399">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-401">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ controle de classe do \\ \\ \| dispositivo")</span><span class="sxs-lookup"><span data-stu-id="e228d-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DeviceType")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-402">Tipo físico do modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-402">Physical type of the modem.</span></span>

<span data-ttu-id="e228d-403">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="e228d-403">The values are:</span></span>

<dl> <dd><span data-ttu-id="e228d-404">"Modem nulo"</span><span class="sxs-lookup"><span data-stu-id="e228d-404">"Null Modem"</span></span></dd> <dd><span data-ttu-id="e228d-405">"Modem interno"</span><span class="sxs-lookup"><span data-stu-id="e228d-405">"Internal Modem"</span></span></dd> <dd><span data-ttu-id="e228d-406">"Modem externo"</span><span class="sxs-lookup"><span data-stu-id="e228d-406">"External Modem"</span></span></dd> <dd><span data-ttu-id="e228d-407">"Modem PCMCIA"</span><span class="sxs-lookup"><span data-stu-id="e228d-407">"PCMCIA Modem"</span></span></dd> <dd><span data-ttu-id="e228d-408">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="e228d-408">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Null_Modem"></span><span id="null_modem"></span><span id="NULL_MODEM"></span>

<span data-ttu-id="e228d-409">**Modem nulo** ("modem nulo")</span><span class="sxs-lookup"><span data-stu-id="e228d-409">**Null Modem** ("Null Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Modem"></span><span id="internal_modem"></span><span id="INTERNAL_MODEM"></span>

<span data-ttu-id="e228d-410">**Modem interno** ("modem interno")</span><span class="sxs-lookup"><span data-stu-id="e228d-410">**Internal Modem** ("Internal Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="External_Modem"></span><span id="external_modem"></span><span id="EXTERNAL_MODEM"></span>

<span data-ttu-id="e228d-411">**Modem externo** ("modem externo")</span><span class="sxs-lookup"><span data-stu-id="e228d-411">**External Modem** ("External Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Modem"></span><span id="pcmcia_modem"></span><span id="PCMCIA_MODEM"></span>

<span data-ttu-id="e228d-412">**Modem PCMCIA** ("PCMCIA modem")</span><span class="sxs-lookup"><span data-stu-id="e228d-412">**PCMCIA Modem** ("PCMCIA Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e228d-413">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e228d-413">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-414">**Dialtype**</span><span class="sxs-lookup"><span data-stu-id="e228d-414">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-415">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e228d-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-417">Tipo de método de discagem usado.</span><span class="sxs-lookup"><span data-stu-id="e228d-417">Type of dialing method used.</span></span>

<span data-ttu-id="e228d-418">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-418">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e228d-419">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e228d-419">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="e228d-420">**Tom** (1)</span><span class="sxs-lookup"><span data-stu-id="e228d-420">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="e228d-421">**Pulse** (2)</span><span class="sxs-lookup"><span data-stu-id="e228d-421">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-422">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="e228d-422">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-423">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e228d-423">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-424">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-425">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="e228d-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-426">Data do driver do modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-426">Date of the modem driver.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-427">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e228d-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-428">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e228d-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-430">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="e228d-430">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="e228d-431">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-432">**ErrorControlForced**</span><span class="sxs-lookup"><span data-stu-id="e228d-432">**ErrorControlForced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-433">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-435">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \| ErrorControl \_ forçada")</span><span class="sxs-lookup"><span data-stu-id="e228d-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Forced")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-436">Cadeia de caracteres de comando usada para habilitar o controle de correção de erros ao estabelecer uma conexão.</span><span class="sxs-lookup"><span data-stu-id="e228d-436">Command string used to enable error correction control when establishing a connection.</span></span> <span data-ttu-id="e228d-437">Isso aumenta a confiabilidade da conexão.</span><span class="sxs-lookup"><span data-stu-id="e228d-437">This increases the reliability of the connection.</span></span>

<span data-ttu-id="e228d-438">Exemplo: "+ Q5S36 = 4S48 = 7"</span><span class="sxs-lookup"><span data-stu-id="e228d-438">Example: "+Q5S36=4S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-439">**ErrorControlInfo**</span><span class="sxs-lookup"><span data-stu-id="e228d-439">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-440">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e228d-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-442">Características de correção de erro do modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-442">Error correction characteristics of the modem.</span></span>

<span data-ttu-id="e228d-443">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-443">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e228d-444">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e228d-444">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e228d-445">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e228d-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="e228d-446">**Sem correção de erro** (2)</span><span class="sxs-lookup"><span data-stu-id="e228d-446">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="e228d-447">**MNP5 4** (3)</span><span class="sxs-lookup"><span data-stu-id="e228d-447">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="e228d-448">**LAPM** (4)</span><span class="sxs-lookup"><span data-stu-id="e228d-448">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-449">**ErrorControlOff**</span><span class="sxs-lookup"><span data-stu-id="e228d-449">**ErrorControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-450">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-452">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ off")</span><span class="sxs-lookup"><span data-stu-id="e228d-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-453">Cadeia de caracteres de comando usada para desabilitar o controle de erro.</span><span class="sxs-lookup"><span data-stu-id="e228d-453">Command string used to disable error control.</span></span>

<span data-ttu-id="e228d-454">Exemplo: "+ Q6S36 = 3S48 = 128"</span><span class="sxs-lookup"><span data-stu-id="e228d-454">Example: "+Q6S36=3S48=128"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-455">**ErrorControlOn**</span><span class="sxs-lookup"><span data-stu-id="e228d-455">**ErrorControlOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-456">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-457">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-458">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ on")</span><span class="sxs-lookup"><span data-stu-id="e228d-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_On")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-459">Cadeia de caracteres de comando usada para habilitar o controle de erro.</span><span class="sxs-lookup"><span data-stu-id="e228d-459">Command string used to enable error control.</span></span>

<span data-ttu-id="e228d-460">Exemplo: "+ Q5S36 = 7S48 = 7"</span><span class="sxs-lookup"><span data-stu-id="e228d-460">Example: "+Q5S36=7S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-461">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e228d-461">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-462">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-463">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-464">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="e228d-464">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="e228d-465">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-465">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-466">**FlowControlHard**</span><span class="sxs-lookup"><span data-stu-id="e228d-466">**FlowControlHard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-467">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-468">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-469">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \| FlowControl \_ Hard")</span><span class="sxs-lookup"><span data-stu-id="e228d-469">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Hard")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-470">Cadeia de caracteres de comando usada para habilitar o controle de fluxo de hardware.</span><span class="sxs-lookup"><span data-stu-id="e228d-470">Command string used to enable hardware flow control.</span></span> <span data-ttu-id="e228d-471">O controle de fluxo consiste em sinais enviados entre computadores que verificam se ambos os computadores estão prontos para transmitir ou receber dados.</span><span class="sxs-lookup"><span data-stu-id="e228d-471">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="e228d-472">Exemplo: "&K1"</span><span class="sxs-lookup"><span data-stu-id="e228d-472">Example: "&K1"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-473">**FlowControlOff**</span><span class="sxs-lookup"><span data-stu-id="e228d-473">**FlowControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-474">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-476">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ off")</span><span class="sxs-lookup"><span data-stu-id="e228d-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-477">Cadeia de caracteres de comando usada para desabilitar o controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e228d-477">Command string used to disable flow control.</span></span> <span data-ttu-id="e228d-478">O controle de fluxo consiste em sinais enviados entre computadores que verificam se ambos os computadores estão prontos para transmitir ou receber dados.</span><span class="sxs-lookup"><span data-stu-id="e228d-478">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="e228d-479">Exemplo: "&K0"</span><span class="sxs-lookup"><span data-stu-id="e228d-479">Example: "&K0"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-480">**FlowControlSoft**</span><span class="sxs-lookup"><span data-stu-id="e228d-480">**FlowControlSoft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-481">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-482">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-483">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ soft")</span><span class="sxs-lookup"><span data-stu-id="e228d-483">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Soft")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-484">Cadeia de caracteres de comando usada para habilitar o controle de fluxo de software.</span><span class="sxs-lookup"><span data-stu-id="e228d-484">Command string used to enable software flow control.</span></span> <span data-ttu-id="e228d-485">O controle de fluxo consiste em sinais enviados entre computadores que verificam se ambos os computadores estão prontos para transmitir ou receber dados.</span><span class="sxs-lookup"><span data-stu-id="e228d-485">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="e228d-486">Exemplo: "&K2"</span><span class="sxs-lookup"><span data-stu-id="e228d-486">Example: "&K2"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-487">**InactivityScale**</span><span class="sxs-lookup"><span data-stu-id="e228d-487">**InactivityScale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-488">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-488">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-489">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-490">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InactivityScale")</span><span class="sxs-lookup"><span data-stu-id="e228d-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InactivityScale")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-491">Multiplicador usado com a propriedade **InactivityTimeout** para calcular o período de tempo limite de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="e228d-491">Multiplier used with the **InactivityTimeout** property to calculate the timeout period of a connection.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-492">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="e228d-492">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-493">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e228d-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-494">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-495">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="e228d-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-496">Limite de tempo (em segundos) para a desconexão automática da linha telefônica, se nenhum dado for trocado.</span><span class="sxs-lookup"><span data-stu-id="e228d-496">Time limit (in seconds) for automatic disconnection of the phone line, if no data is exchanged.</span></span> <span data-ttu-id="e228d-497">Um valor de 0 (zero) indica que esse recurso está presente, mas não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e228d-497">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

<span data-ttu-id="e228d-498">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-498">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-499">**Index**</span><span class="sxs-lookup"><span data-stu-id="e228d-499">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-500">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e228d-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-501">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-502">Número de índice deste modem POTS.</span><span class="sxs-lookup"><span data-stu-id="e228d-502">Index number for this POTS modem.</span></span>

<span data-ttu-id="e228d-503">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="e228d-503">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="e228d-504">**IndexEx**</span><span class="sxs-lookup"><span data-stu-id="e228d-504">**IndexEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-505">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-506">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-507">A ID da instância do dispositivo para este modem POTS.</span><span class="sxs-lookup"><span data-stu-id="e228d-507">The device instance ID for this POTS modem.</span></span>

<span data-ttu-id="e228d-508">Exemplo: "1&08"</span><span class="sxs-lookup"><span data-stu-id="e228d-508">Example: "1&08"</span></span>

<span data-ttu-id="e228d-509">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Essa propriedade está disponível a partir do Windows Server 2016 e do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e228d-509">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is available beginning with Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e228d-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-511">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e228d-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-512">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-513">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="e228d-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-514">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="e228d-514">Date and time the object was installed.</span></span> <span data-ttu-id="e228d-515">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="e228d-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e228d-516">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-517">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e228d-517">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-518">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e228d-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-520">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e228d-520">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e228d-521">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-522">**MaxBaudRateToPhone**</span><span class="sxs-lookup"><span data-stu-id="e228d-522">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-523">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e228d-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-524">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-525">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="e228d-525">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-526">Velocidade máxima de comunicação configurável para acessar o sistema telefônico.</span><span class="sxs-lookup"><span data-stu-id="e228d-526">Maximum settable communication speed for accessing the phone system.</span></span>

<span data-ttu-id="e228d-527">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-527">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-528">**MaxBaudRateToSerialPort**</span><span class="sxs-lookup"><span data-stu-id="e228d-528">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-529">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e228d-529">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-530">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-531">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="e228d-531">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-532">Velocidade máxima de comunicação configurável para a porta COM para um modem externo.</span><span class="sxs-lookup"><span data-stu-id="e228d-532">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="e228d-533">Digite 0 (zero) se não for aplicável.</span><span class="sxs-lookup"><span data-stu-id="e228d-533">Enter 0 (zero) if not applicable.</span></span>

<span data-ttu-id="e228d-534">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-534">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-535">**MaxNumberOfPasswords**</span><span class="sxs-lookup"><span data-stu-id="e228d-535">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-536">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e228d-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-537">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-538">Número de senhas definíveis no próprio modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-538">Number of passwords definable in the modem itself.</span></span> <span data-ttu-id="e228d-539">Se não houver suporte para esse recurso, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e228d-539">If this feature is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="e228d-540">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-540">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-541">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="e228d-541">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-542">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-543">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-544">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| modelo de classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="e228d-544">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Model")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-545">Modelo desse modem POTS.</span><span class="sxs-lookup"><span data-stu-id="e228d-545">Model of this POTS modem.</span></span>

<span data-ttu-id="e228d-546">Exemplo: "Sportster 56K external"</span><span class="sxs-lookup"><span data-stu-id="e228d-546">Example: "Sportster 56K External"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-547">**ModemInfPath**</span><span class="sxs-lookup"><span data-stu-id="e228d-547">**ModemInfPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-548">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-549">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-550">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="e228d-550">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-551">Caminho para o arquivo. inf desse modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-551">Path to this modem's .inf file.</span></span> <span data-ttu-id="e228d-552">Esse arquivo contém informações de inicialização para o modem e seu driver.</span><span class="sxs-lookup"><span data-stu-id="e228d-552">This file contains initialization information for the modem and its driver.</span></span>

<span data-ttu-id="e228d-553">Exemplo: "C: \\ Windows \\ inf"</span><span class="sxs-lookup"><span data-stu-id="e228d-553">Example: "C:\\Windows\\INF"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-554">**ModemInfSection**</span><span class="sxs-lookup"><span data-stu-id="e228d-554">**ModemInfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-555">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-555">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-556">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-556">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-557">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="e228d-557">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-558">Nome da seção no arquivo. inf do modem que contém informações sobre o modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-558">Name of the section in the modem's .inf file that contains information about the modem.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-559">**ModulationBell**</span><span class="sxs-lookup"><span data-stu-id="e228d-559">**ModulationBell**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-560">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-561">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-562">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet de \\ \\ \\ \\ modulação de classe de controle \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="e228d-562">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_Bell")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-563">Cadeia de caracteres de comando usada para instruir o modem a usar modulações Bell para 300 e 1200 bps.</span><span class="sxs-lookup"><span data-stu-id="e228d-563">Command string used to instruct the modem to use Bell modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="e228d-564">Exemplo: "B1"</span><span class="sxs-lookup"><span data-stu-id="e228d-564">Example: "B1"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-565">**ModulationCCITT**</span><span class="sxs-lookup"><span data-stu-id="e228d-565">**ModulationCCITT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-566">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-567">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-568">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ \\ \\ modulação de classe de controle \| \_ CCITT")</span><span class="sxs-lookup"><span data-stu-id="e228d-568">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_CCITT")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-569">Cadeia de caracteres de comando usada para instruir o modem a usar modulações CCITT para 300 e 1200 bps.</span><span class="sxs-lookup"><span data-stu-id="e228d-569">Command string used to instruct the modem to use CCITT modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="e228d-570">Exemplo: "B0"</span><span class="sxs-lookup"><span data-stu-id="e228d-570">Example: "B0"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-571">**ModulationScheme**</span><span class="sxs-lookup"><span data-stu-id="e228d-571">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-572">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e228d-572">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-573">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-574">Esquema de modulação do modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-574">Modulation scheme of the modem.</span></span>

<span data-ttu-id="e228d-575">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-575">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e228d-576">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e228d-576">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e228d-577">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e228d-577">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e228d-578">**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="e228d-578">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="e228d-579">**Bell 103** (3)</span><span class="sxs-lookup"><span data-stu-id="e228d-579">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="e228d-580">**Bell 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="e228d-580">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="e228d-581">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="e228d-581">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="e228d-582">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="e228d-582">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="e228d-583">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="e228d-583">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="e228d-584">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="e228d-584">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="e228d-585">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="e228d-585">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="e228d-586">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="e228d-586">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="e228d-587">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="e228d-587">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-588">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e228d-588">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-589">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-590">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-591">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e228d-591">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-592">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="e228d-592">Label by which the object is known.</span></span> <span data-ttu-id="e228d-593">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="e228d-593">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="e228d-594">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-594">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-595">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e228d-595">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-596">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-596">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-597">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-597">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-598">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e228d-598">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-599">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e228d-599">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="e228d-600">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-600">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e228d-601">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e228d-601">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-602">**PortSubClass**</span><span class="sxs-lookup"><span data-stu-id="e228d-602">**PortSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-603">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-604">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-604">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-605">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ classe \| PortSubClass"), **valor** ("porta paralela", "porta serial", "modem")</span><span class="sxs-lookup"><span data-stu-id="e228d-605">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|PortSubClass"), **Value** ("Parallel Port", "Serial Port", "Modem")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-606">Definição da porta usada para este modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-606">Definition of the port used for this modem.</span></span>

<dt>



 <span data-ttu-id="e228d-607">("00")</span><span class="sxs-lookup"><span data-stu-id="e228d-607">("00")</span></span>


</dt> <dd>

<span data-ttu-id="e228d-608">Porta Paralela</span><span class="sxs-lookup"><span data-stu-id="e228d-608">Parallel Port</span></span>

</dd> <dt>



 <span data-ttu-id="e228d-609">("01")</span><span class="sxs-lookup"><span data-stu-id="e228d-609">("01")</span></span>


</dt> <dd>

<span data-ttu-id="e228d-610">Porta serial</span><span class="sxs-lookup"><span data-stu-id="e228d-610">Serial Port</span></span>

</dd> <dt>



 <span data-ttu-id="e228d-611">("02")</span><span class="sxs-lookup"><span data-stu-id="e228d-611">("02")</span></span>


</dt> <dd>

<span data-ttu-id="e228d-612">Modem</span><span class="sxs-lookup"><span data-stu-id="e228d-612">Modem</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-613">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e228d-613">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-614">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e228d-614">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e228d-615">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-615">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-616">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e228d-616">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e228d-617">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="e228d-617">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e228d-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e228d-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e228d-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="e228d-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e228d-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e228d-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e228d-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e228d-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-622">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e228d-622">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e228d-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="e228d-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-624">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="e228d-624">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e228d-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="e228d-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-626">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="e228d-626">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e228d-627">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="e228d-627">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e228d-628">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-628">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e228d-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="e228d-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-630">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="e228d-630">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e228d-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="e228d-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e228d-632">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="e228d-632">Timed Power-On Supported</span></span>

<span data-ttu-id="e228d-633">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="e228d-633">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-634">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e228d-634">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-635">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e228d-635">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-636">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-636">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-637">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="e228d-637">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="e228d-638">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="e228d-638">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="e228d-639">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-640">**Prefix**</span><span class="sxs-lookup"><span data-stu-id="e228d-640">**Prefix**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-641">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-642">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-643">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| prefixo de classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="e228d-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Prefix")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-644">Prefixo de discagem usado para acessar uma linha externa.</span><span class="sxs-lookup"><span data-stu-id="e228d-644">Dialing prefix used to access an outside line.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-645">**Propriedades**</span><span class="sxs-lookup"><span data-stu-id="e228d-645">**Properties**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-646">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="e228d-646">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e228d-647">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-648">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Propriedades da classe de controle \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="e228d-648">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Properties")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-649">Lista de todas as propriedades (e seus valores) para este modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-649">List of all the properties (and their values) for this modem.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-650">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="e228d-650">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-651">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-652">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-653">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="e228d-653">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ProviderName")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-654">Caminho de rede para o computador que fornece os serviços de modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-654">Network path to the computer that provides the modem services.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-655">**Pulso**</span><span class="sxs-lookup"><span data-stu-id="e228d-655">**Pulse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-656">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-656">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-657">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-657">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-658">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| de \\ \\ classe de controle CurrentControlSet do sistema \\ \\ \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="e228d-658">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Pulse")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-659">Cadeia de caracteres de comando usada para instruir o modem a usar o modo de pulso para discagem.</span><span class="sxs-lookup"><span data-stu-id="e228d-659">Command string used to instruct the modem to use pulse mode for dialing.</span></span> <span data-ttu-id="e228d-660">A discagem de pulso é necessária para linhas telefônicas que não podem lidar com a discagem de Tom.</span><span class="sxs-lookup"><span data-stu-id="e228d-660">Pulse dialing is necessary for phone lines that are unable to handle tone dialing.</span></span>

<span data-ttu-id="e228d-661">Exemplo: "P"</span><span class="sxs-lookup"><span data-stu-id="e228d-661">Example: "P"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-662">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="e228d-662">**Reset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-663">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-663">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-664">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-664">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-665">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) (redefine), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| redefine")</span><span class="sxs-lookup"><span data-stu-id="e228d-665">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Reset), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Reset")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-666">Cadeia de caracteres de comando usada para redefinir o modem para a próxima chamada.</span><span class="sxs-lookup"><span data-stu-id="e228d-666">Command string used to reset the modem for the next call.</span></span>

<span data-ttu-id="e228d-667">Exemplo: "às&F"</span><span class="sxs-lookup"><span data-stu-id="e228d-667">Example: "AT&F"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-668">**ResponsesKeyName**</span><span class="sxs-lookup"><span data-stu-id="e228d-668">**ResponsesKeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-669">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-669">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-670">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-670">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-671">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ResponsesKeyName")</span><span class="sxs-lookup"><span data-stu-id="e228d-671">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ResponsesKeyName")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-672">Resposta esse modem pode relatar ao sistema operacional durante o processo de conexão.</span><span class="sxs-lookup"><span data-stu-id="e228d-672">Response this modem might report to the operating system during the connection process.</span></span> <span data-ttu-id="e228d-673">Os dois primeiros caracteres especificam o tipo de resposta.</span><span class="sxs-lookup"><span data-stu-id="e228d-673">The first two characters specify the type of response.</span></span> <span data-ttu-id="e228d-674">Os dois segundos caracteres especificam informações sobre a conexão que está sendo feita.</span><span class="sxs-lookup"><span data-stu-id="e228d-674">The second two characters specify information about the connection being made.</span></span> <span data-ttu-id="e228d-675">Os segundos dois caracteres são usados apenas para o andamento da negociação ou para os códigos de resposta de conexão.</span><span class="sxs-lookup"><span data-stu-id="e228d-675">The second two characters are used only for Negotiation Progress or Connect response codes.</span></span> <span data-ttu-id="e228d-676">Os próximos oito caracteres especificam a velocidade de linha de modem para modem negociada em bits por segundo (bps).</span><span class="sxs-lookup"><span data-stu-id="e228d-676">The next eight characters specify the modem-to-modem line speed negotiated in bits per second (bps).</span></span> <span data-ttu-id="e228d-677">Os caracteres representam um formato de inteiro longo sem sinal de 32 bits (Byte e palavra invertido).</span><span class="sxs-lookup"><span data-stu-id="e228d-677">The characters represent a 32-bit unsigned long integer format (byte and word reversed).</span></span> <span data-ttu-id="e228d-678">Os últimos oito caracteres indicam que o modem está mudando para uma porta diferente ou velocidade de DTE (equipamento de terminal de dados).</span><span class="sxs-lookup"><span data-stu-id="e228d-678">The last eight characters indicate that the modem is changing to a different port or Data Terminal Equipment (DTE) speed.</span></span> <span data-ttu-id="e228d-679">Normalmente, esse campo não é usado porque os modems fazem conexões em uma velocidade de porta bloqueada, independentemente da velocidade do modem-to-modem ou do equipamento de comunicações de dados (DCE).</span><span class="sxs-lookup"><span data-stu-id="e228d-679">Usually this field is not used because modems make connections at a locked port speed regardless of the modem-to-modem or Data Communications Equipment (DCE) speed.</span></span>

</dd> <dt>

<span data-ttu-id="e228d-680">**RingsBeforeAnswer**</span><span class="sxs-lookup"><span data-stu-id="e228d-680">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-681">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e228d-681">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-682">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-682">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-683">Número de anéis antes que o modem responda a uma chamada de entrada.</span><span class="sxs-lookup"><span data-stu-id="e228d-683">Number of rings before the modem answers an incoming call.</span></span>

<span data-ttu-id="e228d-684">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-684">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-685">**SpeakerModeDial**</span><span class="sxs-lookup"><span data-stu-id="e228d-685">**SpeakerModeDial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-686">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-687">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-688">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeDial")</span><span class="sxs-lookup"><span data-stu-id="e228d-688">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeDial")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-689">Cadeia de caracteres de comando usada para ligar o viva-voz do modem depois de discar um número e desativar o alto-falante quando uma conexão for estabelecida.</span><span class="sxs-lookup"><span data-stu-id="e228d-689">Command string used to turn the modem speaker on after dialing a number, and turning the speaker off when a connection has been established.</span></span>

<span data-ttu-id="e228d-690">Exemplo: "M1"</span><span class="sxs-lookup"><span data-stu-id="e228d-690">Example: "M1"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-691">**SpeakerModeOff**</span><span class="sxs-lookup"><span data-stu-id="e228d-691">**SpeakerModeOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-692">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-693">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-693">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-694">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeOff")</span><span class="sxs-lookup"><span data-stu-id="e228d-694">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOff")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-695">Cadeia de caracteres de comando usada para desativar o alto-falante do modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-695">Command string used to turn the modem speaker off.</span></span>

<span data-ttu-id="e228d-696">Exemplo: "M0"</span><span class="sxs-lookup"><span data-stu-id="e228d-696">Example: "M0"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-697">**SpeakerModeOn**</span><span class="sxs-lookup"><span data-stu-id="e228d-697">**SpeakerModeOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-698">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-699">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-700">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeOn")</span><span class="sxs-lookup"><span data-stu-id="e228d-700">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOn")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-701">Cadeia de caracteres de comando usada para ativar o viva-voz do modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-701">Command string used to turn the modem speaker on.</span></span>

<span data-ttu-id="e228d-702">Exemplo: "m2"</span><span class="sxs-lookup"><span data-stu-id="e228d-702">Example: "M2"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-703">**SpeakerModeSetup**</span><span class="sxs-lookup"><span data-stu-id="e228d-703">**SpeakerModeSetup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-704">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-705">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-705">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-706">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeSetup")</span><span class="sxs-lookup"><span data-stu-id="e228d-706">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeSetup")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-707">Cadeia de caracteres de comando usada para instruir o modem a ativar o viva-voz (até que uma conexão seja estabelecida).</span><span class="sxs-lookup"><span data-stu-id="e228d-707">Command string used to instruct the modem to turn the speaker on (until a connection is established).</span></span>

<span data-ttu-id="e228d-708">Exemplo: "M3"</span><span class="sxs-lookup"><span data-stu-id="e228d-708">Example: "M3"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-709">**SpeakerVolumeHigh**</span><span class="sxs-lookup"><span data-stu-id="e228d-709">**SpeakerVolumeHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-710">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-711">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-711">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-712">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \| SpeakerVolume \_ alta")</span><span class="sxs-lookup"><span data-stu-id="e228d-712">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_High")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-713">Cadeia de caracteres de comando usada para definir o alto-falante do modem para o volume mais alto.</span><span class="sxs-lookup"><span data-stu-id="e228d-713">Command string used to set the modem speaker to the highest volume.</span></span>

<span data-ttu-id="e228d-714">Exemplo: "L3"</span><span class="sxs-lookup"><span data-stu-id="e228d-714">Example: "L3"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-715">**SpeakerVolumeInfo**</span><span class="sxs-lookup"><span data-stu-id="e228d-715">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-716">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e228d-716">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-717">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-717">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-718">Descreve o nível de volume dos tons audíveis do modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-718">Describes the volume level of the audible tones from the modem.</span></span>

<span data-ttu-id="e228d-719">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-719">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e228d-720">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e228d-720">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e228d-721">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e228d-721">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e228d-722">**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="e228d-722">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="e228d-723">**Alta** (3)</span><span class="sxs-lookup"><span data-stu-id="e228d-723">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="e228d-724">**Médio** (4)</span><span class="sxs-lookup"><span data-stu-id="e228d-724">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="e228d-725">**Baixo** (5)</span><span class="sxs-lookup"><span data-stu-id="e228d-725">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="e228d-726">**Desativado** (6)</span><span class="sxs-lookup"><span data-stu-id="e228d-726">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="e228d-727">**Automático** (7)</span><span class="sxs-lookup"><span data-stu-id="e228d-727">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-728">**SpeakerVolumeLow**</span><span class="sxs-lookup"><span data-stu-id="e228d-728">**SpeakerVolumeLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-729">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-729">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-730">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-730">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-731">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \| SpeakerVolume \_ baixo")</span><span class="sxs-lookup"><span data-stu-id="e228d-731">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Low")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-732">Cadeia de caracteres de comando usada para definir o alto-falante do modem para o volume mais baixo.</span><span class="sxs-lookup"><span data-stu-id="e228d-732">Command string used to set the modem speaker to the lowest volume.</span></span>

<span data-ttu-id="e228d-733">Exemplo: "L1"</span><span class="sxs-lookup"><span data-stu-id="e228d-733">Example: "L1"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-734">**SpeakerVolumeMed**</span><span class="sxs-lookup"><span data-stu-id="e228d-734">**SpeakerVolumeMed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-735">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-735">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-736">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-736">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-737">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \| SpeakerVolume \_ Med")</span><span class="sxs-lookup"><span data-stu-id="e228d-737">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Med")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-738">Cadeia de caracteres de comando usada para definir o alto-falante do modem para um volume médio.</span><span class="sxs-lookup"><span data-stu-id="e228d-738">Command string used to set the modem speaker to a medium volume.</span></span>

<span data-ttu-id="e228d-739">Exemplo: "L2"</span><span class="sxs-lookup"><span data-stu-id="e228d-739">Example: "L2"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-740">**Status**</span><span class="sxs-lookup"><span data-stu-id="e228d-740">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-741">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-741">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-742">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-742">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-743">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="e228d-743">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-744">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e228d-744">Current status of the object.</span></span> <span data-ttu-id="e228d-745">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="e228d-745">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e228d-746">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="e228d-746">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e228d-747">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="e228d-747">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e228d-748">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="e228d-748">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e228d-749">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="e228d-749">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e228d-750">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-750">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e228d-751">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e228d-751">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e228d-752">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e228d-752">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e228d-753">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="e228d-753">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e228d-754">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="e228d-754">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e228d-755">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e228d-755">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e228d-756">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e228d-756">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e228d-757">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="e228d-757">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e228d-758">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="e228d-758">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e228d-759">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="e228d-759">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e228d-760">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="e228d-760">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e228d-761">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="e228d-761">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e228d-762">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="e228d-762">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e228d-763">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="e228d-763">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-764">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e228d-764">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-765">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e228d-765">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-766">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-766">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-767">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="e228d-767">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-768">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e228d-768">State of the logical device.</span></span> <span data-ttu-id="e228d-769">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="e228d-769">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e228d-770">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-770">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e228d-771">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e228d-771">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e228d-772">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="e228d-772">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e228d-773">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e228d-773">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e228d-774">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="e228d-774">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e228d-775">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="e228d-775">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-776">**StringFormat**</span><span class="sxs-lookup"><span data-stu-id="e228d-776">**StringFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-777">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-777">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-778">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-778">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-779">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ estruturas de dispositivo de linha de API Win32 \| \| LINEDEVCAPS \| dwStringFormat")</span><span class="sxs-lookup"><span data-stu-id="e228d-779">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Line Device Structures\|LINEDEVCAPS\|dwStringFormat")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-780">Tipo de caracteres usado para o texto passado pelo modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-780">Type of characters used for text passed through the modem.</span></span>

<span data-ttu-id="e228d-781">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="e228d-781">The values are:</span></span>

<dl> <dd><span data-ttu-id="e228d-782">"Formato de cadeia de caracteres ASCII"</span><span class="sxs-lookup"><span data-stu-id="e228d-782">"ASCII string format"</span></span></dd> <dd><span data-ttu-id="e228d-783">"Formato de cadeia de caracteres DBCS"</span><span class="sxs-lookup"><span data-stu-id="e228d-783">"DBCS string format"</span></span></dd> <dd><span data-ttu-id="e228d-784">"Formato de cadeia de caracteres UNICODE"</span><span class="sxs-lookup"><span data-stu-id="e228d-784">"UNICODE string format"</span></span></dd> </dl>

<dt>

<span id="ASCII_string_format"></span><span id="ascii_string_format"></span><span id="ASCII_STRING_FORMAT"></span>

<span data-ttu-id="e228d-785">**Formato de cadeia de caracteres ASCII** ("formato de cadeia de caracteres ASCII")</span><span class="sxs-lookup"><span data-stu-id="e228d-785">**ASCII string format** ("ASCII string format")</span></span>


</dt> <dd></dd> <dt>

<span id="DBCS_string_format"></span><span id="dbcs_string_format"></span><span id="DBCS_STRING_FORMAT"></span>

<span data-ttu-id="e228d-786">**Formato de cadeia de caracteres DBCS** ("formato de cadeia de caracteres DBCS")</span><span class="sxs-lookup"><span data-stu-id="e228d-786">**DBCS string format** ("DBCS string format")</span></span>


</dt> <dd></dd> <dt>

<span id="UNICODE_string_format"></span><span id="unicode_string_format"></span><span id="UNICODE_STRING_FORMAT"></span>

<span data-ttu-id="e228d-787">**Formato de cadeia de caracteres Unicode** ("formato de cadeia de caracteres Unicode")</span><span class="sxs-lookup"><span data-stu-id="e228d-787">**UNICODE string format** ("UNICODE string format")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e228d-788">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="e228d-788">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-789">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e228d-789">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-790">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-790">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-791">Se **for true**, o modem oferece suporte a retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e228d-791">If **TRUE**, the modem supports callback.</span></span>

<span data-ttu-id="e228d-792">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-792">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-793">**SupportsSynchronousConnect**</span><span class="sxs-lookup"><span data-stu-id="e228d-793">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-794">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e228d-794">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-795">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-795">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-796">Se for **true**, síncrona, bem como assíncrona, haverá suporte para a comunicação.</span><span class="sxs-lookup"><span data-stu-id="e228d-796">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

<span data-ttu-id="e228d-797">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-797">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-798">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e228d-798">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-799">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-799">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-800">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-800">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-801">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e228d-801">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e228d-802">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="e228d-802">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="e228d-803">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-803">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-804">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e228d-804">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-805">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-805">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-806">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-806">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-807">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e228d-807">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e228d-808">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="e228d-808">Name of the scoping system.</span></span>

<span data-ttu-id="e228d-809">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-809">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-810">**Terminador**</span><span class="sxs-lookup"><span data-stu-id="e228d-810">**Terminator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-811">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-811">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-812">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-812">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-813">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| terminador de classe de controle" Win32Registry System \\ \\ CurrentControlSet \\ \\ \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="e228d-813">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Terminator")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-814">Cadeia de caracteres que marca o final de uma cadeia de caracteres de comando.</span><span class="sxs-lookup"><span data-stu-id="e228d-814">String that marks the end of a command string.</span></span>

<span data-ttu-id="e228d-815">Exemplo: "<CR"</span><span class="sxs-lookup"><span data-stu-id="e228d-815">Example: "<cr"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-816">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="e228d-816">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-817">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e228d-817">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-818">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-818">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e228d-819">Data e hora da última redefinição do modem.</span><span class="sxs-lookup"><span data-stu-id="e228d-819">Date and time the modem was last reset.</span></span>

<span data-ttu-id="e228d-820">Essa propriedade é herdada do [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-820">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="e228d-821">**Tom**</span><span class="sxs-lookup"><span data-stu-id="e228d-821">**Tone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-822">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-822">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-823">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-823">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-824">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Tom")</span><span class="sxs-lookup"><span data-stu-id="e228d-824">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Tone")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-825">Cadeia de caracteres de comando que instrui o modem a usar o modo de Tom para discagem.</span><span class="sxs-lookup"><span data-stu-id="e228d-825">Command string that instructs the modem to use tone mode for dialing.</span></span> <span data-ttu-id="e228d-826">A linha telefônica deve dar suporte à discagem de Tom.</span><span class="sxs-lookup"><span data-stu-id="e228d-826">The phone line must support tone dialing.</span></span>

<span data-ttu-id="e228d-827">Exemplo: "T"</span><span class="sxs-lookup"><span data-stu-id="e228d-827">Example: "T"</span></span>

</dd> <dt>

<span data-ttu-id="e228d-828">**VoiceSwitchFeature**</span><span class="sxs-lookup"><span data-stu-id="e228d-828">**VoiceSwitchFeature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e228d-829">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e228d-829">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e228d-830">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e228d-830">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e228d-831">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| VoiceSwitchFeature")</span><span class="sxs-lookup"><span data-stu-id="e228d-831">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|VoiceSwitchFeature")</span></span>
</dt> </dl>

<span data-ttu-id="e228d-832">Cadeias de caracteres de comando usadas para ativar os recursos de voz de um modem de voz.</span><span class="sxs-lookup"><span data-stu-id="e228d-832">Command strings used to activate the voice capabilities of a voice modem.</span></span>

<span data-ttu-id="e228d-833">Exemplo: "AT + V"</span><span class="sxs-lookup"><span data-stu-id="e228d-833">Example: "AT+V"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e228d-834">Comentários</span><span class="sxs-lookup"><span data-stu-id="e228d-834">Remarks</span></span>

<span data-ttu-id="e228d-835">A classe **Win32 \_ POTSModem** é derivada de [**CIM \_ POTSModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="e228d-835">The **Win32\_POTSModem** class is derived from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e228d-836">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e228d-836">Requirements</span></span>



| <span data-ttu-id="e228d-837">Requisito</span><span class="sxs-lookup"><span data-stu-id="e228d-837">Requirement</span></span> | <span data-ttu-id="e228d-838">Valor</span><span class="sxs-lookup"><span data-stu-id="e228d-838">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e228d-839">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e228d-839">Minimum supported client</span></span><br/> | <span data-ttu-id="e228d-840">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e228d-840">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e228d-841">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e228d-841">Minimum supported server</span></span><br/> | <span data-ttu-id="e228d-842">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e228d-842">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e228d-843">Namespace</span><span class="sxs-lookup"><span data-stu-id="e228d-843">Namespace</span></span><br/>                | <span data-ttu-id="e228d-844">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e228d-844">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e228d-845">MOF</span><span class="sxs-lookup"><span data-stu-id="e228d-845">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e228d-846"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e228d-846"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e228d-847">DLL</span><span class="sxs-lookup"><span data-stu-id="e228d-847">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e228d-848"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e228d-848"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e228d-849">Confira também</span><span class="sxs-lookup"><span data-stu-id="e228d-849">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e228d-850">**\_POTSMODEM CIM**</span><span class="sxs-lookup"><span data-stu-id="e228d-850">**CIM\_PotsModem**</span></span>](cim-potsmodem.md)
</dt> <dt>

[<span data-ttu-id="e228d-851">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="e228d-851">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
