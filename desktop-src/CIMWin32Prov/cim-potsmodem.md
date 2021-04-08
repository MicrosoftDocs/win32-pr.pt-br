---
description: A \_ classe CIM POTSModem representa um dispositivo que traduz dados binários em modulações de onda para transmissão baseada em som conectando-se à rede do sistema de telefonia antigo (POTS).
ms.assetid: 2740f305-769d-464c-910a-998522f5121b
ms.tgt_platform: multiple
title: Classe CIM_POTSModem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_POTSModem
- CIM_POTSModem.AnswerMode
- CIM_POTSModem.Availability
- CIM_POTSModem.Caption
- CIM_POTSModem.CompressionInfo
- CIM_POTSModem.ConfigManagerErrorCode
- CIM_POTSModem.ConfigManagerUserConfig
- CIM_POTSModem.CountriesSupported
- CIM_POTSModem.CountrySelected
- CIM_POTSModem.CreationClassName
- CIM_POTSModem.CurrentPasswords
- CIM_POTSModem.Description
- CIM_POTSModem.DeviceID
- CIM_POTSModem.DialType
- CIM_POTSModem.ErrorCleared
- CIM_POTSModem.ErrorControlInfo
- CIM_POTSModem.ErrorDescription
- CIM_POTSModem.InactivityTimeout
- CIM_POTSModem.InstallDate
- CIM_POTSModem.LastErrorCode
- CIM_POTSModem.MaxBaudRateToPhone
- CIM_POTSModem.MaxBaudRateToSerialPort
- CIM_POTSModem.MaxNumberOfPasswords
- CIM_POTSModem.ModulationScheme
- CIM_POTSModem.Name
- CIM_POTSModem.PNPDeviceID
- CIM_POTSModem.PowerManagementCapabilities
- CIM_POTSModem.PowerManagementSupported
- CIM_POTSModem.RingsBeforeAnswer
- CIM_POTSModem.SpeakerVolumeInfo
- CIM_POTSModem.Status
- CIM_POTSModem.StatusInfo
- CIM_POTSModem.SupportsCallback
- CIM_POTSModem.SupportsSynchronousConnect
- CIM_POTSModem.SystemCreationClassName
- CIM_POTSModem.SystemName
- CIM_POTSModem.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7fbaeedd1de4006dfdccbcec313a7428d7b7f03
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920416"
---
# <a name="cim_potsmodem-class"></a><span data-ttu-id="0bcc1-103">\_Classe CIM POTSModem</span><span class="sxs-lookup"><span data-stu-id="0bcc1-103">CIM\_POTSModem class</span></span>

<span data-ttu-id="0bcc1-104">A classe **CIM \_ POTSModem** representa um dispositivo que traduz dados binários em modulações de onda para transmissão baseada em som conectando-se à rede do sistema de telefonia antigo (POTS).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-104">The **CIM\_POTSModem** class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bcc1-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0bcc1-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0bcc1-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0bcc1-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bcc1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bcc1-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C546-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_POTSModem : CIM_LogicalDevice
{
  uint16   AnswerMode;
  uint16   Availability;
  string   Caption;
  uint16   CompressionInfo;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  string   Description;
  string   DeviceID;
  uint16   DialType;
  boolean  ErrorCleared;
  uint16   ErrorControlInfo;
  string   ErrorDescription;
  uint32   InactivityTimeout;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    RingsBeforeAnswer;
  uint16   SpeakerVolumeInfo;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="0bcc1-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0bcc1-110">Members</span></span>

<span data-ttu-id="0bcc1-111">A classe **CIM \_ POTSModem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0bcc1-111">The **CIM\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="0bcc1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0bcc1-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0bcc1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0bcc1-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0bcc1-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="0bcc1-114">Methods</span></span>

<span data-ttu-id="0bcc1-115">A classe **CIM \_ POTSModem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-115">The **CIM\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="0bcc1-116">Método</span><span class="sxs-lookup"><span data-stu-id="0bcc1-116">Method</span></span>                                                               | <span data-ttu-id="0bcc1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bcc1-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bcc1-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-118">**Reset**</span></span>](reset-method-in-class-cim-potsmodem.md)                 | <span data-ttu-id="0bcc1-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="0bcc1-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="0bcc1-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-potsmodem.md) | <span data-ttu-id="0bcc1-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="0bcc1-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0bcc1-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0bcc1-124">Properties</span></span>

<span data-ttu-id="0bcc1-125">A classe **CIM \_ POTSModem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-125">The **CIM\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0bcc1-126">**Respondermode**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-126">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-129">Configuração de resposta automática ou de retorno de chamada atual para o modem.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-129">Current auto-answer or call-back setting for the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bcc1-130">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0bcc1-131">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0bcc1-132">**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-132">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="0bcc1-133">**Resposta manual** (3)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-133">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="0bcc1-134">**Resposta automática** (4)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-134">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="0bcc1-135">**Resposta automática com retorno de chamada** (5)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-135">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bcc1-136">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-136">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-137">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-139">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-140">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-140">Availability and status of the device.</span></span>

<span data-ttu-id="0bcc1-141">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-141">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0bcc1-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bcc1-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0bcc1-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0bcc1-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0bcc1-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0bcc1-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0bcc1-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="0bcc1-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0bcc1-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0bcc1-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0bcc1-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0bcc1-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0bcc1-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0bcc1-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-155">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0bcc1-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-157">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-157">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0bcc1-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-159">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-159">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0bcc1-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0bcc1-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-162">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0bcc1-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-164">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0bcc1-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-166">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0bcc1-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-168">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0bcc1-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-170">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0bcc1-171">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-171">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-174">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-175">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-175">Short textual description of the object.</span></span>

<span data-ttu-id="0bcc1-176">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-177">**CompressionInfo**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-177">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-178">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-180">Características de compactação de dados do modem.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-180">Data compression characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bcc1-181">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0bcc1-182">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="0bcc1-183">**Sem compactação** (2)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-183">**No Compression** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="0bcc1-184">**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-184">**MNP 5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="0bcc1-185">**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-185">**V.42bis** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bcc1-186">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-187">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-189">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-190">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-190">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0bcc1-191">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0bcc1-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0bcc1-193"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-194">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0bcc1-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0bcc1-196">(1)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-197">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0bcc1-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0bcc1-199">(2)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0bcc1-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0bcc1-201">(3)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-202">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0bcc1-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0bcc1-204">(4)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-205">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-205">Device is not working properly.</span></span> <span data-ttu-id="0bcc1-206">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0bcc1-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0bcc1-208">(5)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-209">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0bcc1-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0bcc1-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-212">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0bcc1-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0bcc1-214">(7)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0bcc1-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0bcc1-216">(8)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-217">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0bcc1-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0bcc1-219">(9)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-220">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-220">Device is not working properly.</span></span> <span data-ttu-id="0bcc1-221">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0bcc1-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0bcc1-223">(10)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-224">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0bcc1-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0bcc1-226">(11)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-227">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0bcc1-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0bcc1-229">12</span><span class="sxs-lookup"><span data-stu-id="0bcc1-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-230">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0bcc1-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0bcc1-232">(13)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-233">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0bcc1-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0bcc1-235">(14)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-236">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0bcc1-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0bcc1-238">(15)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-239">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0bcc1-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0bcc1-241">(16)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-242">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0bcc1-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0bcc1-244">(17)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-245">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0bcc1-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0bcc1-247">(18)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-248">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0bcc1-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0bcc1-250">(19)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0bcc1-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0bcc1-252">(20)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-253">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0bcc1-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0bcc1-255">(21)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-256">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-256">System failure.</span></span> <span data-ttu-id="0bcc1-257">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0bcc1-258">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0bcc1-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0bcc1-260">(22)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-261">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0bcc1-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0bcc1-263">(23)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-264">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-264">System failure.</span></span> <span data-ttu-id="0bcc1-265">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0bcc1-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0bcc1-267">(24)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-268">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0bcc1-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0bcc1-270">(25)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-271">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0bcc1-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0bcc1-273">(26)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-274">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0bcc1-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0bcc1-276">(27)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-277">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0bcc1-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0bcc1-279">(28)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-280">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0bcc1-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0bcc1-282">(29)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-283">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-283">Device is disabled.</span></span> <span data-ttu-id="0bcc1-284">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-284">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0bcc1-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0bcc1-286">(30)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-286">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-287">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-287">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0bcc1-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0bcc1-289">(31)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-289">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-290">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-290">Device is not working properly.</span></span> <span data-ttu-id="0bcc1-291">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-291">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0bcc1-292">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-292">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-293">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-295">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-295">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-296">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-296">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0bcc1-297">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-298">**CountriesSupported**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-298">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-299">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-301">Países ou regiões em que o modem pode operar.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-301">Countries or regions in which the modem can operate.</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-302">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-302">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-305">País ou região para o qual o modem está programado no momento.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-305">Country or region for which the modem is currently programmed.</span></span> <span data-ttu-id="0bcc1-306">Quando há suporte para vários países ou regiões, essa propriedade define qual deles está selecionado atualmente para uso.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-306">When multiple countries or regions are supported, this property defines which one is currently selected for use.</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-310">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-311">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0bcc1-312">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0bcc1-313">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-314">**CurrentPasswords**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-314">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-315">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-315">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-317">Senhas definidas no momento para o modem.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-317">Currently defined passwords for the modem.</span></span> <span data-ttu-id="0bcc1-318">Essa matriz pode ser deixada em branco por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-318">This array can be left blank for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-319">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-319">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-322">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-322">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-323">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-323">Textual description of the object.</span></span>

<span data-ttu-id="0bcc1-324">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-324">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-325">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-325">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-326">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-328">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-329">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-329">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="0bcc1-330">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-331">**Dialtype**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-331">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-332">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-334">Tipo de discagem usado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-334">Type of dialing that is used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bcc1-335">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="0bcc1-336">**Tom** (1)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-336">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="0bcc1-337">**Pulse** (2)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-337">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bcc1-338">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-338">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-339">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-339">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-341">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-341">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="0bcc1-342">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-343">**ErrorControlInfo**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-343">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-344">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-346">Características de correção de erro do modem.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-346">Error correction characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bcc1-347">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-347">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0bcc1-348">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-348">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="0bcc1-349">**Sem correção de erro** (2)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-349">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="0bcc1-350">**MNP5 4** (3)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-350">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="0bcc1-351">**LAPM** (4)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-351">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bcc1-352">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-352">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-355">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-355">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="0bcc1-356">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-357">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-357">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-358">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-360">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-361">Limite de tempo (em segundos) para a desconexão automática da linha telefônica se nenhum dado for trocado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-361">Time limit (in seconds) for automatic disconnection of the phone line if no data is exchanged.</span></span> <span data-ttu-id="0bcc1-362">Um valor de 0 (zero) indica que esse recurso está presente, mas não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-362">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-363">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-363">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-364">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-366">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-367">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-367">Date and time the object was installed.</span></span> <span data-ttu-id="0bcc1-368">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-368">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0bcc1-369">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-370">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-371">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-373">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0bcc1-374">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-375">**MaxBaudRateToPhone**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-375">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-376">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-378">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-378">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-379">Velocidade máxima de comunicação configurável para acessar o sistema telefônico.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-379">Maximum settable communication speed for accessing the phone system.</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-380">**MaxBaudRateToSerialPort**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-380">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-381">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-383">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-383">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-384">Velocidade máxima de comunicação configurável para a porta COM para um modem externo.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-384">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="0bcc1-385">Digite 0 (zero) se não for aplicável.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-385">Enter 0 (zero) if not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-386">**MaxNumberOfPasswords**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-386">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-387">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-389">Número máximo de senhas definíveis no próprio modem.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-389">Maximum number of passwords definable in the modem itself.</span></span> <span data-ttu-id="0bcc1-390">Se não houver suporte para esse recurso, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-390">If this feature is not supported, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-391">**ModulationScheme**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-391">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-392">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-394">Esquema de modulação do modem.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-394">Modulation scheme of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bcc1-395">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-395">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0bcc1-396">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-396">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0bcc1-397">**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-397">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="0bcc1-398">**Bell 103** (3)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-398">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="0bcc1-399">**Bell 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-399">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="0bcc1-400">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-400">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="0bcc1-401">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-401">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="0bcc1-402">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-402">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="0bcc1-403">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-403">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="0bcc1-404">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-404">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="0bcc1-405">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-405">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="0bcc1-406">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-406">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bcc1-407">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-407">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-408">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-410">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-410">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-411">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-411">Label by which the object is known.</span></span> <span data-ttu-id="0bcc1-412">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-412">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0bcc1-413">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-414">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-414">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-415">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-417">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-417">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-418">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-418">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="0bcc1-419">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0bcc1-420">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0bcc1-420">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-421">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-421">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-422">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-422">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-423">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-424">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-424">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="0bcc1-425">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-425">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bcc1-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0bcc1-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0bcc1-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0bcc1-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-430">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-430">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0bcc1-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-432">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-432">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0bcc1-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-434">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="0bcc1-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="0bcc1-435">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-435">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="0bcc1-436">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-436">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0bcc1-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-438">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0bcc1-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0bcc1-440">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-440">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0bcc1-441">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-441">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-442">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-442">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-443">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-444">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-444">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="0bcc1-445">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0bcc1-445">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0bcc1-446">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-446">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="0bcc1-447">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0bcc1-447">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="0bcc1-448">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-449">**RingsBeforeAnswer**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-449">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-450">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-450">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-452">Número de anéis antes que o modem responda a uma chamada de entrada.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-452">Number of rings before the modem answers an incoming call.</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-453">**SpeakerVolumeInfo**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-453">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-454">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-456">Nível de volume dos tons audíveis do modem.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-456">Volume level of the audible tones from the modem.</span></span> <span data-ttu-id="0bcc1-457">Por exemplo, alto, médio ou baixo volume pode ser relatado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-457">For example, high, medium, or low volume can be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bcc1-458">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-458">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0bcc1-459">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0bcc1-460">**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-460">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="0bcc1-461">**Alta** (3)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-461">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="0bcc1-462">**Médio** (4)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-462">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="0bcc1-463">**Baixo** (5)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-463">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="0bcc1-464">**Desativado** (6)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-464">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="0bcc1-465">**Automático** (7)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-465">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bcc1-466">**Status**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-466">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-467">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-468">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-469">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-469">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-470">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-470">Current status of the object.</span></span> <span data-ttu-id="0bcc1-471">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0bcc1-472">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0bcc1-472">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0bcc1-473">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0bcc1-474">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0bcc1-475">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bcc1-476">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0bcc1-477">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0bcc1-478">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0bcc1-479">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0bcc1-480">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0bcc1-481">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0bcc1-482">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0bcc1-483">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0bcc1-484">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bcc1-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-486">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-488">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="0bcc1-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-489">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-489">State of the logical device.</span></span> <span data-ttu-id="0bcc1-490">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-490">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0bcc1-491">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0bcc1-492">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bcc1-493">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0bcc1-494">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0bcc1-495">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0bcc1-496">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bcc1-497">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-497">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-498">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-498">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-499">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-500">Se **for true**, o modem dará suporte ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-500">If **TRUE**, the modem supports call-back.</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-501">**SupportsSynchronousConnect**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-501">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-502">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-502">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-503">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-504">Se for **true**, síncrona, bem como assíncrona, haverá suporte para a comunicação.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-504">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-506">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-508">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-509">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-509">Scoping system's creation class name.</span></span>

<span data-ttu-id="0bcc1-510">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-512">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-513">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-514">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0bcc1-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-515">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-515">Scoping system's name.</span></span>

<span data-ttu-id="0bcc1-516">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bcc1-517">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-517">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bcc1-518">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-518">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0bcc1-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0bcc1-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bcc1-520">Data e hora da última redefinição deste controlador.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-520">Date and time this controller was last reset.</span></span> <span data-ttu-id="0bcc1-521">Isso pode significar que o controlador estava desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-521">This could mean the controller was powered down, or reinitialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bcc1-522">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bcc1-522">Remarks</span></span>

<span data-ttu-id="0bcc1-523">A classe **CIM \_ POTSModem** é derivada do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-523">The **CIM\_POTSModem** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0bcc1-524">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-524">WMI does not implement this class.</span></span> <span data-ttu-id="0bcc1-525">Para classes WMI derivadas do **CIM \_ POTSModem**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0bcc1-525">For WMI classes derived from **CIM\_POTSModem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0bcc1-526">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-526">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0bcc1-527">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0bcc1-527">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bcc1-528">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bcc1-528">Requirements</span></span>



| <span data-ttu-id="0bcc1-529">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bcc1-529">Requirement</span></span> | <span data-ttu-id="0bcc1-530">Valor</span><span class="sxs-lookup"><span data-stu-id="0bcc1-530">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bcc1-531">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bcc1-531">Minimum supported client</span></span><br/> | <span data-ttu-id="0bcc1-532">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0bcc1-532">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0bcc1-533">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bcc1-533">Minimum supported server</span></span><br/> | <span data-ttu-id="0bcc1-534">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bcc1-534">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0bcc1-535">Namespace</span><span class="sxs-lookup"><span data-stu-id="0bcc1-535">Namespace</span></span><br/>                | <span data-ttu-id="0bcc1-536">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0bcc1-536">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0bcc1-537">MOF</span><span class="sxs-lookup"><span data-stu-id="0bcc1-537">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bcc1-538"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bcc1-538"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bcc1-539">DLL</span><span class="sxs-lookup"><span data-stu-id="0bcc1-539">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bcc1-540"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bcc1-540"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bcc1-541">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bcc1-541">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcc1-542">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0bcc1-542">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

